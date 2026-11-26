---
title: "Commentary on SphinxTrain1.07's bw (Part I)"
date: 2013-01-10
categories: ["backward algorithm", "Baum-Welch algorithm", "bw", "Forward algorithm", "L Rabiner", "open source speech recognition", "scaling", "source code", "speed", "sphinxtrain", "SphinxTrain1.07", "streams", "X. D. Huang"]
---

# Commentary on SphinxTrain1.07's bw (Part I)

I was once asked by a fellow who didn't work in ASR on how the estimation algorithms in speech recognition work. That's a tough question to answer. From the high level, you can explain how properties of Q function would allow an increase of likelihood after each re-estimation. You can also explain how the Baum-Welch algorithm is derived from the Q-function and how the estimation algorithm can eventually expressed by greeks, and naturally link it to the alpha and bet pass. Finally, you can also just write down the reestimation formulae and let people perplex about it. 

All are options, but this is not what I wanted nor the fellow wanted. We hoped that somehow there is one single of entry in understanding the Baum-Welch algorithm. Once we get there, we will grok. Unfortunately, that's impossible for Baum-Welch. It is really a rather deep algorithm, which takes several type of understanding. 

In this post, I narrow down the discussion to just Baum-Welch in SphinxTrain1.07. I will focus on the coding aspect of the program. Two stresses here:

1. How Baum-Welch of speech recognition in practice is different from the theory?
2. How different parts of the theory is mapped to the actual code.

In fact, in Part I, I will just describe the high level organization of the Baum-Welch algorithm in bw. I assumed the readers know what the Baum-Welch algorithm is. In Part II, I will focus on the low level functions such as *next_utt_state, foward, backward_update, accum_global .*

(At a certain point, I might write another post just to describe Baum-Welch, This will help my Math as well......)

