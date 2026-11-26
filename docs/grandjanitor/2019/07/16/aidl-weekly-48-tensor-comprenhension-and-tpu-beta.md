---
title: "AIDL Weekly #48 - Tensor Comprenhension and TPU beta"
date: 2019-07-16
---

# AIDL Weekly #48 - Tensor Comprenhension and TPU beta

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 48 *February 17th 2018* ](http://aidl.io/issues/48/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Perhaps the most interesting news last week is Facebook's Tensor Comprehension. Google's TPU is also at its beta stage. The price is ~4x more expensive than the P100 pool, but we are still very excited.

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

This newsletter is a labor of love from us. All publishing costs and operating expenses are paid out of our pockets. If you like what we do, you can help defray our costs by sending a donation via [link](http://paypal.me/aidlio/9). For crypto enthusiasts, you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## News

### [TPU is now beta in Cloud](https://techcrunch.com/2018/02/12/googles-custom-tpu-machine-learning-accelerators-are-now-available-in-beta/)

Enough said, it's currently billing $6.50/hour, so more than 4 times than the P100 pool ($1.46/hour).

[techcrunch.com](https://techcrunch.com/2018/02/12/googles-custom-tpu-machine-learning-accelerators-are-now-available-in-beta/)

## Blog Posts

### [Trade with RL](http://www.wildml.com/2018/02/introduction-to-learning-to-trade-with-reinforcement-learning/?lipi=urn%3Ali%3Apage%3Ad_flagship3_feed%3BHVokF2EaRxKqj8erYR%2Fizg%3D%3D)

Denny Britz hadn't written a post for a long time, but all his post are worthwhile to read. In this post, he talks about a potential research direction on using RL to do trading. The research direction is fun, but it also has a paragraph on how order book work, which we found very educational.

As he said, this is not about using DL to predict stock price. And Eh - as we discussed in the forum, there is obvious problem with using supervised learning to predict price. :)

[wildml.com](http://www.wildml.com/2018/02/introduction-to-learning-to-trade-with-reinforcement-learning/?lipi=urn%3Ali%3Apage%3Ad_flagship3_feed%3BHVokF2EaRxKqj8erYR%2Fizg%3D%3D)

---

### [Deep Reinforcement Learning Doesn't Work Yet By Alex Irpan ](https://www.alexirpan.com/2018/02/14/rl-hard.html)

This article summarized the problems of RL, what it is really good for, which is mostly competitive games. And its limitations.

[alexirpan.com](https://www.alexirpan.com/2018/02/14/rl-hard.html)

---

### [Facebook's Tensor Comprehension](https://research.fb.com/announcing-tensor-comprehensions/)

Facebook's Tensor Comprehension (TC) package took the spotlight last week. It promised a lot, given a symbolic matrix expression, TC is able to find the best CUDA kernel code with the right synchronization and parallelization. The implementation can be further tuned through evolutionary strategy. This sounds extremely powerful, that's perhaps why even Head of FAIR, Prof. Yann Lecun, gave it a [mention](https://www.facebook.com/groups/DeepNetGroup/permalink/571546453238241/).

[fb.com](https://research.fb.com/announcing-tensor-comprehensions/)

---

### [The Problem of Replication in ML](http://www.sciencemag.org/news/2018/02/missing-data-hinder-replication-artificial-intelligence-studies)

This piece from Science Magazine discusses on intrinsic difficulty of advancing AI, namely how to replicate experiments from papers. We think it is indeed a major roadblock in both practical and research development.

[sciencemag.org](http://www.sciencemag.org/news/2018/02/missing-data-hinder-replication-artificial-intelligence-studies)

---

### [Why is ML in Finance hard?](https://www.hardikp.com/2018/02/11/why-is-machine-learning-in-finance-so-hard/)

We found this post useful because many members are asking us how to implement a predictor for financial data, e.g. DJI or simply crytocurrencies' price. Yet quantitative finance is hard, what's the reason behind? This article would give you a good explanation.

[hardikp.com](https://www.hardikp.com/2018/02/11/why-is-machine-learning-in-finance-so-hard/)

## Paper/Thesis Review

### [Preparing for ML interviews](https://docs.google.com/presentation/d/1KmmchoykI_dJUYe5mw8Mrz1HdZlM6NE8wSIV7uVKF0A/edit#slide=id.g10d8a2531040fd33_36)

This presentation, prepared by Sravya Tirukkovalur, gives a comprehensive approach on how to interview on ML-related jobs. We like the part about "knowing vs explaining", which is indeed a tough skill to learn in real-life.

[google.com](https://docs.google.com/presentation/d/1KmmchoykI_dJUYe5mw8Mrz1HdZlM6NE8wSIV7uVKF0A/edit#slide=id.g10d8a2531040fd33_36)

## Contemporary Classic

### [Chomsky on AI](https://www.theatlantic.com/technology/archive/2012/11/noam-chomsky-on-where-artificial-intelligence-went-wrong/261637/?utm_source=fbb)

The Atlantic ran an interview with Prof. Noam Chomsky back in 2012. As you know, he is known to have profound contribution to the field of linguistic. On the other hand, he is vocal critic of using probabilistic methods in current days AI.

We don't pretend to understand all points from Prof. Chomsky. But check out this interview. The interviewer, Yarden Katz, was an MIT graduate student in the Department of Brain and Cognitive Science, now a fellow of System Biology at Harvard. He asked brilliant questions and Chomsky's answer deserve your attention.

Here are several gems in the interview: 
- On statistics and probability:

Chomsky: *Well ... there's nothing wrong with probability theory, there's nothing wrong with statistics. [...] If you can use it, fine. But the question is what are you using it for? First of all, first question is, is there any point in understanding noisy data? Is there some point to understanding what's going on outside the window?* 
- On cognitive science:

Chomsky: *It's worth remembering that with regard to cognitive science, we're kind of pre-Galilean, just beginning to open up the subject.* 
- On the original AI:

Chomsky: *"I have to say, myself, that I was very skeptical about the original work [in AI]. I thought it was first of all way too optimistic, it was assuming you could achieve things that required real understanding of systems that were barely understood, and you just can't get to that understanding by throwing a complicated machine at it."*

[theatlantic.com](https://www.theatlantic.com/technology/archive/2012/11/noam-chomsky-on-where-artificial-intelligence-went-wrong/261637/?utm_source=fbb)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 100,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
