---
title: "Reading Michael Nielsen's \"Neural Networks and Deep Learning\""
date: 2016-10-02
categories: ["deep learning", "deep neural network", "DNN"]
tags: ["beginners", "deep learning", "DNN", "intermediate"]
---

# Reading Michael Nielsen's "Neural Networks and Deep Learning"

# Introduction

Let me preface this article: after I wrote [my top five list on deep learning resources](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/), one oft-asked question is "What is the Math prerequisites to learn deep learning?" My first answer is Calculus and Linear Algebra, but then I will qualify certain techniques of Calculus and Linear Algebra are more useful. e.g. you should already know gradient, differentiation, partial differentiation and [Lagrange multipliers](https://en.wikipedia.org/wiki/Lagrange_multiplier), you should know [matrix differentiation](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf) and preferably [trace trick](http://nonconditional.com/2012/06/the-trace-trick-for-gaussian-log-likelihood/) , [eigen-decomposition](https://en.wikipedia.org/wiki/Eigendecomposition_of_a_matrix) and such. If your goal is to understand machine learning in general, then having good skills in integrations and knowledge in analysis helps. e.g. 1-2 stars problems of Chapter 2 at [PRML](https://www.microsoft.com/en-us/research/people/cmbishop/) [1] requires some knowledge of advanced function such as gamma, beta. Having some Math would help you go through these questions more easily. 

Nevertheless, I find that people who want to learn Math first before approaching deep learning miss the point. Many engineering topics was not motivated by pure mathematical pursuit. More often than not, an engineering field is motivated by a physical observation. Mathematics is more like an aid to imagine and create a new solution. In the case of deep learning. If you listen to [Hinton](https://en.wikipedia.org/wiki/Geoffrey_Hinton), he would often say he tries to first come up an idea and makes it work mathematically later. His insistence of working on neural networks at the time of kernel method stems more from his observation of the brain. "If the brain can do it, how come we can't?" should be a question you ask every day when you run a deep learning algorithm. I think *these observations are fundamental* to deep learning. And you should go through arguments of why people think neural networks are worthwhile in the first place. Reading classic papers from[Wiesel and Hubel](http://hubel.med.harvard.edu/papers/HubelWiesel1962Jphysiol.pdf) helps. [Understanding the history of neural network ](http://www.andreykurenkov.com/writing/a-brief-history-of-neural-nets-and-deep-learning/)helps. Once you read these materials, you will quickly grasp the big picture of much development of deep learning.

Saying so, I think there are certain topics which are fundamental in deep learning. They are not necessarily very mathematical. For example, I will name back propagation [2] as a very fundamental concept which you want to get good at. Now, you may think that's silly. "I know backprop already!" Yes, backprop is probably in every single machine learning class. It will easily give you an illusion that you master the material. But you can always learn more about a fundamental concept. And back propagation is important theoretically and practically. You will encounter back propagation either as a user of deep learning tools, a writer of a deep learning framework or an innovator of new algorithm. So a thorough understanding of backprop is very important, and one course is not enough.

This very long digression finally brings me to the great introductory book [Michael Nielson's *Neural Network and Deep Learning*](http://neuralnetworksanddeeplearning.com/) (NNDL) The reason why I think Nielson's book is important is that it offers an alternative discussion of back propagation as an algorithm. So I will use the rest of the article to explain why I appreciate the book so much and recommend nearly all beginning or intermediate learners of deep learning to read it. 

# First Impression

I first learned about "Neural Network and Deep Learning" (NNDL) from going through Tensorflow's tutorial. My first thought is "ah, another blogger tries to cover neural network". i.e. I didn't think it was promising. At that time, there were already plenty of articles about deep learning. Unfortunately, they often repeat the same topics without bringing anything new. 

# Synopsis

Don't make my mistake! NNDL is a great introductory book which balance theory and practice of deep neural network. The book has 6 chapters: 
1. [Using neural network to recognize digits](http://neuralnetworksanddeeplearning.com/chap1.html) - the basic of neural network, a basic implementation using python (network.py)
2. [How the backpropagation algorithm works](http://neuralnetworksanddeeplearning.com/chap2.html) - various explanation(s) of back propagation
3. [Improving the way neural networks learn](http://neuralnetworksanddeeplearning.com/chap3.html) - standard improvements of the simple back propagation, another implementation in python (network2.py)
4. [A visual proof that neural nets can compute any function](http://neuralnetworksanddeeplearning.com/chap4.html) - universal approximation algorithm without the Math, plus fun games which you can approximate function yourself
5. [Why are deep neural networks hard to train?](http://neuralnetworksanddeeplearning.com/chap5.html) - practical difficultie of using back propagation, [vanishing gradients](https://en.wikipedia.org/wiki/Vanishing_gradient_problem)
6. [Deep Learning](http://neuralnetworksanddeeplearning.com/chap6.html) - [convolution neural network ](https://en.wikipedia.org/wiki/Convolutional_neural_network)(CNN), the final implementation based on Theano (network3.py), recent advances in deep learning (circa 2015).

The accompanied python scripts are the gems of the book. network.py and network2.py can run in plain-old python. You need Theano on network3.py, but I think the strength of the book really lies on network.py and network2.py (Chapter 1 to 3) because if you want to learn CNN, [Kaparthy's lectures ](http://cs231n.github.io/convolutional-networks/)probably gives you bang for your buck. 

# Why I like Nielsen's Treatment of Back Propagation?

Reading Nielson's exposition of neural network is the sixth time I learn about the basic formulation of back propagation [see footnote 3]. So what's the difference between his treatment and my other reads then?

Forget about my first two reads because I didn't care enough neural networks enough to know why back propagation is so named. But my latter reads pretty much give me the same impression of neural network: "a neural network is merely a stacking of logistic functions. So how do you train the system? Oh, just differentiate the loss functions, the rest is technicalities." Usually the books will guide you to verify certain formulae in the text. Of course, you will be guided to deduce that "error" is actually "propagating backward" from a network. Let us call this view *network-level* view. In a *network-level* view, you really don't care about how individual neurons operate. All you care is to see neural network as yet another machine learning algorithm.

The problem of network level view is that it doesn't quite explain a lot of phenomena about back propagation. * Why is it so slow some time? Why certain initialization schemes matter?*  Nielsen does an incredibly good job to break down the standard equations into 4 fundamental equations (BP1 to BP4 in Chapter2). Once interpret them, you will realize "Oh, saturation is really a big problem in back propagation" and "Oh, of course you have to initialize the weights of neural network with non-zero values. Or else nothing propagate/back propagate!" These insights, while not mathematical in nature and can be understood with college calculus, is deeper understanding about back propagation.

Another valuable part about Nielsen's explanation is that it comes with a accessible implementation. His first implementation (network.py) is a 74 lines python in idiomatic python. By adding print statements on his code, you will quickly grasp on a lot of these daunting equations are implemented in practice. For example, as an exercise, you can try to identify how he implement BP1 to BP4 in network.py. It's true that there are books and implementations about neural network, but the description and implementation don't always come together. Nielsen's presentation is a rare exception. 

# Other Small Things I Like

- Nielsen correctly point out the Del symbol in machine learning is more like a convenient device rather than its more usual meaning like the Del operator in Math.
- In Chapter 4, Nielson mentioned universal approximation of neural network. Unlike standard text book which points you to a bunch of papers with daunting math, Nielsen created a javascript which allows you to approximate functions (!), which I think those are great ways to learn intuition behind the theorem.
- He points out that it's important to differentiate *activation* and the *weighted input*. In fact, this point is one thing which can confuse you when reading a derivation of back propagation because textbooks usually use different symbols for activation and weighted input.

There are many of these insightful comments from the book, I encourage you to read and discover them. 

# Things I don't like

- There are many exercises of the book. Unfortunately, there is no answer keys. In a way, this make Nielson more an old-style author which encourage readers to think. I guess this is something I don't always like because spending time to think of one single problem forever doesn't always give you better understanding.
- Chapter 6 gives the final implementation in Theano. Unfortunately, there is not much introductory material on Theano within the book. I think this is annoying but forgivable, as Nielson pointed out, it's harder to introduce Theano and introductory book. I would think anyone interested in Theano should probably go through the standard Theano's tutorial at [here](http://deeplearning.net/software/theano/tutorial/) and [here](http://deeplearning.net/tutorial/).

# Conclusion

All-in-all, I highly recommend *[Neural Network and Deep Learning ](http://neuralnetworksanddeeplearning.com/chap2.html)* to any beginning and intermediate learners of deep learning. If this is the first time you learn back propagation, NNDL is a great general introductory book. If you are like me, who already know a thing or two about neural networks, NNDL still have a lot to offer.

Arthur

[1] In my view, PRML's problem sets have 3 ratings, 1-star, 2-star and 3-star. 1-star usually requires college-level of Calculus and patient manipulation, 2-star requires some creative thoughts in problem solving or knowledge other than basic Calculus. 3-star are more long-form questions and it could contain multiple 2-star questions in one. For your reference, I solved around 100 out of the 412 questions. Most of them are 1-star questions.

[2] The other important concept in my mind is gradient descent, and it is still an active research topic.

[3] The 5 reads before "learnt" it once back in HKUST, read it from Mitchell's book, read it from Duda and Hart, learnt it again from Ng's lecture, read it again from PRML. My 7th is to learn from Karparthy's lecture, he present the material in yet another way. So it's worth your time to look at them.

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me (Arthur) at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).
