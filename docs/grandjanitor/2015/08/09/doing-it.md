---
title: "Doing It"
date: 2015-08-09
---

# Doing It

I was usually in a group, try to tackle a task. We might miss a certain implementation, a certain proof, or even some of us lack of some simple knowledge of certain programming language. And you can guess the consequence: all planning efforts stop here. One of us would say "Let's not pursue that path. There's too much risk and unknown."

I ponder about these situations for a while. There is a surprisingly simple solution for all of these problems : spend a little time to try out a simple solution.

For example, when you don't know a certain language, can you write an "if"-clause or even a "Hello World" with that language? Further can you write a for-loop. For me, google this kind of questions for around 10 minutes usually gives me basic knowledge of the language and implement a simple program. And surprisingly, that's what ~70% needs - repeat an action (for-loop) under certain condition (an if-statement).

Another example, suppose you don't have an implementation of say [linear regression](https://en.wikipedia.org/wiki/Linear_regression). Can you simplify the problem first? e.g. Can you first implement linear regression with 1 variable? (i.e. only the linear term.) If you can do it, can you then extend your implementation to multiple variables? Implementing an algorithm, unlike understanding an algorithm, doesn't take as much time. So it's silly to get caught up before you start.

As a final example, how about learning a certain machine learning algorithm? What should you first do? My approach would be first running some existing examples of the algorithm. For example, if you want to learn the basic of SVM, try to run examples from the [tutorial of libsvm](http://www.csie.ntu.edu.tw/~cjlin/papers/guide/guide.pdf). If you want to learn DNN, go through the tutorial of [deep learning tutorial](http://deeplearning.net/tutorial/). For sure, you will not get every nuance in machine learning this way. e.g. how to make a decision when you get stuck? How to decide if you machine learning algorithm is suitable for the task? Yes. Those take experience and more in-depth methodology. (Check out [Andrew Ng's Machine Learning Class.](https://www.coursera.org/learn/machine-learning/home/info)) But knowing these algorithms from top-down or solely based on mathematics is unlikely to get you too far.

One common retort from people opposing of doing it is that you usually don't quite get state-of-the-art performance in the first few passes. I do agree certain parts of their viewpoints. Sometimes, more planning gives you a more refined first solution. But for the most time, you don't conjure knowledge out of nothing, you *build up* knowledge. It's useless to be too caught up in thinking some time.

I also don't oppose to understanding. For example, doing derivations and proofs for algorithm always help your implementation. But in practice, getting a feel about an algorithm would also help you to understand an algorithm.

If you ask me, what is really shameful is that we were sometimes blocked by our subtle fear of learning something new. That doesn't do any good for you, or the team. That's what I am driving at in this article.

Arthur

Reference: I was inspired by this post : "[Concrete, Then Abstract](http://www.cs.uni.edu/~wallingf/blog/archives/monthly/2015-08.html#e2015-08-04T13_00_49.htm)". I also highly recommend "[Zen and the Art of Motorcycle Maintenance: An Inquiry Into Values](http://www.amazon.com/Zen-Art-Motorcycle-Maintenance-Inquiry/dp/0060589469)" to my readers.
