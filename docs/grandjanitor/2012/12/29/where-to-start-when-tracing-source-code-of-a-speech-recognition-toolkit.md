---
title: "Where to start when tracing source code of a speech recognition toolkit?"
date: 2012-12-29
categories: ["Baum-Welch algorithm", "Boost", "C++", "decoding APIs", "java", "open source speech recognition", "source code", "sphinx3", "Sphinx4", "Thought", "training scripts", "Viterbi algorithm"]
---

# Where to start when tracing source code of a speech recognition toolkit?

Modern speech recognition software are complicated piece of software. To understand it, you need to have some basic understanding of the principle of speech recognition, as well as some ideas on the programming language being used. 

By now, you may hear a lot of people say they know about a speech recognizer. And by now, you probably realize that most of these people have absolutely no ideas what's going on inside a recognizer. So if you are reading this blog message, you are probably telling yourself, "I might want to trace the codebase of some recognizers' code." Be it Sphinx, HTK, Julius, Kaldi or whatever codebase you are looking at.

For the above toolkits, I will say I only know in detail about Sphinx, probably a little bit about HTK's HVite. But I won't say the same for others. In fact, even in Sphinx, I only know intimately about Sphinx 3/SphinxTrain/sphinxbase triplet. So just like you, I hope to learn more.

So here it begs the question: how would you trace a speech recognition toolkit codebase? If you think it is easy, probably because you worked in speech recognition for a while and you probably shouldn't read this post.

Let's just use sphinx as an example, there are hundreds of files in each component of Sphinx. So where should you start? A blunt approach would be reading each of the file one by one. That's not a smart the way. So here is a suggestion for you : focus on the following four things,

1. Viterbi algorithm
2. Workflow of training
3. Baum-Welch algorithm.
4. Estimation algorithms of language models.

When you know where the Viterbi algorithm is, you will soon figure out how the feature vector is generated. On the same vein: if you know where the Baum-Welch algorithm, you will probably know how the statistics are generated. If you know the workflow of the training, then you will understand the how the model is "evolved". If you know how the language model is estimated, then you would have understanding of one of the most important heuristic of the search. 

Some of you may protest, how about the front-end? Isn't that important too? True, but not when you try to understand a codebase. For all practical purpose, a feature vector is just an N-dimensional vector. The waveform is just an NxT matrix. You can certainly do a lot of fancy things on this NxT matrix. But when you think of Viterbi and Baum-Welch, they probably just read the frames and then calculate Gaussian distribution. That's pretty much it's how much you want to know a front-end. 

How about adaptation algorithms? That I think it's important. But it should probably go after understanding of the major things in the code. Because no matter whether you are doing adaptation online or doing this in speaker adaptive training. It is something on top of the Baum-Welch algorithm. Some implementation stick adaptation within the Baum-Welch executable. There is certainly nothing wrong about it. But it is still a kind of add-on. 

How about decoding API? Those are useful things to know but it is more important when you just need to write an application. For example, in Sphinx4, you just need to know how to call the Recognizer class. In sphinx3, live_decode is what you need to know. But only understanding those won't give you too much insights of how the decoder really works. 

How about the data structure? Those are sort of important and should be understood when you try to understand a certain algorithm. In the case of languages such as Java and C++, you should probably take notes on a custom-made data structure. Or whether the designer call a specific data structure libraries. Like Boost in C++. 

I guess this pretty much sums it all. Now let me get back to one non-trivial item on the list, which is the workflow of training. Many of you might think that recognition systems differ from each other because they have different decoders. Dead wrong! As I stressed from [time to time](http://grandjanitor.blogspot.com/2012/05/what-should-be-our-focus-in-speech.html), they differ because they have different acoustic models and language models. So that's why in many research labs, much effort was put on preserving the parameters and procedures of how models is trained. Much effort was also put to fine tuned this procedure. 

On this part, I got to say open source speech recognition still has long long way to go. For starter, there is no much sharing of recipes among speech hobbyists. What many try to do is to search for a good model. If you don't know how to train a model, you probably don't even know how to improve it for you own project. 

Arthur

---

## Comments

**MOHAMED OLUD MOHAMED KHELIFA** (2016-04-07):

How introducing phoneme length parameter into standard HMM ?
Knowing the length of a specific phoneme can be used to limit the length of the HMM chain that represent it, which in turn increase the speed of recognition and its accuracy, so, how introducing phoneme length parameter into standard HMM model and producing new one to be used in building accurate ASR system using HTK?
thanks for any reply

**Arthur Chan** (2016-04-29):

What you are thinking perhaps is to add a duration model into HMM. Basically means that instead of having a geometric distribution of length, you want to have certain distribution of length.

The easiest way, while not the best, is perhaps using N-best rescoring with your duration model. Say first you dump 100-best out of your decoder, then try to use your duration model to score your N-best list one-by-one.

You can also incorporate your duration model into a decoder. I think that's much harder and require more low-level programming.

Will it help though? I doubt. Many people tried duration model with limited success. Or else it become parts of the standard setup. But it's a good exercise and you will certainly draw some fun out of it.

