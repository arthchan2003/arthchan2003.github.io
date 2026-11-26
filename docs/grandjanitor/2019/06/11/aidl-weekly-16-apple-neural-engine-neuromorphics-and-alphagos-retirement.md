---
title: "AIDL Weekly #16 - Apple Neural Engine, Neuromorphics and AlphaGo's Retirement"
date: 2019-06-11
---

# AIDL Weekly #16 - Apple Neural Engine, Neuromorphics and AlphaGo's Retirement

# [Issue 16 *June 2nd 2017* ](http://aidl.io/issues/16/index.html#start)

## Editorial

### Editorial

Last week we learned that AlphaGo retired after her glorious career: beating the best human Go player and a team of 5 top players in the world. We include 4 pieces in this issue just to wrap up the event.

None of these should be surprising to AIDL readers though. As we have predicted in [Issue 15](http://aidl.io/issues/15#start): 

> Go joins the pantheon of games like Chess, where computers have proven to be better than humans. As with Chess, research funding will move from Go to some other more complex A.I.-vs-human research projects.

It still leave us a question: what is the meaning of researching AlphaGo? We believe Dr. Andrej Karpathy gives a very good answer - he believes that AlphaGo's research only solve a very narrow sense of AI. Unless we are talking about yet another computer game, it's rather hard for AlphaGo's research to transfer. Take a look of the Blog section to see Dr. K's article.

---

We also heard about all about new chips last week, Apple Neural Engine and ARM new processor. So that's why we also include the Bloomberg piece on Apple Neural Engine. On the same vein, you may heard neuromorphics which purportedly used spiking neural networks, are they real? And are they getting better than the vanilla deep learning chips such as TPU. We include two pieces to analyze the matter.

---

As always if you like our newsletter, feel free to subscribe and forward it your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

## News

### [Apple Neural Engine](https://www.bloomberg.com/news/articles/2017-05-26/apple-said-to-plan-dedicated-chip-to-power-ai-on-devices)

Bloomberg reported that Apple is working on a chip for AI-specific tasks, known as Apple Neural Engine (ANE). The chip would mainly used for facial recognition and speech recognition.

Apple hadn't responded to the report yet, but analysts are whispering what the ANE is going to be. Our guess is that unlike Google's TPU, ANE is more a chip for embedded device like iPhone and IPad. Apple treats privacy matter seriously so it's hard to imagine they come up with a TPU-like chip which focus on processing in data centers. But it's thinkable that Apple would design Neural Engine by putting an optimized matrix computations into a separate unit, much like TPU.

[bloomberg.com](https://www.bloomberg.com/news/articles/2017-05-26/apple-said-to-plan-dedicated-chip-to-power-ai-on-devices)

---

### [AlphaGo vs Ke Jie - Game 3](https://www.youtube.com/watch?v=ru0E7N0-kFE)

Once again, Ke Jie resigned.

Quote from the Game 

> "This Summit is one of the greatest matches that I’ve had. I believe, it’s actually one of the greatest matches in history.” - Ke Jie, 9 Dan Professional, during the post match wrap up
>
>
>
> We held this event aiming to discover new insights into this ancient, beautiful game. I can safely say that what has taken place since Tuesday has exceeded our highest hopes. We have seen many new and exciting moves, and we also saw AlphaGo truly pushed to its limits by the great genius Ke Jie, particularly in the amazing game two. It was thrilling to be in the match room and the control room watching that game unfold, and it has been a truly huge honour to play with such a great master.” - Demis Hassabis, CEO of Deepmind, during the post match wrap up

[youtube.com](https://www.youtube.com/watch?v=ru0E7N0-kFE)

---

### [Prospect of Neuromorphic Chips. ](http://spectrum.ieee.org/semiconductors/design/neuromorphic-chips-are-destined-for-deep-learningor-obscurity)

Is there any design better than GPU/TPU for deep learning? And what if it is like deep learning, which is also biologically-inspired? Then you are thinking about neuromorphics chips, which loosely speaking is to build circuitry based on knowledge of human neurons.

Just a note for our readers: biological and artificial neurons operate in very different principles. For example, biological neurons communicate based on spikes and it's time varying. Whereas, ANN is more a static approximation of biological neural networks, with different activation functions. (\*)

This piece from IEEE gives a great high-level review on the advantages and disadvantages of neuromorphics design, and give you a clear picture what neuromorphic chips and its challenge against systems such as Tensor Process Unit. If you want a more technical version, check out Prof. Eugenio Culurciello's article, which we also included in this issue.

(\*) University of Washington's on-line course on [Computational Neuroscience](https://www.coursera.org/learn/computational-neuroscience) would give you many valuable insights.

[ieee.org](http://spectrum.ieee.org/semiconductors/design/neuromorphic-chips-are-destined-for-deep-learningor-obscurity)

---

### [AlphaGo Defeats Team of Five Top Players](https://techcrunch.com/2017/05/26/googles-alphago-ai-defeats-team-of-five-leading-go-players/?ncid=rss&utm_source=tctwreshare&utm_medium=feed&utm_campaign=Feed%3A+Techcrunch+%28TechCrunch%29&sr_share=twitter)

After two wins against Ke Jie, AlphaGo was able to defeat a committee of five top players, or "Team Go". Is it a significant event?

Let's think in this way: In terms of Elo points, given AlphaGo records (50 wins 1 lose), we may safely say it is around 400 Elo points stronger than the strongest human player.

The question is would forming a committee of five players overcome this 400 points difference? We doubt, because humans also have to communicate when they decide a move, and it seems to be a much slower channel. In a nutshell, it doesn't seem to be a surprise AlphaGo also beat "Team Go".

[techcrunch.com](https://techcrunch.com/2017/05/26/googles-alphago-ai-defeats-team-of-five-leading-go-players/?ncid=rss&utm_source=tctwreshare&utm_medium=feed&utm_campaign=Feed%3A+Techcrunch+%28TechCrunch%29&sr_share=twitter)

---

### [Google Launches AI Investment Platform.](https://www.axios.com/exclusive-google-launches-ai-investment-arm-2423046588.html)

We will just quote the Axios' article here: 

> Why it matters: Google has never before had an investment effort aimed at a specific type of technology. Plus, this will be led by engineers, rather than by professional venture capitalists.

[axios.com](https://www.axios.com/exclusive-google-launches-ai-investment-arm-2423046588.html)

---

### [AlphaGo's Retirement](https://www.theverge.com/2017/5/27/15704088/alphago-ke-jie-game-3-result-retires-future)

After defeating the best Go player, DeepMind announces that they are retiring AlphaGo. CEO Dennis Hassabis states: 

> The research team behind AlphaGo will now throw their considerable energy into the next set of grand challenges, developing advanced general algorithms that could one day help scientists as they tackle some of our most complex problems, such as finding new cures for diseases, dramatically reducing energy consumption, or inventing revolutionary new materials.

[theverge.com](https://www.theverge.com/2017/5/27/15704088/alphago-ke-jie-game-3-result-retires-future)

## Blog Posts

### [AlphaGo, in Context By Andrej Karpathy](https://medium.com/@karpathy/alphago-in-context-c47718cb95a5)

After AlphaGo retired, there is a void on what AlphaGo means to the development of machine learning. I think Dr. Karpathy's article is the first analysis piece which looks at the research merit of AlphaGo. More importantly, how much AlphaGo's research can be applied to the next big problem?

Dr. K is quite blunt: 

> While AlphaGo does not introduce fundamental breakthroughs in AI algorithmically, and while it is still an example of narrow AI, AlphaGo does symbolize Alphabet’s AI power: in both the quantity/quality of the talent present in the company, the computational resources at their disposal, and the all in focus on AI from the very top.

I (Arthur Chan) got to agree. Before the Summit, I wondered there is any doubt AlphaGo would lose. So further development would only advance just the narrow field of computer Go. That's why I appreciate Hassabis to retire the program. There are more unsolved problems in ML - robot picking or true understanding of language. Even in games, RTS such as Starcraft II is much more interesting problem.

[medium.com](https://medium.com/@karpathy/alphago-in-context-c47718cb95a5)

---

### [NN solve differential equations. ](https://becominghuman.ai/neural-networks-for-solving-differential-equations-fa230ac5e04c)

We post several more interesting articles on the technical side. The first is about how neural network can solve differential equations, written by Alex Honchar. He starts from explaining how to use NN to solve ODE, then move on to partial differential equations. Honchar also included TF code as an example.

[becominghuman.ai](https://becominghuman.ai/neural-networks-for-solving-differential-equations-fa230ac5e04c)

---

### [Variational Bayes](http://www.openias.org/variational-coin-toss)

This is a great article on using variational Bayes, which is widely used in both deep learning and non-deep learning problems. This article start from the tractable cases of VB method such as binomial and Gaussian, and it follows by why evidence lower bound (ELBO) is commonly used in literature. It's helpful if you want to understand the basic principle of VB.

[openias.org](http://www.openias.org/variational-coin-toss)

---

### [Neuromorphics and Deep Neural Networks](https://medium.com/@culurciello/neuromorphic-and-spiking-or-not-894a836dc3b3)

I have been following [Prof. Eugenio Culurciello](https://twitter.com/culurciello) on Plus and [Twitter](https://twitter.com/culurciello) for quite some time. Mainly because his skill sets is rare even in our exotic world of deep learning. For 10 years, he was researching on implementations of neuromophic chip. He also start a deep learning class, so you can think he wields the knowledge in both VLSI design and deep learning. In this piece, he analyze the advantage of using spiking neural network vs deep learning-based approach. For example, why using neural system could reduce power consumption, how its compute are different down to the level of using transistors. It's a good piece if you want to read further the IEEE piece.

[medium.com](https://medium.com/@culurciello/neuromorphic-and-spiking-or-not-894a836dc3b3)

---

### [Human Level AI - When will we have it?](http://spectrum.ieee.org/computing/software/humanlevel-ai-is-right-around-the-corner-or-hundreds-of-years-away)

This is an interesting IEEE piece, interviewing technologists and visionaries on where we stand on AGI. There are essentially two camps of the interviewees. One group is more conventionally into predicting the future, such as Robin Hanson and Ray Kurzweil. There is another group which consists of real technologists such as Jürgen Schmidhuber. We believe the latter group's thinking is more concrete and perhaps more indicative of the future.

[ieee.org](http://spectrum.ieee.org/computing/software/humanlevel-ai-is-right-around-the-corner-or-hundreds-of-years-away)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing)

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## About Us
