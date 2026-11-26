---
title: "AIDL Weekly #23 - Elon vs Musk"
date: 2019-06-22
---

# AIDL Weekly #23 - Elon vs Musk

# [Issue 23 *July 28th 2017* ](http://aidl.io/issues/23/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we look at the argument between Elon Musk and Mark Zuckerberg. Which one of the two billionaires is more right? (Or less wrong?) We will find out. 

We also heard some disturbing news from popular outlets again - this time, Facebook kills its A.I agent s which create its own language! Is it true? In our fact-checking section, we will look at the claim closely.

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Elon vs Mark](https://techcrunch.com/2017/07/25/elon-musk-mark-zuckerberg-artificial-intelligence/)

Ah...... Elon and Mark. One is the [real-life Ironman](http://www.telegraph.co.uk/technology/0/elon-musk-tech-billionaire-spacex-cowboy-real-life-iron-man/). One wants to build a [J. A. R. V. I. S.](http://nerdist.com/mark-zuckerberg-wants-to-build-a-j-a-r-v-i-s-iron-man/). Isn't it a surprise that they argue? But it's happening! 

If there is anything like trash talk in A.I., Elon Musk and Mark Zuckerberg are doing it. How should we view their fight?

Besides the obvious entertainment value of the fight. (You know this piece has [~370 likes at AIDL](https://www.facebook.com/groups/DeepNetGroup/permalink/476577279401826/)?) It's hard to dismiss the danger of artificial intelligence. But we want to qualify we meant by "danger". For example, immediate danger of A.I. based weapon is real. Some members quickly point us to this [piece](https://www.rt.com/news/395375-kalashnikov-automated-neural-network-gun/) on automatic combat module. And you bet that all your familiar deep-learning technologies are all being used for military purposes. For example, speech recognition can be easily used as a means to automatically collect data from phone messages.

It makes sense to ask whether this kind of existing A.I. applications are causing danger of humanity. But this is not the A.I. what Elon Musk is cautioning people! The A.I. he was talking about is more what Prof. [Nick Bostrom](http://www.nickbostrom.com/) called [Superintelligence](https://www.amazon.com/Superintelligence-Dangers-Strategies-Nick-Bostrom/dp/0198739834/ref=sr_1_1?ie=UTF8&qid=1501205762&sr=8-1&keywords=superintelligence), which is more a God-like being which has intelligence human cannot fathom. In this tenet of thinking, or shall we call "alarmist", A.I. is a super scary subject. For example, just right now, alarmist could tell you "Well, a super-intelligent A.I. must already exist, because the best strategy to hurt human being is to hide itself". If you say, "How about the current AI development just doesn't seem to be this scary?", then Alarmists would retort that there might quote prominent statisticians [I. J. Good](https://en.wikipedia.org/wiki/I._J._Good)'s concept of "intelligence explosion", claiming you just can't predict how intelligence of machine would develop.

So how should we view the matter? So far, it doesn't seem like there are any real proof on the alarmists' side of thinking. More importantly, the theory of alarmists such as Musk's doesn't allow any one of us to experiment and *falsify* [1]. Is it really a good scientific theory? We doubt. On the other hand, people who criticize Musk are usually practitioners, actual ML researchers, and those who actually build an AI system before. They support their arguments with facts and experience. We found their views make more sense.

That's why, between Elon and Mark, we chose Mark. We are not alone, apparently [Prof. Andrew Ng seems to agree with us](https://www.facebook.com/groups/DeepNetGroup/search/?query=Andrew%20Ng). He suggested when we talk about the danger of A.I., rather than talking about Musk's killer robots, the core issues should be poverty, inequality and job loss. We cannot agree more.

[1] We use the term "falsify" similar to Thomas Kuhn's ["The Structure of Scientific Revolution"](https://en.wikipedia.org/wiki/The_Structure_of_Scientific_Revolutions).

[techcrunch.com](https://techcrunch.com/2017/07/25/elon-musk-mark-zuckerberg-artificial-intelligence/)

---

### [The Origin of The Imagenet Database](https://qz.com/1034972/the-data-that-changed-the-direction-of-ai-research-and-possibly-the-world/)

We seem to forget that modern deep learning is indebted to Stanford Professor, Fei-Fei Li who propose, design and collect the Imagenet database. 

As for those who protest and say "Imagenet is just a database! The fascinating part is XNet, YNet and ZNet!"[1] Remember the adage "90% of data science is data preparation"? In fact, as the Quartz story being told, Prof. Li's journey of creating a 1-million annotated image database is yet another technical breakthrough in the field. e.g. If not because Amazon mechanical turk was there, it was close to impossible for her to organize so many workers to do such annotation.

So check out the story of the origin of Imagenet. Perhaps more importantly, check out the story of Prof. Fei-Fei Li, the mother of Imagenet.

[1] Make-up neural networks names, but [ZFNet](https://arxiv.org/abs/1311.2901) is real.

[qz.com](https://qz.com/1034972/the-data-that-changed-the-direction-of-ai-research-and-possibly-the-world/)

## Factchecking

### Fact-Checking : "Facebook kills AI that invented its own language......"

You know that news can develop, but do you know faked news can also "develop"? Interesting huh? 

It happens. For example, in [Issue 19](http://aidl.io/issues/19#start), we fact-checked if the rumor "Facebook AI Created Its Own Unique Language" is true. We rate it **False**. And to recap, FAIR researchers were more evolving two agents which was first trained in *English*. So the resulting language is again *English*. And if you really think that AI is inventing its own language, then you are equating colloquialism as a language.

That's what we said in Issue 19, what happened since then? Oh well, faked news always have legs by itself. Some good people (perhaps a bit gullible) from popular outlet, once again think that FB created an AI which created its language. This time imagination make the good people always think that FB "kills" the A.I.

So this is a simple one: we rate this piece **false**, as there was no AI creating a language, thus saying FB "kills" such AI is non-sensical.

(Follow Up at 20170729: We are contacting several researchers from Facebook to understand the matter better. We will keep you all posted on the latest".)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [37 Reasons Why Your Neural Network Doesn't Work](https://blog.slavv.com/37-reasons-why-your-neural-network-is-not-working-4020854bd607)

If you first start out in deep learning, for the most part you just need to download a script and run it. But when you start to use a new data set, it's very likely you would hit a non-working training. Why is it the case? In 37 points, Slav Ivanov shares his own experience on debugging neural networks. I (Arthur) like his analysis because it's clear he has extensive experience in debugging. His lessons also contain gems extracted from classes such as cs231n. 

[slavv.com](https://blog.slavv.com/37-reasons-why-your-neural-network-is-not-working-4020854bd607)

---

### [Gluon - A New Deep Learning Framework](https://mli.github.io/cvpr17/)

There are many deep learning frameworks in the world. While you are reading this blurb, perhaps someone is writing a new one. So why do we bring up Gluon then? 

To understand the significance of Gluon, it's better to understand the difference between what its author, *imperative* versus *symbolic* programming in deep learning frameworks. These terms are used by Gluon's author Mu Li, who is a researcher from AWS Deep Learning.

The term imperative come straightly from the term imperative programming, which means that your program statements explicitly changes the state of the program. Whereas, a symbolic programming language may hide these detail from you, but it gives with a reward. e.g. it might optimize your program better. So one consequence is if you want to use debugger on your program, it's possible to do so in an imperative language (Think gdb for C.), but not in a symbolic language.

Now this is a very important distinction in deep learning frameworks. For example, Tensorflow is not an imperative framework. So working on TF would mean that you can't use a debugger easily Whereas, frameworks such as PyTorch, on the other hand, is imperative. That's way they are more fun and easier to work with, but the speed is slower.

What Gluon promises is that you can *mix up* the two types of programming together. The basic philosophy is that when you develop your framework, you can use imperative language, whereas deployment would based on a symbolic one. The mechanism is based on what Li called *hybridize* and it's fairly flexible objects declare from imperative and symbolic programming togethers.

I don't want to spoil too much here for you, but Gluon does has many interesting idea. If you are interested, check out Li's [slides](https://mli.github.io/cvpr17/gluon_part1.pdf) and other information from the page.

[github.io](https://mli.github.io/cvpr17/)

---

### [Deep Learning for NLP Best Practices](http://ruder.io/deep-learning-nlp-best-practices/index.html)

[Sebastian Ruder](http://ruder.io/#open) wrote some of the best tutorials for beginners. Yet "Deep Learning for NLP Best Practices" is not only just for beginner, you can learn a lot by going through some of his advices. Just take a look of "LSTM tricks". There are discussion on training the initial states (by Hinton) and use gradient clipping (as in Mikolov's RNNLM). Reading it feels like I am showered with gifts in Christmas. 

[ruder.io](http://ruder.io/deep-learning-nlp-best-practices/index.html)

---

### [Does Neuroscience has Anything to Offer AI?](https://neuroecology.wordpress.com/2017/07/24/monday-open-question-does-neuroscience-have-anything-to-offer-ai/)

This piece, written by Adam J. Calhoun, commented on Davis Hassabis' article published last week (check out issue 22). His view on why AI and Neuroscience are separated is quite interesting: He stated that AI is more a field to get work done, yet Neuroscience is more a field to understand why. That certainly describe the mainstream thinking of both fields quite well. 

He also discuss how modern DL architecture (his example? Densenet) starts to look alike of human brain -cortex (his example? human sensory system). All-in-all, it's an article you want to read if you care about either AI or neuroscience.

[wordpress.com](https://neuroecology.wordpress.com/2017/07/24/monday-open-question-does-neuroscience-have-anything-to-offer-ai/)

## Video

### [AIDL Office Hour Episode 9: Interview with FloydHub CEO Sai Prashanth Soundararaj](https://www.youtube.com/watch?v=xaL6N92Wugo)

We are happy to talk with FloydHub's CEO [Sai Prashanth Soundarara](https://www.linkedin.com/in/saiprashanths/). Before we talk with Sai, we learned from the AIDL that [FloydHub](https://www.floydhub.com/) was the choice solution if you want to run deep learning on the cloud. But why? This video could probably give you a lot of insights. In the video, Sai guides us through on why FloydHub's solution is different from say using an AWS instance. As well as how FloydHub resolve issues such as installation issues such as python library dependencies. 

[youtube.com](https://www.youtube.com/watch?v=xaL6N92Wugo)
