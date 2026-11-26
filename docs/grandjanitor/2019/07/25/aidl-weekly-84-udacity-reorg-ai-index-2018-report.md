---
title: "AIDL Weekly #84 - Udacity Reorg, AI Index 2018 Report"
date: 2019-07-25
---

# AIDL Weekly #84 - Udacity Reorg, AI Index 2018 Report

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 84 *December 17th 2018* ](http://aidl.io/issues/84/index.html#start)

## Editorial

### Thoughts From Your Curators

This week we link you to the latest AI Index report, discuss the impact of reorganization of Udacity and analyze a blog post from OpenAI.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

---

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 186,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## News

### Pulse of AI Last Week

- [Megvii $500M](https://www.reuters.com/article/us-megvii-fundraising/chinas-ai-start-up-megvii-raising-500-million-at-3-5-billion-valuation-sources-idUSKBN1O90AV)
- [FortressIQ $12M](https://techcrunch.com/2018/12/04/fortressiq-raises-12m-to-bring-new-ai-twist-to-process-automation/)
- [Optibus $40M](https://venturebeat.com/2018/12/12/optibus-raises-40-million-for-ai-that-optimizes-bus-routes/)
- [Softbank is selling Nvidia's stakes](https://www.bloomberg.com/news/articles/2018-12-11/softbank-is-said-to-plan-sale-of-stake-in-nvidia-next-year)

Artificial Intelligence and Deep Learning Weekly

---

### [Udacity Reorg](https://xconomy.com/san-francisco/2018/12/13/udacity-achieves-50000-nanodegree-grads-amid-company-reorganization/)

When you think about it, democratization of AI also coincided with democratization of on-line learning. Remember Coursera Machine Learning by Andrew Ng? It is when many of us start to learn about machine learning, but it's also the first time many of us learn an important skill through an on-line curriculum.

Yet these days both Coursera and Udacity seem to have issues to come up with a sustainable business models. For Coursera, [they hired a new CEO back in July last year](https://www.edsurge.com/news/2017-06-13-new-ceo-at-coursera-comes-from-financial-tech-not-higher-ed), and his focus is on searching for a viable business model. Udacity's route is as winding and tortuous. They are thinking of [filing an IPO](https://uk.reuters.com/article/us-udacity-revenue/udacity-with-eye-to-eventual-ipo-says-revenue-more-than-doubled-in-2017-idUKKCN1GB2E2) earlier this year, yet they went through a [round of layoff](https://techcrunch.com/2018/09/28/online-education-unicorn-udacity-has-quietly-laid-off-5-of-staff-at-least-25-people-since-august/). And it seems like they will focus more on corporate training than the current models.

What does it mean to us AI/DL learners? For starter, it might mean that the beloved subsidies for underprivileged students would be gone from on-line learning sites. Or it can also mean development of new materials would slow down.

We hope our prediction is wrong. Hopefully, both Udacity and Coursera can come up with business models which can be both profitable yet cater to learners.

[xconomy.com](https://xconomy.com/san-francisco/2018/12/13/udacity-achieves-50000-nanodegree-grads-amid-company-reorganization/)

## Blog Posts

### [Reading the AI Index 2018 Report ](http://cdn.aiindex.org/2018/AI%20Index%202018%20Annual%20Report.pdf)

The new AI Index report for 2018 is just published last week. We are excited because you may think of it as one report which capture the state of AI development every year. Looking through the report, you may find the section on the growth of AI as a field and its public perception. You may also learn the trend of the state of the art of several fields such as computer vision and machine translation.

The 2017 report was criticized for focusing too much on North America development, but then this year you can see the report cover much of activities around the world. e.g. We learn that Tsinghua University has the highest increase of course enrollment in AI.

Notably missing in the report is automatic speech recognition (ASR). That perhaps has to do with the difficulty of searching for one golden benchmark for ASR. As you may know, ASR performance tremendously across different noise condition.

Anyway, we recommend you to read the report in details.

[aiindex.org](http://cdn.aiindex.org/2018/AI%20Index%202018%20Annual%20Report.pdf)

---

### [How to scale AI Training without voodoo? ](https://blog.openai.com/science-of-ai/)

Last few years, we several works in deep learning training which use large batch size. The advantage of the approach is that you may easily spread the computation of a large batch across several machines.

But here is the problem, how can you decide what batch size to use, or... if a task is suitable to have a large batch size. OpenAI's work seems to give at least one answer to the problem. They found that a simple quantity, gradient noise scale correlate to the optimal batch size in a training task.

Reading the paper, there are many to unpack here. e.g. The authors favor the use of simplified version of the metric which just require calculation of a determinant of a matrix, and the trace of the covariance matrix. They found that such measure correlates with the batch size.

All-in-all, this is indeed an interesting finding because now you may have a guidance for tuning one important parameter, batch size, in your training. Perhaps the question in practice: can you just use a sample of your dataset to training set to measure gradient noise scale, and use it in a larger set? And more importantly, do we have other guidance on tuning other parameters? Those are interesting question to ask, and if we can solve them, may be we can truly call neural network training a science more than an art.

[openai.com](https://blog.openai.com/science-of-ai/)

---

### ["Contributing and bringing machine learning to JavaScript ecosystem with TensorFlow.js" by Manraj Singh](https://medium.com/@manrajsingh/contributing-and-bringing-machine-learning-to-javascript-ecosystem-with-tensorflow-js-55606c365532?fbclid=IwAR0v5mq97bHid-wPaXXQb00s26tNwdC0pTGLrlHvcvWxJV_8hvz769cRbII)

There are many posts on AIDL which ask about how to use a deep learning framework. But there are many of them are about experience in contributing deep learning engine. Singh's post is a notable exception.

[medium.com](https://medium.com/@manrajsingh/contributing-and-bringing-machine-learning-to-javascript-ecosystem-with-tensorflow-js-55606c365532?fbclid=IwAR0v5mq97bHid-wPaXXQb00s26tNwdC0pTGLrlHvcvWxJV_8hvz769cRbII)

---

### Notable AI Blog Posts

BAIR 
- [Scaling Multi-Agent Reinforcement Learning](https://bair.berkeley.edu/blog/2018/12/12/rllib/?fbclid=IwAR0v2zesfYwYmLpxCJ0aeUOSqiSFpgnZY04MGIOQBLt5SQ59r-SakEGckhQ)
- [Building Gene Expression Atlases with Deep Generative Models for Single-cell Transcriptomics](https://bair.berkeley.edu/blog/2018/12/05/genes/)

Google: 
- [Providing Gender-Specific Translations in Google Translate](https://ai.googleblog.com/2018/12/providing-gender-specific-translations.html?fbclid=IwAR3EQO1ahdGa2_bDCmqT93zcMO4homLcHBICXt0jz_dasho83ju3WdKyB6I)

Artificial Intelligence and Deep Learning Weekly

## Open Source

### [Papers With Code ](https://github.com/zziz/pwc?fbclid=IwAR3yO5oandH9f_T0qi8LK7I6_54-lhjQAJqMLjDrdlSTC_gaftPCAbXmGE8#2018)

Written by [Zaur Fataliyev](https://github.com/zziz) and suggested by one of our AIDL moderators, Zubair Ahmed, this github contains papers with its codebase, and it spans from 2013 to 2018. It's a great resource for everyone who not just want to read deep learning papers, but also study the underlying implementations.

[github.com](https://github.com/zziz/pwc?fbclid=IwAR3yO5oandH9f_T0qi8LK7I6_54-lhjQAJqMLjDrdlSTC_gaftPCAbXmGE8#2018)

## About Us

### About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 186,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
