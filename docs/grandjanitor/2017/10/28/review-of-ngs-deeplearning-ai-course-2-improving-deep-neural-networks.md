---
title: "Review of Ng's deeplearning.ai Course 2: Improving Deep Neural Networks"
date: 2017-10-28
categories: ["Andrew Ng", "course review", "deep learning", "deep neural network", "Geoff Hinton", "Machine Learning", "review"]
tags: ["deep learning", "DNN", "review"]
---

# Review of Ng's deeplearning.ai Course 2: Improving Deep Neural Networks

*[image not recovered: mike-kotsch-204195.jpg]*

(My Reviews on [Course 2](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/) and [Course 3](/grandjanitor/2017/11/25/review-of-ngs-deeplearning-ai-course-3-structuring-machine-learning-projects/).)

In your life, there are times you think you know something, yet genuine understanding seems to elude you. It's always frustrating, isn't it? For example, why would all these seemingly simple concepts such as gradients or regularization can throw us off when we learn them since Day 1 of our learning in machine learning?

In programming, there's a term called "grok", grokking something usually means that not only you know the term, but you also have intuitive understanding of the concept. Or as in "Zen and the Art of Motorcycle Maintenance" [1], you just try to dive deep into a concept, as if it is a journey...... For example, if you really think about speech recognition, then you would realize the frame independence assumption [2] is very important. Because it simplifies the problem in both search and parameter estimation. Yet it certainly introduces a modeling error. These small things which are not mentioned in classes or lectures are things you need to grok.

That brings us to Course 2 of deeplearning.ai. What are you grokking in this Course? After you take Course 1, should you take Course 2? My answer is yes and here is my reasoning. 

# Really, What is Gradient Descent?

Gradient descent is a seemingly simple subject - say you want to find a minima of the function a convex function, so you follow the gradient down hill and after many iterations, you eventually hit the minima. Sounds simple right?

Of course, once you start to realize that functions are normally not convex, and they are n-dimensional, and there can be plateaus. Or when you follow the gradient, but it happens to be a wrong direction! So you will have zigzagging when you try to descend. It's a little bit like descending from a real mountain, yet you don't really can't see n-dimensional space!

That explains the early difficulty of deep learning development - Stochastic gradient descent (SGD) was just too slow back in 2000 for DNN. That results in very interesting research of restricted Boltzmann machine (RBM) which was stacked and used to initialize DNN, which was prominent subject of Hinton's NNML after Lecture 8, or *pretraining*, which is still being used in some recipes in speech recognition as well as financial prediction.

But we are not doing RBM any more! In fact, research in RBM is not as fervent as in 2008. [4] Why? It has to do with people just understand more about SGD and can run it better - it has to do with initialization, e.g. [Glorot's](http://proceedings.mlr.press/v9/glorot10a.html) and [He's initialization](https://arxiv.org/pdf/1512.03385.pdf). It also has to do with how gradient descent is done - ADAM is our current best.

So how do you learn these stuffs? Before Ng deeplearning.ai's class, I would say knowledge like this spread out on courses such as cs231n or cs224n. But as I mentioned in the [Course 1's review](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/), those are really courses with specific applications in mind. Or you can go to read Michael Nielsen's [Neural Network and Deep Learning](http://neuralnetworksanddeeplearning.com/). Of course, Nielsen's work is a book. So it really depends on whether you have the patience to work through the details while reading. (Also see[my review](/grandjanitor/2016/10/02/reading-michael-nielsons-neural-networks-and-deep-learning/) of the book.)

Now you don't have to. The one-stop shop is Course 2. Course 2 actually covers the material I just mentioned such as initialization, gradient descent, as well as deeper concepts such as regularization and batch normalization. That makes me recommend you to keep on taking the course after you finish Course 1. If you take the class, and are also willing to read Sebastian Ruder's [Review of SGD](http://ruder.io/optimizing-gradient-descent/) or Grabriel Goh's [Why Momentum Really Works](https://distill.pub/2017/momentum/), you would be much ahead of the game.

As a note, I also like Andrew breaks down many of the SGD algorithm as a smoothing algorithm. That's a new insight for me even after I used SGD many times. 

# Is it hard?

Nope, as Math goes, Course 1 is probably toughest. Of course, even in Course 1, you will finish coursework faster if you don't overthink the problem. Most notebooks have the derived results for you. On the other hand, you do want to derive the formulae, you do need to have decent skill in matrix calculus. 

# Is it Necessary to Understand These Details?; Also Top-Down vs Bottom-Up learning, which is Better?

A legitimate question here is that : well, in our current state of deep learning which we have so many toolkits which already implemented techniques such as ADAM. Do I really need to dig so deep?

I do think there are always two views in learning - one is from top-down, which in deep learning, perhaps is to read a bunch of papers, learn the concepts and see if you can wrap you head around them. the[fast.ai class](http://course.fast.ai/) is one of them. And 95% of the current AI enthusiasts are following such paths.

What's the problem of the top-down approach? Let me go back to my first paragraph - which is - do you really *grok* something when you do something top-down? I frequently can't. In my work life, I also heard senior people say that top-down is the way to go. Yet, when I went ahead to check if they *truly* understand an implementation. They frequently can't give a satisfactory answer. That happens to a lot of senior technical people who later turn to more management. Literally, they lost their touch.

On the other hand, every time, I pop up an editor and write an algorithm, I gain tremendous understanding! For example, I was asked to write a forward inference once with C, you better know what you are doing when you write in C! In fact, I come to have opinion these days that you *have to* implement an algorithm once before you can claim you understand it.

So how come there are two sides of the opinion then? One of my speculations is that back in 80s/90s, students are often taught to learn how to write program in *first writing.* That create mindsets that you have to think up a perfect program before you start to write one. Of course, in ML, such mindset is highly *impractical* because and the ML development process are really experimental. You can't always assume you perfect the settings before you try something.

Another equally dangerous mindset is to say *"if you are too focused on details, then you miss the big picture won't come up with something new!"* . This I heard a lot when I first do research and it's close to most BS-ty thing I've heard. If you want to come up with something new, the first thing you should learn is *all the details* of existing works. The so called "big picture" and "details" are always interconnected. That's why in the AIDL forum, we never see young kids, who say "*Oh I have this brand new idea, which is completely different from all previous works!", would* go anywhere. That's because you always learn how to walk before you run. And knowing the details has no downsides.

Perhaps this is my long reasons why Ng's class is useful for me, even after I read many literature. I distrust people who only talk about theory but don't show any implementation. 

# Conclusion

This concludes my review of Course 2. To many people, after they took Course 1, they just decide to take Course 2, I don't blame them, but you always want to ask if your time is well-spent.

To me though, taking Course 2 is not just about understanding more on deep learning. It is also my hope to grok some of the seemingly simple concepts in the field. Hope that my review is useful and I will keep you all posted when my Course 3's review is done.

Arthur

Footnotes: [1] As Pirsig said - it's really not about motorcycle maintenance.

[2] Strictly speaking, it is *conditional frame independence* assumption. But practitioners in ASR frequently just called it frame independence assumption.

[3] Also see [HODL's interview with Ruslan Salakhutdinov](https://www.youtube.com/watch?v=OT91E6_Qm1A&index=1&list=PLkDaE6sCZn6FcbHlDzbVzf3TVgxzxK7lr), his account is first hand on the rise and fall of RBM.
