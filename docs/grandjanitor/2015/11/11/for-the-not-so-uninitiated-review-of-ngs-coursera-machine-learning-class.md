---
title: "For the Not-So-Uninitiated: Review of Ng's Coursera Machine Learning Class"
date: 2015-11-11
categories: ["Machine Learning"]
tags: ["Andrew Ng", "Coursera", "Machine Learning"]
---

# For the Not-So-Uninitiated: Review of Ng's Coursera Machine Learning Class

I heard about [Prof. Andrew Ng's Machine Learning Class](https://www.coursera.org/learn/machine-learning/home/welcome) for a long time. As MOOC goes, this is a famous one. You can say *the class actually popularized MOOC*. Many people seem to be benefited from the class and it has ~70% positive rating. I have no doubt that Prof. Ng has done a good job in teaching non-data scientist on a lot of difficult concepts in machine learning.

On the other hand, if you are more a experienced practitioner of ML, i.e. like me, who has worked on a sub field of the industry (eh, speech recognition......) for a while, would the class be useful for you?

I think the answer is *yes* for several reasons: 
1. *You want to connect the dots* : most of us work in a particular machine learning problem for a while, it's easy to fall into certain tunnel vision inherent to a certain type of machine learning. e.g. For a while, people think that using 13 dimension of MFCC is the norm in ASR. So if you learn machine learning through ASR, it's natural to think that feature engineering is not important. **That cannot be more wrong!** If you look at reviews of Kaggle winners, most will tell you they spent majority of time to engineer feature. So learning machine learning from ground up would give you a new perspective.
2. *You want to learn the language of machine learning properly:*  One thing I found which is useful Ng's class is that it doesn't assume you know everything (unlike many postgraduate level classes). e.g. I found that Ng's explanation of the term of bias vs variance makes a lot of sense - because the terms have to be interpreted differently to make sense. Before his class, I always have to conjure in my head on the equation of bias and variance. True, it's more elegant that way, but for the most part an intuitive feeling is more crucial at work.
3. *You want to practice*: Suppose you are like me, who has been focusing on one area in ASR, e.g. in my case, I spent quite a portion of my time just work on the codebase of the in-house engine. Chances are you will lack of opportunities to train yourself on other techniques. e.g. I never implemented linear regression (a one-liner), logistic regression before. So this class will give you an opportunity to play with these stuffs hand-ons.
4. *Your knowledge is outdated* : You might have learned pattern recognition or machine learning once back in school. But technology has changed so you want to keep up. I think Ng's class is a good starter class. There are more difficult ones such as Hinton's [Neural Network for Machine Learning](https://www.coursera.org/course/neuralnets), the [Caltech class by Prof. Yaser Abu-Mostafa](https://work.caltech.edu/telecourse.html), or the [CMU's class ](http://www.cs.cmu.edu/~tom/10701_sp11/lectures.shtml)by Prof. Toni Mitchell. If you are already proficient, yes, may be you should jump to those first.

So this is how I see Ng's class. It is deliberately simple and leaned on the practical side. Math is minimal and calculus is nada. There is no deep learning and you don't have to implement algorithm to train SVM. There is o latest stuffs such as random forest and gradient boosting. But it's a good starter class. It also get you good warm up if you hadn't learn for a while.

Of course, this also speaks quite a bit of the downsides of the class, there are just too many practical techniques which are not covered. For example, if you work on a few machine learning class, you will notice that SVM with RBF kernel is not the most scalable option. Random forest and gradient boosting is usually a better choice. And even when using SVM, using a linear kernel with right packages (such as pegasus-ml) would give you much faster run. In practice, it could mean if you can deliver or not. So this is what Ng's class is lacking, it doesn't cover many important modern techniques.

In a way, you should see it as your *first* *machine learning class*. The realistic expectation should be you need to keep on learning. (Isn't that speak for everything?)

Issues aside, I feel very grateful to learn something new in machine learning again. That was since I took my last ML class back in 2002, the landscape of the field was so different back then. For that, let's thank to Prof. Ng! And Happy Learning.

Arthur 

# Postscript at 2017 April

Since taking this first class of coursera, I took several other classes such as [Dragomir Radev's NLP](https://www.coursera.org/learn/natural-language-processing) and perhaps more interesting to you, [Hinton's Neural Network Machine Learning](https://www.coursera.org/learn/neural-networks). You can find my reviews on the following hyperlinks:

http://thegrandjanitor.com/2015/12/22/radevs-coursera-introduction-to-natural-language-processing-a-review/

http://thegrandjanitor.com/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/

I also have a mind to write a review for perfect beginner of machine learning, so stay tuned! :)

(20151112) Edit: tunnel effects -&gt; tunnel vision. Fixed some writing issues. (20170416) In the process of organizing my articles. So I do some superficial edits.

Reference:

Andrew Ng's Coursera Machine Learning Class : https://www.coursera.org/learn/machine-learning/home/welcome

Geoff Hinton's Neural Networks for Machine Learning: https://www.coursera.org/course/neuralnets

The Caltech class: https://work.caltech.edu/telecourse.html

The CMU class: http://www.cs.cmu.edu/~tom/10701_sp11/lectures.shtml