Unlike the [post of setting up Sphinx4](http://grandjanitor.blogspot.com/2012/12/sphinx-4-from-c-background-setting-up.html). This is not a post for faint of heart. So skip the post if you feel dizzy.

**Some Fun Reading Before You Move On**

Before you move on, here are three references which I found highly useful to understand Baum-Welch in speech recognition. They are

1. L. Rabiner and B. H. Juang, Fundamentals of Speech Recognition. Chapter 6. "Theory and Implementation of Hidden Markov Model." p.343 and p.369. *Comments: In general, the whole Chapter 6 is essential to understand HMM-based speech recognition. There are also a full derivation of the re-estimation formulae. Unfortunately, it only gives the formula without proof for the most important case, in which observation probability was expressed as Gaussian Mixture Model (GMM).*
2. X. D. Huang, A. Acero and H. W. Hon, Spoken Language Processing. Chapter 8. "Hidden Markov Models" *Comments: written by one of the authors of Sphinx 2, Xuedong Huang, the book is a very good review of spoken language system. Chapter 8 in particular has detailed proof of all reestimation algorithms. If you want to choose one book to buy in speech recognition. This is the one. The only thing I would say it's the typeface of greeks are kind of ugly.*
3. X. D. Huang, Y. Ariki, M. A. Jack, Hidden Markov Models for Speech Recognition. Chapter 5, 6, 7. *Comments: again by Xuedong Huang, I think this is the most detail derivations I ever seen on continuous HMM in books. (There might be good papers I don't know of). Related to Sphinx, it has a chapter of semi-continuous HMM (SCHMM) as well.*

bw also features rather nice code commentaries. My understanding is that it is mostly written by Eric Thayer, who put great effort to pull multiple fragmented codebase together and form the embryo of today's SphinxTrain.

**Baum-Welch algorithm in Theory**  
**  
**Now you read the references, in a very high-level what does a program of Baum-Welch estimation does? To summarize, we can think of it this way

\* For each training utterance  

1. Build an HMM-network to represent it.
2. Run Forward Algorithm
3. Run Backward Algorithm
4. From the Forward/Backward, calculate the statistics (or counts or posterior scores depends on how you call it.)

\* After we run through all utterances, estimate the parameters (means, variances, transition probability etc....) from the statistics.

Sounds simple? I actually skipped a lot of details here but this is the big picture.

**Baum-Welch algorithm in Practice**  
**  
**  

There are several practical concerns on doing Baum-Welch in practice. These are particularly important when it is implemented for speech recognition. 

1. **Scaling of alpha/beta scores** : *this* *is explained in detail in Rabiner's book (p.365-p.368). The gist is that when you calculate the alpha or beta scores. They can easily exceed the range of precision of any machines. It turns out there is a beautiful way to avoid this problem.*
2. **Multiple observation sequences**: or stream. *this is a little bit archaic, but there are still some researches work on having multiple streams of features for speech recognition (e.g. combining the lip signal and speech signal).*
3. **Speed**: *most implementation you see are not based on a full run of forward or backward algorithm. To improve speed, most implementations use a beam to constrained the search.*
4. **Different types of states**: *you can have HMM states which are emitting or non-emitting. How you handle it complicates the implementation.*

You will see bw has taken care of a lot of these practical issues. In my opinion, that is the reason why the whole program is a little bit bloated (5000 lines total). 

*  
*

**Tracing of bw: High Level**  
**  
**Now we get into the code level. I will follow the version of bw from SphinxTrain1.07. I don't see there are much changes in 1.08 yet. So this tracing is very likely to be applicable for a while.

I will organize the tracing in this way. First I will go through the high-level flow of the high-level. Then I will describe some interesting places in the code by line numbers.

**main() - src/programs/bw/main.c**  
**  
**This is the high level of main.c (Line 1903 to 1914)

```
 main ->   
    main_initialize()  
    if it is not mmie training  
      main_reestimate()  
    else  
      main_reestimate_mmi()  

```

main_initialize()  
We will first go forward with *main_initialize*()

```
 main_initailize  
 -> initialize the model inventory, essentially means 4 things, means (mean) variances (var), transition matrices (tmat), mixture weights (mixw).  
 -> a lexicon (or .... a dictionary)  
 -> model definition  
 -> feature vector type  
 -> lda (lda matrix)  
 -> cmn and agc  
 -> svspec  
 -> codebook definition (ts2cb)  
 -> mllr for SAT type of training.   

```

Interesting codes:  

- Line 359: *extract diagonal matrix if we specified a full one.*
- Line 380: *precompute Gaussian distribution. That's usually mean the constant and almost always most the code faster.*
- Line 390: *specify what type of reestimation.*
- Line 481: *check point. I never use this one but it seems like something that allow the training to restart if network fails.*
- Line 546 to 577: *do MLLR transformation for models: for SAT type of training.*

(Note to myself: got to understand why svspec was included in the code.)

**main_reestimate()**  
**  
**Now let's go to main_reestimate. In a nutshell, this is where the looping occurred.

```
      -> for every utterane.   
        -> corpus_get_generic_featurevec (get feature vector (mfc))  
        -> feat_s2mfc2feat_live (get the feature vector)  
        -> corpus_get_sent (get the transcription)  
        -> corpus_get_phseg (get the phoneme segmentation.)  
        -> pdumpfn (open a dump file, this is more related Dave's constrained Baum-Welch research)  
        -> next_utt_states() /*create the state sequence network. One key function in bw. I will trace it more in detail.  */ 
        -> if it is not in Viterbi mode.  
         -> baum_welch_update()  /*i.e. Baum-Welch update */
         else   
         -> viterbi()  /*i.e. Viterbi update)

```

Interesting code:

- Line 702: several parameter for the algorithm was initialized including *abeam, bbeam, spthres, maxuttlen.*

    - *abeam* and *bbeam* are essentially the beam sizes which control forward and backward algorithm.
    - *maxuttlen*: this controls how large an utterance will be read in. In these days, I seldom see this parameter set to something other than 0. (i.e. no limit).
    - *spthres: "*State posterior probability floor for reestimation. States below this are not counted". ** Another parameter I seldom use......

#### baum_welch_update()

```
 baum_welch_update()  
 -> for each utterance
       forward() (forward.c) (<This is where the forward algorithm is -Very complicated. 700 lines)  
       if -outphsegdir is specified , dump a phoneme segmentation.  
       backward_update() (backward.c Do backward algorithm and also update the accumulator)  
           (<- This is even more complicated 1400 lines)  
 -> accum_global() (Global accumulation.)   
         (<- Sort of long, but it's more trivial than forward and backwrd.)  

```

Now this is the last function for today. If you look back to the section of "Baum-Welch in theory". you will notice how the procedure are mapped onto Sphinx. Several thoughts:

1. One thing to notice is that *forward, backward_update* and *accum_global* need to work together. But you got to realize all of these are long complicated functions. So like *next_utt_state**,* I will separate the discussion on another post.
2. Another comment here: *backward_update* not only carry out the backward pass. It also do an update of the statistics.

#### Conclusion of this post

In this post, I went through the high-level description of Baum-Welch algorithm as well as how the theory is mapped onto the C codebase. My next post (will there be one?), I will focus on the low level functions such as *next_utt_state, forward, backward_update* and *accum_global*.

Feel free to comment. 

Arthur

---

## Comments

**telfer cronos** (2013-11-06):

Thanks. Your post is a lot of fun. I will look at it much more carefully today. I have used sphinx - perhaps only the pre-compiled demonstrations. ANyway seeing your blog has inspired me to have another look at Sphinx.

Richard Mullins

**Arthur Chan** (2013-11-17):

Hey Richard,

Both HTK and Sphinx is great toolkits. If you are into ASR, read the source codes of both, I believe you will learn great insights (as well as idiosyncrasies) in the process.

Of course, don't forget Kaldi!

Arthur

**telfer cronos** (2013-11-06):

Thanks. Your post is a lot of fun. I will look at it much more carefully today. I have used sphinx - perhaps only the pre-compiled demonstrations. ANyway seeing your blog has inspired me to have another look at Sphinx.

Richard Mullins

