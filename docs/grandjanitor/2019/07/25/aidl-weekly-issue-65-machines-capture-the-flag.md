---
title: "AIDL Weekly Issue #65 - Machines! Capture The Flag!"
date: 2019-07-25
---

# AIDL Weekly Issue #65 - Machines! Capture The Flag!

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 65 *July 9th 2018* ](http://aidl.io/issues/65/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we cover Adrian Rosebrock's interview with François Chollet. We also discuss Ben Evans' article on "Ways of Thinking About Machine Learning" and how DeepMind now can play Quake III's "Capture The Flag" at human level.

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 155,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Signal Media $16M](https://techcrunch.com/2018/06/27/ai-fueled-market-intelligence-firm-signal-media-takes-16m-to-tackle-more-targets/)
- [ThetaWay $30M](https://venturebeat.com/2018/07/02/thetaray-raises-30-million-to-grow-its-ai-powered-cybersecurity-business/)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [An interview with François Chollet by Adrian Rosebrock](https://www.pyimagesearch.com/2018/07/02/an-interview-with-francois-chollet/)

François Chollet is the lead developer of Keras, a popular package that interfaces with Tensorflow, Theano and Pytorch. A little about the interviewer too: Adrian Rosebrock has been making a name for his many hand-ons tutorial of using OpenCV, Nvidia DIGITS for deep learning applications. His questions are sharp and touch on many issues in AI today.

[pyimagesearch.com](https://www.pyimagesearch.com/2018/07/02/an-interview-with-francois-chollet/)

---

### [Capture The Flag](https://deepmind.com/blog/capture-the-flag/)

After AlphaGo, we are all looking for the next breakthrough in AI. So this piece on how DeepMind cracks Quake III Capture the Flag is interesting.

To understand this piece, you should understand that the agent is learning only from pixels and scores, they weren't told about the rules. This is quite unlike OpenAI's work on DotAI which quite [a few of assumptions were made](http://www.wildml.com/2017/08/hype-or-not-some-perspective-on-openais-dota-2-bot/).

More interestingly, after training with human players and self-play, the agent shows cooperative behavior. That makes sense: if you put an RL-agent in an environment which cooperation is rewarded, then obviously the agent will cooperate more.

As Jack Clark mentioned in his [Import AI](https://jack-clark.net/) newsletter, this result doesn't seem to get as much press as other DeepMind's result. It's a pity. Large scale RL-training can now competitive and cooperative players, we think it's a big deal.

You can also find the paper version at [here](https://arxiv.org/pdf/1807.01281.pdf).

[deepmind.com](https://deepmind.com/blog/capture-the-flag/)

---

### [Ways to Think about Machine Learning](https://www.ben-evans.com/benedictevans/2018/06/22/ways-to-think-about-machine-learning-8nefy)

This is written by Ben Evans who works at a16z, trending around two weeks ago. Evans suggest several helpful ways to think of ML. For example, he believes thinking of ML as AI is really unhelpful. It's much more useful to think of ML as automation. In a way, that follows the view from industrial revolution. i.e. machines are slowly replacing humans. Evans works in a16, so his view certainly comes from practice.

Another thought, which is intertwined with his view that "ML as automation", is the idea that ML is a foundational technology similar to relational database in 80s. This is an interesting view. In fact, say if you just think about technology such as image classification, it is really the foundation of other relevant technologies such detection, segmentation. And of course, most medical image classification is still, in a nutshell, image classification based on Convnet. And who knows, what will people dream up in the next 10 years?

We think Evans' article is a useful view to look at AI, his view is more helpful than say thinking AI is a super-intelligence, or AI will steal our jobs. Those are wishful thinkings mixed up with fears and silly imaginations.

[ben-evans.com](https://www.ben-evans.com/benedictevans/2018/06/22/ways-to-think-about-machine-learning-8nefy)

## Open Source

### [ModaNet](https://arxiv.org/abs/1807.01394)

Here is a clothing dataset which is annotated in polygons. ModaNet is based on the [PaperDoll dataset](http://tamaraberg.com/papers/paperdoll.pdf) with 50k+ images. It's useful for such as commercial clothing classification and understanding.

[arxiv.org](https://arxiv.org/abs/1807.01394)

## Contemporary Classic

### [Understanding LSTMs](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)

LSTM is a tough subject. When you first see a LSTM, you will mostly be mesmerized by its complicated structure as compared to a simple vanilla DNN. There seems to be few keys for understanding: 
- It's helpful to think of each gate as a neural network. So an LSTM-unit is just a composition of multiple networks where each has its unique function.
- Forget about the diagram. This is a rare case that understanding the equations first is more important.
- Start from a simpler architecture such as [GRU](https://arxiv.org/pdf/1406.1078.pdf). Update and reset gates are more intuitive to understand than the standard 3-gate form of LSTM.

That said, if you do want to learn LSTM better, we highly recommend you to read this article from Chris Olah. In the article, Olah dissect the an LSTM, more importantly, map different gates to its corresponding equations. It was a very helpful tool for one of us (Arthur) to understand the subject.

[github.io](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 155,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
