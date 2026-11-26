---
title: "Review of Ng's deeplearning.ai Course 1: Neural Networks and Deep Learning"
date: 2017-10-14
categories: ["backpropagation", "deep learning", "deep neural network", "Machine Learning"]
tags: ["deep learning", "Machine Learning"]
---

# Review of Ng's deeplearning.ai Course 1: Neural Networks and Deep Learning

*[image not recovered: agence-producteurs-locaux-damien-kuhn-97746.jpg]*

Credit:: Damien Kühn CC

(See my reviews on [Course 2](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/) and [Course 3](/grandjanitor/2017/11/25/review-of-ngs-deeplearning-ai-course-3-structuring-machine-learning-projects/).)

As you all know, Prof. Ng has a new specialization on Deep Learning. I wrote about the course extensively yet informally, which include two "Quick Impressions" [before](/grandjanitor/2017/08/09/quick-impression-on-deeplearning-ai/) and [after](/grandjanitor/2017/08/21/quick-impression-on-deeplearning-ai-after-finishing-coursework/) I finished Course 1 to 3 of the specialization. I also wrote three posts just on Heroes on Deep Learning including [Prof. Geoffrey Hinton](/grandjanitor/2017/08/13/quick-impression-on-deeplearning-ai-heroes-of-deep-learning-geoffrey-hinton/), [Prof. Yoshua Bengio ](/grandjanitor/2017/08/27/quick-impression-on-deeplearning-ais-heroes-of-deep-learning-with-prof-yoshua-bengio/)and [Prof. Pieter Abbeel and Dr. Yuanqing Lin](/grandjanitor/2017/09/11/my-third-quick-impression-on-hodl-interviews-with-pieter-abbeel-and-yuanqing-lin/) . And Waikit and I started a study group, [Coursera deeplearning.ai](https://www.facebook.com/groups/DeepLearningAISpecialization/) (C. dl-ai), focused on just the specialization. This is my full review of Course 1 after finish watching all the videos. I will give a description on what the course is about, and why you want to take it. There are already few very good reviews (from [Arvind](https://medium.com/towards-data-science/thoughts-after-taking-the-deeplearning-ai-courses-8568f132153) and [Gautam](https://medium.com/@gautam.karmakar/my-experience-with-new-deep-learning-course-from-deeplearning-ai-coursera-585c6997401f)). I will write based on my experience as the admin of [AIDL](https://www.facebook.com/groups/DeepNetGroup/), as well as a deep learning learner.

# The Most Frequently Asked Question in AIDL

If you don't know, [AIDL](https://www.facebook.com/groups/DeepNetGroup/) is one of most active Facebook group on the matter of A.I. and deep learning. So what is the most frequently asked question (FAQ) in our group then? Well, nothing fancy:

> How do I start deep learning?

In fact, we got asked that question daily and I have personally answered that question for more than 500 times. Eventually I decided to create an FAQ - which basically points back to "[My Top-5 List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)" which gives a list of resources for beginners.

# The Second Most Important Class

That brings us to the question what should be the most important class to take? Oh well, for 90% of the learners these days, I would first recommend Andrew Ng's "[Machine Learning](https://www.coursera.org/learn/machine-learning)", which is both good for beginners or more experienced practitioners (like me). Lucky for me, [I took it around 2 years ago](/grandjanitor/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/) and got benefited from the class since then.

But what's next? What would be a good second class? That's always the question on my mind. Karpathy cs231n comes to mind, or may be Socher's cs224[dn] is another choice. But they are too specialized in the subfields. E.g. If you view them from the study of general deep learning, the material in both classes on model architecture are incomplete.

Or you can think of general class such as [Hinton's NNML](/grandjanitor/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/). But the class confuses even PhD friends I know. Indeed, asking beginners to learn restricted Boltzmann machine is just too much. Same can be said for [Koller's PGM](https://www.coursera.org/specializations/probabilistic-graphical-models). Hinton's and Koller's class, to be frank, are quite advanced. It's better to take them if you already know the basics of ML.

That narrows us to several choices which you might already consider: first is fast.ai by Jeremy Howard, second is deep learning specialization from Udacity. But in my view, those class also seems to miss something essential - e.g., fast.ai adopts a *top-down approach.* But that's not how I learn. I alway love to approach a technical subject from ground up. e.g. If I want to study string search, I would want to rewrite some classic algorithms such as [KMP](https://en.wikipedia.org/wiki/Knuth%E2%80%93Morris%E2%80%93Pratt_algorithm). And for deep learning, I always think you should start with a good implementation of back-propagation.

That's why for a long time, [Top-5 List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/) picked cs231n and cs224d as the second and third class. They are the best I can think of after researching ~20 DL classes. Of course, deeplearning.ai changes my belief that either cs231n and cs224d should be the best second class.

# Learning Deep Learning by Program Verification

So what so special about deeplearning.ai? Just like Andrew's Machine Learning class, deeplearning.ai follows an approach what I would call *program verification**.* What that means is that instead of guessing whether your algorithm is right just by staring at the code, deeplearning.ai gives you an opportunity to come up with an implementation your own provided that you match with its official one.

Why is it important then? First off, let me say that not everyone believes this is right approach. e.g. Back when I started, many well-intentioned senior scientists told me that such a matching approach is not really good experimentally. Because supposed your experiment have randomness, you should simply run your experiment N times, and calculate the variance. Matching would remove this experimental aspect of your work.

So I certainly understand the point of what the scientists said. But then, in practice, it was a huge pain in the neck to *verify* if you program is correct. That's why in most of my work I adopt the matching approach. You need to learn a lot about numerical properties of algorithm this way. But once you follow this approach, you will also get an ML tasks done efficiently.

But can you learn in another way? Nope, you got to have some practical experience in implementation. Many people would advocate learning by just reading paper, or just by running pre-prepared programs. I always think that's missing the point - you would lose a lot of understanding if you skip an implementation.

# What do you Learn in Course 1?

For the most part, implementing feed-forward (FF) algorithm and back-propagation (BP) algorithm *from scratch*. Since for most of us, we are just using frameworks such as TF or Keras, such implementation from scratch experience is invaluable. The nice thing about the class is that the mathematical formulation of BP is fined tuned such that it is suitable for implementing on Python numpy, the course designated language.

# Wow, Implementing Back Propagation from scratch? Wouldn't it be very difficult?

Not really, in fact, many members finish the class in less than a week. So the key here: when many of us calling it a *from-scratch* implementation, in fact it is highly guided. All the tough matrix differentiation is done for you. There are also strong hints on what numpy functions you should use. At least for me, homework is very simple. (Also see Footnote [1])

# Do you need to take Ng's "Machine Learning" before you take this class?

That's preferable but not mandatory. Although without knowing the more classical view of ML, you won't be able to understand some of the ideas in the class. e.g. the difference how bias and variance are viewed. In general, all good-old machine learning (GOML) techniques are still used in practice. Learning it up doesn't seem to have any downsides.

You may also notice that both "Machine Learning" and deeplearning.ai covers neural network. So will the material duplicated? Not really. deeplearning.ai would guide you through implementation of multi-layer of deep neural networks, IMO which requires a more careful and consistent formulation than a simple network with one hidden layer. So doing both won't hurt and in fact it's likely that you will have to implement a certain method multiple times in your life anyway. 

# Wouldn't this class be too Simple for Me?

So another question you might ask. If the class is so simple, does it even make sense to take it? The answer is a resounding yes. I am quite experienced in deep learning (~4 years by now) and I learn machine learning since college. I still found the course very useful, because it offers many useful insights which only industry expert knows. And of course, when a luminary such as Andrew speaks, you do want to listen.

In my case, I also want to take the course so that I can write reviews about it and my colleagues in [Voci](http://www.vocitec.com/) can ask me questions. But with that in mind, I still learn several things new through listening to Andrew.

# Conclusion

That's what I have so far. Follow us on Facebook [AIDL](https://www.facebook.com/groups/DeepNetGroup/), I will post reviews of the later courses in the future.

Arthur

[1] So what is a true *from-scratch*  implementation? Perhaps you write everything from C and even the matrix manipulation part?

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me (Arthur) at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci). 

History: Nov 29, 2017: revised the text once. Mostly rewriting the clunky parts. Oct 16, 2017: fixed typoes and misc. changes. Oct 14, 2017: first published

---

## Comments

**SEIBOLD Heinz Peter** (2018-01-31):

I also would recommend to start with Andrew Ng's "Machine Learning". Matlab/Octace codes match much better with the material of the lectures than Python. Particularly the implemantation of vectorized solutions.

