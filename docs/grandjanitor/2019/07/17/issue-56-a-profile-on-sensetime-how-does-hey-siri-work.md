---
title: "Issue 56 - A profile on SenseTime; How does \"Hey Siri\" work?"
date: 2019-07-17
---

# Issue 56 - A profile on SenseTime; How does "Hey Siri" work?

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 56 *April 20th 2018* ](http://aidl.io/issues/56/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We have the profile of SenseTime this week in the News section this week, and we also analyze Apple's personalized "Hey Siri" feature in the Blog section. 

---

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 132,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: original_ratio_extra_large_8dc093d8-7af3-4439-bc5f-4d7cedd6284a.png]*](http://www.comet.ml/?ref=aidl) 

### [Comet.ml - Machine Learning Experimentation Management](http://www.comet.ml/?ref=aidl)

Comet.ml allows tracking of machine learning experiments with an emphasis on collaboration and knowledge sharing. It allows you to keep your current workflow and report your result from any machine - whether it’s your laptop or a GPU cluster. It will automatically track your hyperparameters, metrics, code, model definition and allows you to easily compare and analyze models. 

Just add a single line of code to your training script: 

> experiment = comet_ml.Experiment(api_key="YOUR_API_KEY")

Comet is completely **free** for open source projects. **We also provide 100% free unlimited access for students and academics.** [Click here to sign up!](http://www.comet.ml/?ref=aidl)

[comet.ml](http://www.comet.ml/?ref=aidl)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [A Profile on SenseTime](https://qz.com/1248493/sensetime-the-billion-dollar-alibaba-backed-ai-company-thats-quietly-watching-everyone-in-china/)

On Issue #55, we reported in our Deal section that SenseTime become the biggest AI startup in the planet now. In this article from Quartz, we learn how the company started by a professor from Chinese University in Hong Kong, how their business boom from China's lending industry. 

One sentence should wow you. 

> SenseTime claims to have a training database of over 2 billion images

and as you know, most public database tops at around 10 million images (e.g. Imagenet has ~1.2M images. So we are talking about a factor of 100 difference.

Where does SenseTime get all the data? The Chinese government. SenseTime's story should make us realize that China's advantage on AI is real. Unlike European countries in U.S., China has much lax rules on privacy of data. [A recent survey](http://www.scmp.com/business/companies/article/2135713/increasing-use-artificial-intelligence-stoking-privacy-concerns) shows 76.3% of citizens feel that A.I. would invade their privacy. But this lack of privacy allows data to be shared more easily, which is good for ML/AI development.

[qz.com](https://qz.com/1248493/sensetime-the-billion-dollar-alibaba-backed-ai-company-thats-quietly-watching-everyone-in-china/)

---

### Deals

- [BenevolentAI $115M, now valued at $2B](https://techcrunch.com/2018/04/18/benevolentai-which-uses-ai-to-develop-drugs-and-energy-solutions-nabs-115m-at-2b-valuation/)
- [Eightfold.ai $24M](https://techcrunch.com/2018/04/17/two-facebook-and-google-geniuses-are-combining-search-and-ai-to-transform-hr/)

Artificial Intelligence and Deep Learning Weekly 

---

### [Waymo applies for SDC testing in California](https://www.sfchronicle.com/business/article/Exclusive-Waymo-appplies-for-no-driver-testing-12832425.php)

According to SF Chronicle, it will start testing around the Waymo's campus first. 

[sfchronicle.com](https://www.sfchronicle.com/business/article/Exclusive-Waymo-appplies-for-no-driver-testing-12832425.php)

## Blog Posts

### [How to Build an Image Database Quickly](https://www.pyimagesearch.com/2018/04/09/how-to-quickly-build-a-deep-learning-image-dataset/)

We're always a big fan of Joey Adrian Rosebrock. Here is another one of his practical and useful articles, which concern how to create an image database. 

[pyimagesearch.com](https://www.pyimagesearch.com/2018/04/09/how-to-quickly-build-a-deep-learning-image-dataset/)

---

### [Update Google DIY Toolkits](https://9to5google.com/2018/04/16/google-aiy-projects-target/)

The very popular Google Vision and Voice Toolkit is now getting an update. It's mostly and update on [hardwares](https://developers.googleblog.com/2018/04/aiy-projects-updated-kits-for-2018.html), and it's now available in Target. 

[9to5google.com](https://9to5google.com/2018/04/16/google-aiy-projects-target/)

---

### [How does "Hey Siri" work?](https://machinelearning.apple.com/2018/04/16/personalized-hey-siri.html)

Apple ML Blog doesn't disappoint, it gives an expose on how personalized "Hey Siri" works, which includes the architecture of the system (LSTM) and the use of curriculum learning. 

Just to be clear here "personalized" means the system would only adapt to the user's speech. Some may interpret it as you can use *any* keywords, but that's normally not the case for keyword wakeup system. If it is up to users to choose, they might come up overly-short or easy to confuse words.

In fact, here is one sentence which caught our eyes: 

> The phrase “Hey Siri” was originally chosen to be as natural as possible;

Why? A lot of times when you build a keyword wakeup system, the designers want to choose a keyword which is complicated and difficult to be confused. Yet, Apple's engineers choose to go against this rule, they rather follow what users like instead. This gives them a good product feature, but keep them busy to resolve bigger issues such as false alarm : As the article argued, when a user used a natural phase "Hey Siri", other users would likely to use the same phrase as well.

Respect to the Apple team. Notice that personalized wakeup keyword is quite unique to Siri, we don't see similar features in products such as Alexa. Also the whole speaker ID and keyword wakeup process is done on device. It makes it extra difficult to create a good system.

[apple.com](https://machinelearning.apple.com/2018/04/16/personalized-hey-siri.html)

## Member's Question

### Maximum Number of Classes

Question: What's the maximum number of classes a classification algorithm can support ?? 

Answer: (By Arthur) If the objects themselves are not confusing, the answer is theoretically infinite, provided that you also have the right amount of training data for each class.

But if you want to differentiate between two objects but they are both apples, and there is no feature which you can differentiate them. Then the answer is you algorithm will only have 50% chance to come up with the right answer. This sounds funny, but it happens a lot in speech recognition where two words can have the same pronunciations.

Artificial Intelligence and Deep Learning Weekly

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 132,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760 

Artificial Intelligence and Deep Learning Weekly
