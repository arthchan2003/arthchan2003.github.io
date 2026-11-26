---
title: "Issue 60 - Teach Machines Cause and Effect"
date: 2019-07-18
---

# Issue 60 - Teach Machines Cause and Effect

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 60 *May 27th 2018* ](http://aidl.io/issues/60/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we take a closer look at Prof. Judea Pearl's interview with Quanta Magazine on how he thinks about the current limitations of machine learning. You can find out in our Blog section. 

To those in the U.S., happy Memorial Day weekend!

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 143,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Unisound $100M](https://www.chinamoneynetwork.com/2018/05/11/chinese-ai-firm-unisound-raises-100m-series-c-round-led-by-china-electronics-health-fund)
- [Roadstar.ai record-breaking $128M](http://www.scmp.com/tech/start-ups/article/2146275/start-roadstarai-gets-record-us128m-funding-autonomous-car-race-baidu)
- [Softbank $21M for a Chinese robotic firm ](https://www.chinamoneynetwork.com/2018/05/18/softbank-cvc-china-creation-ventures-co-lead-21m-round-in-chinese-robotic-firm)
- [Ojo Labs $205M](https://www.housingwire.com/articles/43413-texas-based-ojo-labs-raises-205-million-to-bring-ai-to-real-estate)

Artificial Intelligence and Deep Learning Weekly 

---

### Pulse: Intel

Two pieces of news about the new Intel AI group, which released both an [NLP deep learning library](https://venturebeat.com/2018/05/24/intel-ai-lab-open-sources-library-for-deep-learning-driven-nlp/) and the [Nervana chip for accelerated AI training](https://venturebeat.com/2018/05/23/intel-unveils-nervana-neural-net-l-1000-for-accelerated-ai-training/). By most measures, these products are not ground-breaking. However, Intel continues to chip away into the AI space. 

Artificial Intelligence and Deep Learning Weekly

---

### [Xiaoice can also have a phone conversation](https://www.theverge.com/2018/5/22/17379508/microsoft-xiaoice-chat-bot-phone-call-demo)

As you might recall, two weeks ago when Google release Duplex, there was surprising [backlash at the product](https://www.theverge.com/2018/5/9/17335710/google-duplex-phone-call-ai-assistant-service-industry). Microsoft seems have learnt from Google's lesson, as well as [its own](https://www.theverge.com/2016/3/24/11297050/tay-microsoft-chatbot-racist) misfire. The release of Xiaoice is much more subdued. 

The details are also different, Xiaoice doesn't make phone calls for you, instead it holds a call. The data used to train the two systems are different.

As with Duplex, we couldn't quite find the technical papers of Xiaoice. If we succeed in our sleuthing, you'll be the first to know.

[theverge.com](https://www.theverge.com/2018/5/22/17379508/microsoft-xiaoice-chat-bot-phone-call-demo)

## Blog Posts

### [Teach Them Cause and Effect](https://www.quantamagazine.org/to-build-truly-intelligent-machines-teach-them-cause-and-effect-20180515/)

In this Quanta Magazine's interview, Prof. Judea Pearl talked about his view on why learning cause and effect is important to AI research. His interview is filled with gems, so we will give you a summary of quotes here: 

On deep learning: 

> As much as I look into what’s being done with deep learning, I see they’re all stuck there on the level of associations.

On deep learning is just curve fitting: 

> (Q: it sounds like you’re not very impressed with machine learning.) No, I’m very impressed, because we did not expect that so many problems could be solved by pure curve fitting.

On the limitation of deep learning as well as why it is hard to explain his ideas to researcher 

> AI is currently split. First, there are those who are intoxicated by the success of machine learning and deep learning and neural nets. They don’t understand what I’m talking about. They want to continue to fit curves. But when you talk to people who have done any work in AI outside statistical learning, they get it immediately. I have read several papers written in the past two months about the limitations of machine learning.

On free will in machines? 

> We’re going to have robots with free will, absolutely. We have to understand how to program them and what we gain out of it. For some reason, evolution has found this sensation of free will to be computationally desirable.

Prof. Pearl's main thesis is that AI should understand how causality works in nature. This allows machine to postulate hypotheses just like humans do: 

> It turned out to be a great thrill for me to see that a simple calculus of causation solves problems that the greatest statisticians of our time deemed to be ill-defined or unsolvable. And all this with the ease and fun of finding a proof in high-school geometry.

All-in-all, a very interesting interview. Do cause and effect matter? It's above our pay grade to judge. But today's AI certainly doesn't have a complete answer to model cause and effect. Prof. Pearl's work is perhaps some of the rare exceptions.

[quantamagazine.org](https://www.quantamagazine.org/to-build-truly-intelligent-machines-teach-them-cause-and-effect-20180515/)

---

### [ML beyond Curve Fitting: An Intro to Causal Inference and do-Calculus](http://www.inference.vc/untitled/)

Here's an excellent post written by Ferenc Huszár, on the basics of casual model proposed by Judea Pearl. In particular, it gives a great summary on how *do*-calculus work. We are also new to the idea. But Huszár has done a great job to explain the difference between observation and interventional distribution. Why do-calculus can give you an approximation of the interventional distribution, and how deep learning can potential apply to the idea. We find this an illuminating read. 

[inference.vc](http://www.inference.vc/untitled/)

---

### [BAIR: Delayed Impact of Fair Machine Learning](http://bair.berkeley.edu/blog/2018/05/17/delayed-impact/)

Normally when you think of fair machine learning, you would generally think of using a criterion other than profit as a kind of method of selection such as fairness. But then in this BAIR blog, authors Liu et al found that in certain situations, these selection methods don't really optimize for the long term benefit for a group. So here's where ML can help. 

Check out the details from the blog and here is the [corresponding paper](https://arxiv.org/pdf/1803.04383.pdf).

[berkeley.edu](http://bair.berkeley.edu/blog/2018/05/17/delayed-impact/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 143,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760 

Artificial Intelligence and Deep Learning Weekly
