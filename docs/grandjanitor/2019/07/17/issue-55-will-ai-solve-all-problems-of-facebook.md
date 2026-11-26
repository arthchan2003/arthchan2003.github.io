---
title: "Issue 55 - Will AI solve all problems of Facebook?"
date: 2019-07-17
---

# Issue 55 - Will AI solve all problems of Facebook?

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 55 *April 13th 2018* ](http://aidl.io/issues/55/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Our headline this week is Zuckerberg's Senate hearing, we look at the core technical problem Facebook encounters when it comes to fake news/profiles detection. In our Blog section, we cover DeepMind's navigation agent, Skydio R1, as well as how researchers are learning dog's behavior through AI.

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

This newsletter is a labor of love from us. All publishing costs and operating expenses are paid out of our pockets. If you like what we do, you can help defray our costs by sending a donation via [link](http://paypal.me/aidlio/9). For crypto enthusiasts, you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: original_ratio_extra_large_582f2421-6680-4113-9a0d-ef5c3e953c3f.png]*](http://www.comet.ml/?ref=aidl) 

### [Comet.ml - Machine Learning Experimentation Management](http://www.comet.ml/?ref=aidl)

Comet.ml allows tracking of machine learning experiments with an emphasis on collaboration and knowledge sharing. It allows you to keep your current workflow and report your result from any machine - whether it’s your laptop or a GPU cluster. It will automatically track your hyperparameters, metrics, code, model definition and allows you to easily compare and analyze models. 

Just add a single line of code to your training script: 

> experiment = comet_ml.Experiment(api_key="YOUR_API_KEY")

Comet is completely **free** for open source projects. **We also provide 100% free unlimited access for students and academics.** [Click here to sign up!](http://www.comet.ml/?ref=aidl)

[comet.ml](http://www.comet.ml/?ref=aidl)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Facebook's Issues from the AI Point of View](https://www.washingtonpost.com/news/the-switch/wp/2018/04/11/ai-will-solve-facebooks-most-vexing-problems-mark-zuckerberg-says-just-dont-ask-when-or-how/?noredirect=on&utm_term=.8c1cdafeda9a)

This hasn't been a good month to Facebook, with all the privacy issues. You might have heard of Cambridge Analytics(CA) stolen around [87 millions profiles](https://www.theguardian.com/technology/2018/apr/08/facebook-to-contact-the-87-million-users-affected-by-data-breach) and Facebook's algorithm was spreading [faked news](http://fortune.com/2018/02/13/facebook-fake-news-wired-article/). CA was purportedly using "psychographic data" to affect elections in multiple countries. The hits just keep on coming, with new revelations on CA potentially accessing users' private messages. Zuckerberg finally had to testify in front of the Senate [during the week](https://www.nytimes.com/2018/04/12/technology/mark-zuckerberg-testimony.html).

Politics aside, the root problem is still we just don't have good fake news/fake profile detectors. Many companies are trying to build one, but similar to sentiment analysis 10 years ago, researchers/ML algorithms would be perplexed by: 
1. whether the ground truth exists
2. modeling, especially given that context and background are major factors to decide if a certain news is faked.

It probably takes another deep-learning type of disruption to get us there. Zuckerberg is confident that A.I. will solve Facebook's problem. But he refuses to give an ETA.

[washingtonpost.com](https://www.washingtonpost.com/news/the-switch/wp/2018/04/11/ai-will-solve-facebooks-most-vexing-problems-mark-zuckerberg-says-just-dont-ask-when-or-how/?noredirect=on&utm_term=.8c1cdafeda9a)

---

### Deals

- [SenseTime raised $600M, valued at $3B](https://www.bloomberg.com/news/articles/2018-04-09/sensetime-snags-alibaba-funding-at-a-record-3-billion-valuation) - also allegedly the most valuable AI startup company,
- [Brainosix secured $9.8M](https://www.dicardiology.com/content/brainomix-secures-98m-investment-tackle-strokes-ai) - using AI to detect strokes.
- Not exactly a deal, but [USDF just approved an AI-based diagnostic device](https://www.theverge.com/2018/4/11/17224984/artificial-intelligence-idxdr-fda-eye-disease-diabetic-rethinopathy).

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [Skynet Today](http://www.skynettoday.com/)

A new site we highly recommend. It helps chill the inordinate hypes and sensational news coverage on AI. Some topics have been fact-checked by AIDL in the past, including "AI invented languages".

We also like the cover image with the silly robot.

[skynettoday.com](http://www.skynettoday.com/)

---

### ["A Discussion about Accessibility in AI at Stanford" by Rachel Thomas](http://www.fast.ai/2018/04/10/stanford-salon/)

A very good read on Rachel Thomas' view on the pressing issues of A.I. We like this one the most: 

> There are several problems that are far more urgent than the threat of evil super-intelligence, such as how we are encoding racial and gender biases into algorithms (that are increasingly used to make hiring, firing, healthcare benefits, criminal justice, and other life-impacting decisions) or increasing inequality (and the role that algorithms play in perpetuating & accelerating this).

[fast.ai](http://www.fast.ai/2018/04/10/stanford-salon/)

---

### [DeepMind's Navigating Agent Without Maps](https://deepmind.com/blog/learning-to-navigate-cities-without-a-map/)

This is an interesting work from DeepMind. Conventionally, navigation requires annotated maps which might or might not available. Instead, DeepMind researchers built an agent based on computer vision alone, and reward is based on deep reinforcement learning algorithm.

You can find the original paper [here](https://arxiv.org/pdf/1804.00168.pdf).

[deepmind.com](https://deepmind.com/blog/learning-to-navigate-cities-without-a-map/)

---

### [Skydio R1 Automatic Drone Review](https://www.theverge.com/2018/4/5/17195622/skydio-r1-review-autonomous-drone-ai-autopilot-dji-competitor)

Verge's Nick Statt write a review of the first consumer drone, Skydio R1, he puts R1 into several tests in San Francisco area and subject it to several tests. The one which caught our eyes is R1's capability of capturing the Statt's skating. That requires good image segmentation/image localization implemented within the drone.

[theverge.com](https://www.theverge.com/2018/4/5/17195622/skydio-r1-review-autonomous-drone-ai-autopilot-dji-competitor)

---

### [Who’s a good AI? ](https://techcrunch.com/2018/04/11/whos-a-good-ai-dog-based-data-creates-a-canine-machine-learning-system/)

TechCrunch reported on a system jointly built by University of Washington and Allen Institute for .... dog emulation!

But why? You asked. One way to look at it - emulating animals is a good starting point of artificial general intelligence (AGI). For example, one school of thought of AGI, [AIXI](https://en.wikipedia.org/wiki/AIXI) believes that an AGI problem can be reduced to a reinforcement learning problem. In that line of thought, humans or any creatures are just reinforcement learning agents.

That brings back to our good doggy - why do the researchers choose dogs then? Oh well, if we start from humans, then the number of actions we can take every moment is too large, and we can't expect nowadays machine would be able to learn such a large action space. Dogs action, on the other hand, are less complicated and perhaps more a tractable. Pavlovian dog tricks!

[techcrunch.com](https://techcrunch.com/2018/04/11/whos-a-good-ai-dog-based-data-creates-a-canine-machine-learning-system/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 131,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
