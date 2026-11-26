---
title: "AIDL Weekly Issue #61 - Project Maven"
date: 2019-07-25
---

# AIDL Weekly Issue #61 - Project Maven

# [Issue 61 *June 4th 2018* ](http://aidl.io/issues/61/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week, we take a closer look at Google's involvement in project Maven, and how it ends abruptly after complaints from Google's employees.

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 145,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## News

### [Google and Project Maven](https://www.nytimes.com/2018/05/30/technology/google-project-maven-pentagon.html)

This is one of the two pieces we include on [Project Maven](https://www.defense.gov/News/Article/Article/1254719/project-maven-to-deploy-computer-algorithms-to-war-zone-by-years-end/), which is mostly the background story of why Google is involved in defense projects in the first place, and why it could be a problem from its companies' culture perspective.

We encourage you to read the whole piece, and only give some perspectives about the AI industry. And in some sense, guide you to understand the root of the internal conflicts of Google.

As you might know, defense projects are usually bid and picked up by big defense contractors such as Lookheed, Raytheon and Boeing. So for a web search company such as Google to join is quite strange. Of course, money is playing a role - Google's web search business model is seeing its limitation and it's hard to guarantee future growth.

But then, the more important part is that Google has been advancing on AI in a faster pace. Way before the time of deep learning, there was a saying that the largest database only exists in either Google or government agencies. So AI is not just an interesting research project for Google, her vast amount of data and brain power also created a tremendous opportunity for her to replace traditional big houses such as Lookheed. Obviously smart employees see that, that's why Google now has a Head of Defense and Intelligence Sales, and in a way, it will likely be a solid revenue source for Google in the future.

This shouldn't surprise you. U.S. defense has advocated research in automatic speech recognition and machine translation. In a way, you may even see is natural to see Google would have to make a decision of creating AI-based weapons once they decide to work on AI.

[nytimes.com](https://www.nytimes.com/2018/05/30/technology/google-project-maven-pentagon.html)

---

### [No More Google in Project Maven](https://gizmodo.com/google-plans-not-to-renew-its-contract-for-project-mave-1826488620)

Worth mentioning: While the project is gone from Google, the department of Defense and Intelligence Sales still exists within Google.

[gizmodo.com](https://gizmodo.com/google-plans-not-to-renew-its-contract-for-project-mave-1826488620)

## Blog Posts

### [AI Winter Is Well On Its Way By Filip Piekniewski](http://blog.piekniewski.info/2018/05/28/ai-winter-is-well-on-its-way/)

This is widely circulated post by Dr. Filip Piekniewski (picked up by techmeme) on the hype of deep learning. Dr. Piekniewski looked at several evidence that the current AI hype is slowing down, that includes the recent SDC crash as well as lack of interesting research last year.

He praised long-time deep learning critics: 

> I respect Gary a lot, he behaves like a real scientist should, while most so called "deep learning stars" just behave like cheap celebrities.

We like Piekniewski's criticism on deep learning. Although we reserve judgement on whether AI winter is coming. As he mentioned in the conclusion, predicting the next AI winter is like predicting marketing crash - by itself it's an uncertain business.

And to mention another point: there are actually rather vibrant activities in machine learning and artificial intelligence in mid-2000s before the advent of deep learning. We doubt it would stop just because of one event or two. But of course, ours is also just a prediction.

[piekniewski.info](http://blog.piekniewski.info/2018/05/28/ai-winter-is-well-on-its-way/)

## Open Source

### [BDD100K: A Large-scale Diverse Driving Video Database](http://bair.berkeley.edu/blog/2018/05/30/bdd/)

Perhaps the largest open source computer vision database, it spot 120Million images and suitable for road object detection and lane marking. You can imagine it can be very useful for researches on SDC.

[berkeley.edu](http://bair.berkeley.edu/blog/2018/05/30/bdd/)

## Member's Question

### I realized ML is just Statistics, should I feel demotivated?

[Question](https://www.facebook.com/groups/DeepNetGroup/permalink/623724638020422/): *Anyone had the feeling where you feel very motivated and eager to learn machine learning, and once you actually start, you realize it's just stats which is something you really don't like, and become completely demotivated?*

Answer: (By Arthur) There are two parts of your frustrations. First, it's that you equate machine learning and statistics. Second it is you feel that statistics is boring. So let's address the second part first. Then I will come back to the first part.

Is statistics boring? I guess many people who learn statistics usually learn Math first. If that's your route, then perhaps one of the reasons why statistics is boring is that it is empirical and deal with imperfect phenomenon of the world. So unlike Euclidean geometry, or solving quadratic or cubic, you can't quite come up with an exact solution.

To many people's dissatisfaction though, the world is better to be described to be uncertain, rather than certain. Unfortunately, only statistics can teach us more in the realm of uncertainty. So statistics is actually a rescue, and I personally feel grateful for the subject.

Can statistics be fun? You ask. It all depends on how you look at it. e.g. It took me a while to find a good proof of how a full covariance matrix can be estimated through maximum likelihood. In particular, in matrix form, the math is quite interesting. I end-up bought a book by Abadir and Magnus called "Matrix Algebra" and browse it from time to time. I am pretty sure it is boring to some, but it's a lot of fun to me. Btw, Matrix Algebra can be quite mathematical too. But you may say it is more technical type of Math.

My conclusion of the second part is: are you sure you see everything in statistics and machine learning? There are many deep topics in both subjects. But then you might miss nuance in your first glance. So that's that. Of course, your frustration might come from your personal philosophy. Perhaps you don't like uncertainty? Perhaps you don't like the time-consuming process of collecting data? No one can blame you for that. You just have to be honest to yourself.

Let’s go back to the first part on whether machine learning is just statistics. And this is slightly controversial. Let me just quote one prominent person. Say if you ask Prof. Nil Nilsson, he once said machine learning just the subject of "machine to learn". But statistics is clearly more focused on the data and its observation. So if the fancy image of an intelligent robot is doing things was what attracts you, yeah, ML is the subject to learn. It's just that modern theory of ML has found that statistics is very important.

So why is that the case? Oh well, it's not like people love to be statistical, it has to do with nature is better described by uncertain rules. So say speech recognition? People would love to create several rules of phonetics and do speech recognition. In fact they were tried by PhD students in 60s. So in 70s, people start to realize that's not the way to go. Ha tada, here comes HMM. Boring it is. But it is the basis of many previous generation ASR before seq2seq NN models. In fact, there are still many HMM-based system.

So, to summarize, if you are disappointed by ML. Ask whether reality is better described by certainty or uncertainty. It will help you to have a closure.

Artificial Intelligence and Deep Learning Weekly

## Paper/Thesis Review

### [Do Better ImageNet Models Transfer Better?](https://arxiv.org/abs/1805.08974)

This is a paper from Google investigating the limitation of transfer learning. Several findings catch our eyes. For example, the researchers find that better the model, generally transfer learning would have better performance. But then resnet consistently gives better performance than better models. These are intriguing results, and have practical values when you do image classification.

[arxiv.org](https://arxiv.org/abs/1805.08974)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 145,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
