---
title: "AIDL Weekly Issue #66 - Uber Lays Off 100 SDC operators"
date: 2019-07-25
---

# AIDL Weekly Issue #66 - Uber Lays Off 100 SDC operators

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 66 *July 13th 2018* ](http://aidl.io/issues/66/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We have a **BIG** announcement this week. We launched [Expertify](https://expertify.co), our messaging web app, for our 155,000 A.I. community members to engage and discuss in real-time.

Hope you can join and try it out.

In other news, we look at two technical stories this week: 
- How DeepMind is measuring abstract reasoning, and actually what are the abstract reasoning we are talking about?
- The new Facebook Talk the Walk task - how would AI guide a tourist through the New York City?

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 155,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: twenty_by_nine_extra_large_1683ccfa-0d5d-4064-816d-ddf7a3a2795e.png]*](https://leap.ai/?utm_source=newsletter&utm_medium=email&utm_content=title&utm_campaign=aidl) 

### [Let AI help you figure out which opportunities and jobs are right for you!](https://leap.ai/?utm_source=newsletter&utm_medium=email&utm_content=title&utm_campaign=aidl)

Being bombarded by recruiters trying to poach you for Machine Learning & AI talent? Hard to decide which opportunities are worth considering? 

AI can help you! Leap’s AI-powered Instant Match Algorithm considers your experience, passions, strengths, and preferences to get the best matches for YOU in real-time. Simply follow these 3 simple steps to land your dream ML/AI job! 
- Step 1 - Upload your resume on Leap.ai
- Step 2 - Identify your strengths and passions and get personalized matches
- Step 3 - Apply to the right opportunities. Get Endorsed. Guaranteed Interviews.

[Get Matched Now!](https://leap.ai/?utm_source=newsletter&utm_medium=email&utm_content=cta&utm_campaign=aidl)

[leap.ai](https://leap.ai/?utm_source=newsletter&utm_medium=email&utm_content=title&utm_campaign=aidl)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Uber Lays Off 100 SDC operators](https://www.cnbc.com/2018/07/12/uber-lays-off-100-self-driving-car-operators-in-pittsburgh.html)

We should ask : what does this mean to Uber SDC? And what does it mean to SDC in general?

[cnbc.com](https://www.cnbc.com/2018/07/12/uber-lays-off-100-self-driving-car-operators-in-pittsburgh.html)

---

### Deals

- [Pony.ai $102M](https://venturebeat.com/2018/07/11/pony-ai-raises-102-million-to-deploy-self-driving-cars-in-beijing/)
- [Glasswing venture closes it AI-focused fund for $112M](https://techcrunch.com/2018/07/12/glasswing-ventures-closes-its-artificial-intelligence-focused-fund-with-112-million/)
- [Meero $45M Round](https://venturebeat.com/2018/07/12/meero-raises-45-million-to-take-its-ai-driven-photography-platform-global/)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [DeepMind papers at ICML 2018](https://deepmind.com/blog/deepmind-papers-icml-2018/)

Several interesting papers in our mind: 
- [Machine Theory of Mind](https://arxiv.org/abs/1802.07740)
- [Parallel WaveNet: Fast High-Fidelity Speech Synthesis](https://arxiv.org/abs/1711.10433)
- [Efficient Neural Audio Synthesis](https://arxiv.org/abs/1802.08435)
- [Measuring abstract reasoning in neural networks](http://proceedings.mlr.press/v80/santoro18a/santoro18a.pdf) - see the next item.

[deepmind.com](https://deepmind.com/blog/deepmind-papers-icml-2018/)

---

### [DeepMind's Measuring Abstract Reasoning](https://deepmind.com/blog/measuring-abstract-reasoning/)

This recent work from DeepMind probably catch many of our eyes. What are DeepMind doing? And how are they measuring reasoning from AI?

First of all, what is the abstract reasoning the blog is talking about. In fact, we are really talking about a particular type of intelligence test called "Raven's Progressive Matrices" (RPMs). See the [Wikipedia Page](https://en.wikipedia.org/wiki/Raven%27s_Progressive_Matrices) for some examples. Basically you are given panels of figures each have geometric shapes or patterns and your goal is to reason what should the next panel look like. It is mostly a visual reasoning test for humans. They were first presented with sequences of shapes, colors and patterns in several panels and then asked to derive the las.

With this setup, it's not hard to imagine that you can come up with a task which machines can be used for guessing answers for RPMs. As you might read from the blog, the best architecture is what the authors called wild relationship network (WRAN). What is WRAN? Actually it's rather simple. Say you are given K panels. You just run your favorite network on the task, then the answer would be summed and feed into another MLP.

At this point you might ask, "Hmm. So how much of this really measure abstract reasoning that I am thinking about?" The truth is, not much, even the authors admit that visual reasoning is only part of general-purpose abstract reasoning. Still it's interesting to see if machines can be used to solve a popular IQ test of humans.

If you view it this way, experimental results of the paper are quite fascinating, e.g. the DeepMind researchers have tried to add distractor into panels to see if performance drop. For more details, you might want to take a look of [the paper version of the work](http://proceedings.mlr.press/v80/santoro18a/santoro18a.pdf). You may also find the original data set at [here](https://pantheon.corp.google.com/storage/browser/ravens-matrices?pli=1)

[deepmind.com](https://deepmind.com/blog/measuring-abstract-reasoning/)

## Open Source

### [Andrew Trask's New Book](https://twitter.com/iamtrask/status/1017501946482249728)

We are always fans of Andrew Liam Trask. He is almost finishing a deep learning book. Follow the link to download it!

[twitter.com](https://twitter.com/iamtrask/status/1017501946482249728)

---

### [Navigating New York City by AI Talking With Each Other](https://arxiv.org/abs/1807.03367)

Here's an exciting new task introduced by FB - can we use an AI agent to guide tourist through New York City *verbally*? In the task "Talk the Walk", two agents, "a guide" and "a tourist" has the common goal to reach a target location through dialogue. The "tourist" only access the street view, and can communicate with the "guide" through natural language dialogue. Whereas the guide can only guess the tourist location through a map. This is definitely an open problem. Can AI resolve this task?

First of all, the street view actually comes with landmarks. So the first tasks is to come up with a guess of where the "tourist" is, or tourist localization in the paper. This doesn't make the task easy - the ground truth suggest that landmark observation doesn't always localize a tourist. The team then tries to come up with a method which also account for other information from tourist and map them into a coordinate in the map.

It sounds like a difficult but an interesting open problem to us. Here we are talking about two agents which NLP dialogue is the only means of communication, and thus you can imagine information will be lost in the process. The task sounds really cool and can have major applications in real life. So check it out!

[arxiv.org](https://arxiv.org/abs/1807.03367)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 156,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
