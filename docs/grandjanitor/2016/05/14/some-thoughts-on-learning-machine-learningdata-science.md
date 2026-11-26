---
title: "Some Thoughts on Learning Machine Learning/Data Science"
date: 2016-05-14
tags: ["deep learning", "Machine Learning"]
---

# Some Thoughts on Learning Machine Learning/Data Science

I have been refreshing myself on various aspects of machine learning and data science. For the most part it has been a very nice experience. What I like most is that I finally able to grok many machine learning jargons people talk about. It gave me a lot of trouble even as merely a practitioner of machine learning. Because most people just assume you have some understanding of what they mean.

Here is a little secret: all these jargons can be very shallow to very deep. For instance, "lasso" just mean setting the regularization terms with exponent 1. I always think it's just people don't want to say the mouthful: "Set the regularization term to 1", so they come up with lasso.

Then there is bias-variance trade off. Now here is a concept which is very hard to explain well. What opens my mind is what Andrew Ng said in his Coursera lecture, "just forget the term bias and variance". Then he moves on to talk about over and under-fitting. That's a much easier to understand concept. And then he lead you to think. In the case, when a model underfits, we have an estimator that has "huge bias", and when the model overfit, the estimator would allow too much "variance". Now that's a much easier way to understand. Over and under-fitting can be visualized. Anyone who understands the polynomial regression would understand what overfitting is. That easily leads you to have a eureka moment: "Oh, complex models can easily overfit!" That's actually the key of understanding the whole phenomenon.

Not only people are getting better to explain different concepts. Several important ideas are enunciated better. e.g. reproducibility is huge, and it should be huge in machine learning as well. Yet even now you see junior scientists in entry level ignore all important measures to make sure their work reproducible. That's a pity. In speech recognition, e.g. I remember there was a dark time where training a broadcast news model was so difficult, despite the fact that we know people have done it before. How much time people waste to repeat other peoples' work?

Nowadays, perhaps I would just younger scientists to take the John Hopkins' "Reproducible Research". No kidding. Pay $49 to finish that class.

Anyway, that's my rambling for today. Before I go, I have been actively engaged in the [Facebook's Deep Learning](https://www.facebook.com/groups/DeepNetGroup/) group. It turns out many of the forum uses love to hear more about how to learn deep learning. Perhaps I will write up more in the future.

Arthur
