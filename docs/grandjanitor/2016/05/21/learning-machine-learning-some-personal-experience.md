---
title: "Learning Machine Learning - Some Personal Experience"
date: 2016-05-21
categories: ["deep learning", "Machine Learning"]
---

# Learning Machine Learning - Some Personal Experience

## Introduction

Some context: a good friend of mine, Waikit Lau, starts a facebook group called "[Deep Learning](https://www.facebook.com/groups/DeepNetGroup/)". It is a gathering place of many deep learning enthusiasts around the globe. And so far it is almost 400 members strong. Waikit kindly gave me the admin right of the group; I was able to interact with all members since, and had a lot of fun. 

When asked "Which topic do you like to see in "Deep Learning"?", surprisingly enough, "Learning Deep Learning" is the topic most members would like to see more. So I decided to write a post, summarizing my own experience of learning deep learning, and machine learning in general. 

## My Background

Not every one could predict the advent of deep learning, neither do I. I was trained as a specialist in automatic speech recognition (ASR), with half of the time focusing on research (at HKUST, CMU, BBN), the other half on implementation (Speechworks, CMUSphinx). That reflects in my current role, [Principal Speech Architect](https://www.linkedin.com/in/arthchan2003?trk=nav_responsive_tab_profile), which my research-to-implementation is around 50-50. If you are being nice to me, you can say I was quite familiar with standard modeling in speech recognition, with passable programming skills. Perhaps what I gain from ASR, is more an understanding in languages and linguistics, which I would described as cool party tricks. But real-life speech recognition only use little linguistic [1].

To be frank though, while ASR used a lot of machine learning techniques such as GMM, HMM, n-grams, my skills in general machine learning were clearly lacking. For a while, I didn't have an acute sense of dangerous issues such as over- and under-fitting, nor I would able to foresee the rise of deep neural network in so many different fields. So when my colleagues start to tell me, "Arthur, you got to check out this Microsoft's work using deep neural network!" I was mostly suspicious at the time and couldn't really fathom its importance. Obviously I was *too specialized* in ASR - if I had ever give a deeper thought on "[universal approximation theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem)", the rise of DNN would make a lot of sense to me. I can only blame myself for my ignorance.

That is a long digression. So long story short: I woke up about 4 years ago and said "screw it!" I decided to "empty my cup" and learn again. I decided to learn everything I can learn on neural networks, and in general machine learning again. So this article is about some of the lessons I learn. 

## Learning The Jargons

If you are an absolute beginner, the best way to start is to take a good on-line class. For example[Andrew Ng's machine learning class ](https://www.coursera.org/learn/machine-learning) ([my review](/grandjanitor/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/)) would be a very good place to start. Because Ng's class is generally known to be gentle to beginners.

Ideally you want to finish the whole course, from there you will be able to have some basic understanding on what you are doing. For example, you want to know that "Oh, if I want to make a classifier, I need a train set and a test set; And it's absolutely wrong that they are the same". Now this is a rather deep thought, and actually there are people I know just take short cut and use the training set as the test set. (*Bear in mind, they or their love ones suffer eventually. :)* ) If you don't know anything about machine learning, learning how to setup data set is the absolute minimum you want to learn.

You would also want to know some basic machine learning methods such as linear regression, logistic regression and decision tree. Most method you will use in practice require these techniques as building blocks. e.g. If you don't really know logistic regression, understanding neural network would be much tougher. If you don't understand linear classifier, understand support vector machine would be tough too. If you have know idea what decision tree, no doubt you will confuse about random forest.

Learning basic classifiers also equipped you with intuitive understanding of core algorithms, e.g. you will need to know stochastic gradient descent (SGD) for many things you do in DNN.

Once you go through first class, then there are two things you want to do: one is to actually work on a machine learning problem, the other is to learn more about certain techniques. So let me split them into two sections: 

## How To Work On Actual Machine Learning Problems

#### Where Are The Problems?

If you are still in school and specialize in machine learning, chances you are funded by agency. So more than likely you already have a task. My suggestion for you is try to learn up your own problem as much as you can, and make sure you master all the latest techniques first, because that will help your daily job and career.

On the other hand, what if you were not major in machine learning? For example, what if you were an experienced programmer in the first place, and now shift your attention to machine learning? The simple answer for that is [*Kaggle*](https://www.kaggle.com/). Kaggle is a multi-purpose venue where you can learn and compete in machine learning. You will also start from basic tasks such as MNIST or CIFAR-10 to first hone your skill.

Another good source of basic machine learning tasks, are tutorials of machine learning toolkits. For example, [Theano's deeplearning.net tutorial](http://deeplearning.net/tutorial/) is my first taste on MNIST, from there I also follow the tutorial to train up the [IMDB sentiment classifier](http://deeplearning.net/tutorial/lstm.html#lstm) and well as [polyphonic music generator](http://deeplearning.net/tutorial/rnnrbm.html#rnnrbm).

My only criticism to Kaggle is that it lacks of the most challenging problem you can find in the field. e.g. At the time when imagenet was not yet solved, I would hope a large scale computer vision would be hold at Kaggle. And now when machine reading is the most acute problem, I would hope that there are tasks which every one in the world would try to tackle.

If you have my concerns, then consider other evaluations sources. In your field, there got to be a competition or two holding every years. Join them, and make sure you gain experience from these competitions. By far, I think it is the fastest way to learn. 

#### Practical Matter 1 - Linux Skills

For the most part, what I found tripping many beginners are linux skills, especially software installation. For that I would recommend you to use Ubuntu. Many machine learning software can be installed by simple apt-get. If you are into python, try out [anaconda python](https://www.continuum.io/downloads), because it will save you a lot of time in software installation.

Also remember that Google is your friend. Before you feel frustrated about a certain glitch and give up, always turn to google, paste your error message, to see if you find an answer. Ask forums if you still can't resolve your issue. Remember, working on machine learning requires you to have certain problem-solving skill. So don't feel deter by small things.

Oh you ask what if you are using windows? Nah, switch to Linux, a majority of machine learning tools ran in Linux anyway. Many people would also recommend [Docker](https://www.docker.com/). So far I heard both good and bad things about it. So I can't say if I like it or not. 

#### Practical Matter 2 - Machines

Another showstopper for many people is compute. I will say though if you are a learner, the computational requirement can be just a simple dual-core desktop with no GPU cards. Remember, a lot of powerful machine learning tools are developed before GPU card became trendy. e.g. libsvm is mostly a CPU-based software and all Theano's tutorial can be completed within a week with a decent CPU-only machine. (I know because I did that before.)

On the other hand, if you have to do a moderate size task. Then you should buy a decent GPU card, a GTX980 would be a choice consumer card, for a more supported workstation grade card, Quadro series would be nice. Of course, if you can come up with 5k, then go for a Tesla K40 or K80. The GPU card you use directly affect your productivity. If you know how to build a computer, consider to DIY one. Tim Dettmer has couple of articles (e.g. [here](http://timdettmers.com/2015/03/09/deep-learning-hardware-guide/)) on how to build a decent machine for deep learning. Though you might never reach the performance of a [8-GPU card monster](https://code.facebook.com/posts/1687861518126048/facebook-to-open-source-ai-hardware-design/), you will be able to test with pleasure on all standard techniques including DNN, CNN and LSTM. 

#### Once You Have a Taste

For the most part, your first few tasks will teach you quite a lot of machine learning. Then the next problem you will encounter is how do you progressively improve your classifier performance. I will address that next. 

## How To Learn Different Machine Learning Methods

As you might already know, there are many ways to learning machine learning. Some will approach it mathematically and try to come up with an analysis of how a machine technique works. That's what you will learn when you go through school training, i.e. say a 2-3 year master program, or the first 3-4 year of a PhD program.

I don't think that type of learning has anything wrong. But machine learning is also a discipline which requires real-life experimental data to confirm your theoretical knowledge. An overly theoretical approach would sometimes hurt your learning. That said, you will need both practical and theoretical understanding to work well in practice.

So what should you do? I will say machine learning should be learned through 3 aspects, they are 
1. Running the Program,
2. Hacking the Source Code,
3. Learning the Math (i.e. Theory).

## Running the Program - A Thinking Man Guide

In my view, by far the most important skill in machine learning is *to run* a certain technique. Why? Wouldn't that the theory is important too? Why don't we go to first derive an algorithm from the first principle, and then write our own program?

In practice, I found that starting that a top-down approach, i.e. go from theory to implementation, can work. But most of the time, you will easily pigeonhole yourself into certain technique, and couldn't quite see the big picture of the field.

Another flaw of the top-down approach is that it assumes you would understand more from just the principle. In practice, you might need to deal with multiple types of classifiers at work, and it's hard to understand their principle in a timely manner. Besides, having practical experience of running will teach you aspects of the technique. For example, have you run libsvm on a million data point, with each vector in the dimension of a thousand? Then you will notice that type of algorithm to find support vectors makes a huge difference. You will also appreciate why many practitioners from big companies would suggest beginners to learn random forest soon, because in practice random forest is the faster and more scalable solution.

Let me sort of bite my tongue: While it is meant to be a practice, at this stage, you should try very hard to *feel* and *understand* a certain technique. If you are new, this is also a stage where you should ask if general principle such as *bias vs variance* work in your domain.

What is the mistake you can make while using a technique for beginners? I think the biggest is you decide to run certain things *without thinking why,* that's detrimental to your career. For example, many people would read a paper, pick up all techniques the author used, then rush to rerun all these experiments themselves. While this is usually what people do in evaluation/competition, it is a big mistake in real industrial scenario. You should always think about if a technique would work for you - "Is it accurate but too slow?", "Is its performance good but takes up too much memory?", "Are there any good integration route which fits to our existing codebase?" Those are all tough questions you should answer in practice.

I hope you get an impression from me that *being practical in machine learning requires a lot of thinking too.*  Only when you master this aspect of knowledge, then you are ready to take up more difficult parts of our work, i.e. changing the code, algorithm and even the theory itself. 

## Hacking the Source Code

I believe the more difficult task after you successfully run an experiment, is to change the algorithm itself. Mastery of using a program perhaps ties to your general skills in Linux. Whereas mastery of source code would tie to your coding skills in lower-level language such as C/C++/Java.

Making the source code works require you the capability to *read* and *understand* a source code base, a valuable skill in practice. Reading a code base requires a more specialized type of reading - you want to keep notes of a source file, make sure you understand each of the function calls, which could go many levels deep. gdb is your friend, and your reading session should be based on both gdb and eye-balling the source code. Setting conditional break points and display important variables. These are the tricks. And at the end, make sure you can spell out the big picture of the program - *W**hat does it do*? W*hat algorithm does it implement?*  *Where is the important source files?*  And more importantly, *if I was the one who wrote the program,* *how would I write it?*

What I said so far applies for all types of programs, for machine learning, this is a stage you should focus on just the algorithm. e.g. you can easily implement SGD of linear regression without understanding the math. So why would you want to decouple math out of the process then? The reason is that there are always multiple implementations for a same technique and each implementation can be based on slightly different theories. Once again, chasing down the theory would take you too much time.

And do not underestimate the work required to learn the Math behind even the simplest technique in the field. Consider just linear regression, and consider how people have thought about it as 1) optimizing the squared loss, 2) as a maximum likelihood problem [2], then you will notice it is not a simple topic as you learned in Ng's class. While I love the Math, would not knowing the Math affect your daily work? Not in most circumstances. On the other hand, that will be situations you want to just focus on implementations. That's why decoupling theory and practice is a good thinking. 

## Learning The Math and The Theory

That brings us to our final stage of learning - the theory of machine learning. Man, this is such a tough thing to learn, and I don't really do it well myself. But I can share you some of my experience.

First thing first, as I am an advocate of bottom-up learning in machine learning, why would we want to learn *any theory at all*?

In my view, there are several use of theory, 
1. **Simplify your practice:** e.g. knowing direct method of linear regression would save you a lot of typing when implementing one using SGD.
2. **Identify BS:** e.g. You have a data set with two classes with prior 0.999:0.001, your colleague has created a classifier with 99.8% accuracy and decide he has done his job.
3. **Identify redundant idea:** someone in marketing and sales ask why can't we create more data point by squaring every elements of the data point. You should know how to answer, "That is just polynomial regression."
4. **Have fun with theory and the underlying mathematics**,
5. **Think of a new idea**
6. ~~**Brag before your colleagues**~~ ~~**and show how smart you are.**~~

(There is no 6. Don't try to understand theory because you want to brag. And for that matter, stop bragging.)

So now we establish theory can be useful. How do you learn it? By far I think the most important means are to listen to good lectures, reading papers, and actually do the math,

With lectures, you goal is to gather insight from experienced people. So I would recommend the Ng's class as the first class, then Hinton's [Neural Networks For Machine Learning](https://www.coursera.org/course/neuralnets). I also heard Koller's class on [Graphical Models](https://class.coursera.org/pgm-003) are good. If you understand Mandarin, H. T. Lin's [classes on support vector machine ](https://class.coursera.org/ntumlone-002)are perhaps the best.

On papers, subscribe to[arxiv.org](http://arxiv.org/) today, get an RSS feed for yourself, read at least the headlines daily to learn what's new. That's where I first learn many of the important concepts last few years: LSTM, LSTM with attention, highway networks etc.

If you are new, check out the "Awesome resources", like[Awesome Deep Learning](https://github.com/ChristosChristofidis/awesome-deep-learning), that's where you find all basic papers to read.

And eventually you will find that just listening to lecture and reading papers don't explain enough, this is the moment you should go to the "Bible". When I say Bible, we are really talking about 7-8 textbook which are known to be good in the field: 
- Bishop's [Pattern Recognition and Machine Learning](http://research.microsoft.com/en-us/um/people/cmbishop/prml/), also known as PRML
- Duda and Hart's Pattern Classification, usually known as "Duda and Hart". Note that you want to buy the 3rd edition, but reading the 2nd edition also gives you a historical sense of how the field has evolved.
- Hasti/Tibshirani/Friedman's [Elements of Statistical Learning](http://statweb.stanford.edu/~tibs/ElemStatLearn/)
- Barber's [Bayesian Reasoning and Machine Learning](http://web4.cs.ucl.ac.uk/staff/D.Barber/pmwiki/pmwiki.php?n=Brml.HomePage), or BRML
- Murphy's [Machine Learning: a Probabilistic Perspective](http://www.cs.ubc.ca/~murphyk/MLbook/)
- MacKay's Information Theory, Inference and Learning Algorithms
- Goodfellow/Bengio/Courville's [Deep Learning](http://www.deeplearningbook.org/)
- Tom Mitchell's Machine Learning.

If you have to start with one book, consider either [Pattern Classification](http://www.amazon.com/dp/0471703508/ref=pd_lpo_sbs_dp_ss_2?pf_rd_p=1944687442&pf_rd_s=lpo-top-stripe-1&pf_rd_t=201&pf_rd_i=0471056693&pf_rd_m=ATVPDKIKX0DER&pf_rd_r=0NWYPPMWWNPPW0V6AEEC) by Duda and Hart or [Patten Recognition and Machine Learning](http://www.amazon.com/Pattern-Recognition-Learning-Information-Statistics/dp/0387310738/ref=sr_1_1?s=books&ie=UTF8&qid=1463857253&sr=1-1&keywords=bishop+machine+learning) (PRML) by C. M. Bishop. (Those are the only I read deep as well.) In my view, the former is suitable for a 3rd year undergraduate or graduate students to tackle. There are many computer exercises, so you will enjoy a lot in both math problem solving and programming. PRML is more for advanced graduates, like a PhD. PRML is known to be more Bayesian, in a way, it's more modern.

And *do the Math*, especially for the first few chapters, where you would be frustrated by more advanced calculus problems. Noted though, both Duda and Hard, and PRML's exercises are guided. Try to spread out this kind of Math exercise overtime, for example, I try to spend 20-30 minutes to tackle one problem in PRML a day. Write down all of your solutions and attempts in a note book. You will be greatly benefited from this effort. You will gain valuable insights of different techniques: their theory, their motivations, their implementations as well as their notable variants.

Finally, if you have tough time on the Math, don't stay on the same problem all the time. If you can't solve a problem after a week, look it up on google, or go to standard text such as [Solved Problems in Analysis](http://www.amazon.com/Solved-Problems-Analysis-Functions-Mathematics/dp/0486493903). There is no shame of looking up the answers if you had tried. 

## Conclusion

No one can hit the ground running and train a Google's "[convolutional LSTM](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43455.pdf)" on 80000 hours of data in one day. Nor one can think of the very smart idea of using multiplier in a RNN. (i.e. [LSTM](http://deeplearning.cs.cmu.edu/pdfs/Hochreiter97_lstm.pdf)), [using attention to do sequence-to-sequence learning](http://arxiv.org/abs/1406.1078), or reformulating neural network such that [a very deep one is trainable](https://arxiv.org/abs/1505.00387). It is hard to understand the fundamentals of concepts such as LSTM or CNN, not to say to innovate on them.

But you got start somewhere, in this article I tell you my story of how I started and restarted this learning process. I hope you can join me in learning. Just like all of you, I am looking forward to see what deep learning will bring to humanity. And rest assure, you and I will enjoy the future more because we understand more behind the scene.

You might also like[Learning Deep Learning - My Top Five List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/).

Arthur

[1] As Fred Jelinek said "Every time I fire a linguist, the performance of our speech recognition system goes up.(https://en.wikiquote.org/wiki/Fred_Jelinek)

---

## Comments

**Test** (2017-11-21):

Great article . Somethings i would love to contribute with little suggestions

There is space missing "theMath" in first line of paragraph above the title "Learning The Math and The Theory" ,

Lot of acronyms , would be great to have wiki links or somethings plus make href open in new tab rather than current one .

(will remove this comment soon )

> **grandjanitor** (2017-11-21):
>
> Thanks for the correction! You may consider to do "Ctrl-tab" to start a new page. In this way you won't mess up your reading. Good Luck!

