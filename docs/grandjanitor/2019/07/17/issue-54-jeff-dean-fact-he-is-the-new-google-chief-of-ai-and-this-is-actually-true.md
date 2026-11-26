---
title: "Issue 54 - Jeff Dean Fact: He is the new Google Chief of AI, and this is actually true!"
date: 2019-07-17
---

# Issue 54 - Jeff Dean Fact: He is the new Google Chief of AI, and this is actually true!

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 54 *April 6th 2018* ](http://aidl.io/issues/54/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

In a major shuffle of talents, Apple hired Google AI's chief, John Giannandrea, and Jeff Dean became the new AI Chief of Google. We cover both pieces in our News section. 

We also look deeper into Google's MobileNetV2 and summarized its various components.

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

This newsletter is a labor of love from us. All publishing costs and operating expenses are paid out of our pockets. If you like what we do, you can help defray our costs by sending a donation via [link](http://paypal.me/aidlio/9). For crypto enthusiasts, you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: original_ratio_extra_large_79167f46-5077-4c34-8813-519971231583.png]*](http://www.comet.ml/?ref=aidl) 

### [Comet.ml - Machine Learning Experimentation Management](http://www.comet.ml/?ref=aidl)

Comet.ml allows tracking of machine learning experiments with an emphasis on collaboration and knowledge sharing. It allows you to keep your current workflow and report your result from any machine - whether it’s your laptop or a GPU cluster. It will automatically track your hyperparameters, metrics, code, model definition and allows you to easily compare and analyze models. 

Just add a single line of code to your training script: 

> experiment = comet_ml.Experiment(api_key="YOUR_API_KEY")

Comet is completely **free** for open source projects. **We also provide 100% free unlimited access for students and academics.** [Click here to sign up!](http://www.comet.ml/?ref=aidl)

[comet.ml](http://www.comet.ml/?ref=aidl)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Apple hires ex-Google AI Chief](https://www.nytimes.com/2018/04/03/business/apple-hires-googles-ai-chief.html)

Apple's hiring John Giannandrea, the AI Chief of Google, is an important move. It shows Apple's determination to be a major presence in AI - During John Gianndrea's tenure, AI has been gaining presence inside Google. From what we see, this is big win for Apple. 

[nytimes.com](https://www.nytimes.com/2018/04/03/business/apple-hires-googles-ai-chief.html)

---

### [Jeff Dean is the new AI Chief](https://www.theverge.com/2018/4/3/17191944/google-ai-head-jeff-dean-reshuffle-john-giannandrea)

As John Giannandrea is gone, who would be the new AI Chief in Google? You guess it right. Jeff Dean! 

No doubt Dr. Dean has a lot of achievements in AI - He found the Google Brain team, involved in developing the currently most popular toolkit, Tensorflow. So he being the Google Chief makes a lot of sense.

Of course, talking about Jeff Dean, we got to bring up one of [Jeff Dean facts](https://www.quora.com/What-are-all-the-Jeff-Dean-facts), right? Oh well, from what we heard: *Jeff Dean doesn't exist, he's actually an advanced AI created by Jeff Dean.*

[theverge.com](https://www.theverge.com/2018/4/3/17191944/google-ai-head-jeff-dean-reshuffle-john-giannandrea)

---

### Deals

- [Scotty Lab get $6M from Gradient](https://www.bloomberg.com/news/articles/2018-03-28/google-backs-startup-working-on-remote-controlled-driverless-cars)
- [DeepScale $15M Series A](http://techstartups.com/2018/04/03/artificial-intelligence-startup-deepscale-raises-15-million-advance-automated-vehicle-perception/)
- [6 River Systems $25M Series B](https://www.xconomy.com/boston/2018/04/04/with-25m-in-tow-6-river-systems-aims-to-advance-warehouse-robotics/)
- [Comet.ml $2.5M Seed Round](https://techcrunch.com/2018/04/05/cometml-wants-to-do-for-machine-learning-what-github-did-for-code/) - Also our sponsor of this issue. Congrat!
- [Suplari $10.3M Series A](https://www.geekwire.com/2018/suplari-raises-10-3m-reveals-ai-platform-identifies-cost-savings-procurement-process/)

Artificial Intelligence and Deep Learning Weekly 

---

### [Macron on Frances AI Strategy](https://www.wired.com/story/emmanuel-macron-talks-to-wired-about-frances-ai-strategy)

"The key driver should not only be technological progress, but human progress." Macron said. It's interesting to learn from a world leader on how AI should be adopted in the national level. The French government is planning to spend ~$1.85 billion on developing A.I.. 

[wired.com](https://www.wired.com/story/emmanuel-macron-talks-to-wired-about-frances-ai-strategy)

## Blog Posts

### [MobileNet V2](https://research.googleblog.com/2018/04/mobilenetv2-next-generation-of-on.html)

Model compression in general, is seen as speed-up or memory reduction technique. And unlike research which optimizes performance, some techniques floating around are ad-hoc. This makes Google's MobileNet particularly interesting because they come up with all kind of non-trivial methods to optimize speed/space. 

Reading the [original paper](https://arxiv.org/pdf/1801.04381.pdf), there are three major ingredients in Mobilenet V2: 
- *Depthwise Separable Convolutions*: this actually the major innovation in V1. The idea is that convolution layer can be factored into two convolutions. This was how V1 was able to reduce some models for a factor of 6-8.
- *Linear bottleneck layer*: this is new, the team found that they could insert linear bottleneck layer to summarize information of a convolution layer. There is an interesting discussion on Manifold Hypothesis. Yet, the author stated that the theory only provided them an "empirical hint".
- *Inverted Residue*: this is also new, which means that MobileNet V2 uses an architecture which has opposite direction from the usual Resnet. According to the authors, it's motivated by linear bottleneck layer. Looking at Section 5, it's probably because this new architecture gave rise to an efficient implementation.

Overall, MobileNetV2 is impressive and gives further 30% reduction in computation and memory. Sounds like something you want to check out.

[googleblog.com](https://research.googleblog.com/2018/04/mobilenetv2-next-generation-of-on.html)

## Open Source

### [Microsoft Professional Certificate on AI](https://academy.microsoft.com/en-us/professional-program/tracks/artificial-intelligence/)

The new program released by Microsoft, it's certainly interesting in terms of both breadth and depth. In this 10-class course, MS provides a comprehensive coverage of basic machine learning and AI. Each class requires 8-16 hours classwork which we feel is fairly substantial. We think MS' courses may be comparable to Google's earlier release of on-line ["Crash course"](https://developers.google.com/machine-learning/crash-course/?utm_source=google-ai&utm_medium=card-image&utm_campaign=training-hub&utm_content=ml-crash-course). 

[microsoft.com](https://academy.microsoft.com/en-us/professional-program/tracks/artificial-intelligence/)

---

### [Andrew Ng's "Machine Learning Yearning"](http://www.mlyearning.org/)

A free draft copy is available as we told by [Andrew himself](https://twitter.com/AndrewYNg/status/981584286225592321). 

[mlyearning.org](http://www.mlyearning.org/)

## Other News

### [Google Employee's Letter to CEO](https://www.nytimes.com/2018/04/04/technology/google-letter-ceo-pentagon-project.html)

"We believe that Google should not be in the business of war." says the letter. This address to Google's [involvement of a Pentagon's drone project](https://gizmodo.com/google-is-helping-the-pentagon-build-ai-for-drones-1823464533). 

Looking at the [original one-page letter](https://static01.nyt.com/files/2018/technology/googleletter.pdf) Also, "This plan will irreparably damage Google’s brand and its ability to compete for talent." The letter also names couple of defense contractors. Indeed, many U.S. talents head to Google, mainly to avoid involvement with the military. So perhaps it is where the statement comes from.

[nytimes.com](https://www.nytimes.com/2018/04/04/technology/google-letter-ceo-pentagon-project.html)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 125,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760 

Artificial Intelligence and Deep Learning Weekly
