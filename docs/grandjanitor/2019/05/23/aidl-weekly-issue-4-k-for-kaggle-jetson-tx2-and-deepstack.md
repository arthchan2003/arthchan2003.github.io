---
title: "AIDL Weekly Issue 4: K for Kaggle, Jetson TX2 and DeepStack"
date: 2019-05-23
---

# AIDL Weekly Issue 4: K for Kaggle, Jetson TX2 and DeepStack

Thoughts From Your Humble Curators

Three big news last week: 
1. [Google acquired Kaggle](https://techcrunch.com/2017/03/07/google-is-acquiring-data-science-community-kaggle/)
2. [Jetson TX2](https://blogs.nvidia.com/blog/2017/03/07/surrounded-by-ai-devices-that-do-everything-from-flying-to-farming-nvidia-launches-jetson-tx2/) was out,
3. Just like its rival Libratus, [DeepStack](http://spectrum.ieee.org/automaton/robotics/artificial-intelligence/texas-holdem-ai-bot-taps-deep-learning-to-demolish-humans) made headlines for beating human poker pros.

In this Editorial though, we want to bring to your attention is this little paper titled "Stopping GAN Violence: Generative Unadversarial Networks". After 1 minute of reading, you would quickly notice that it is a fake paper. But to our dismay, there are newsletters just treat the paper as a serious one. It's obvious that the "editors" hadn't really read the original paper.

It is another proof point that the current deep learning space is a over-hyped. Similar happened to [Rocket AI](https://medium.com/the-mission/rocket-ai-2016s-most-notorious-ai-launch-and-the-problem-with-ai-hype-d7908013f8c9)). You can get a chuckle out of it but if over-done, it could also over-correct when expectations aren't met.

Perhaps more importantly, as a community we should spend more conscious effort to fact-check and research a source before we share. We at AIDL Weekly, follow this philosophy religiously and all sources we include are carefully checked - that's why our newsletter stands out in the crowd of AI/ML/DL newsletters.

If you like what we are doing, check out [our FB group](https://www.facebook.com/groups/DeepNetGroup/), our [YouTube channel](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg).

And of course, please [share](http://ctt.ec/oecC4) this newsletter with friends so they can [subscribe](https://aidlweekly.curated.co/) to this newsletter.

Artificial Intelligence and Deep Learning Weekly

### [Google is acquiring Kaggle](https://techcrunch.com/2017/03/08/google-confirms-its-acquisition-of-data-science-community-kaggle/)

First brought up by [TechCrunch](https://techcrunch.com/2017/03/07/google-is-acquiring-data-science-community-kaggle/), Google finally confirmed its acquisition of Kaggle. As you know, Kaggle is the most popular machine learning/data science competition platform. So this move of Google will make the Google's brand and frameworks more entrenched in the data science/machine learning community. We think this is a brilliant acquisition move that helps Google on many levels - recruiting, mindshare, framework dissemination, talent pipelining, etc. 

[techcrunch.com](https://techcrunch.com/2017/03/08/google-confirms-its-acquisition-of-data-science-community-kaggle/)

---

### [Jetson TX2](https://blogs.nvidia.com/blog/2017/03/07/surrounded-by-ai-devices-that-do-everything-from-flying-to-farming-nvidia-launches-jetson-tx2/)

Credit-card sized Jetson TX2 is going to bring embedded deep learning to another level. TX2 has very similar layout as [TX1](http://www.nvidia.com/object/embedded-systems-dev-kits-modules.html). It has a better spec, most notably having 8G memory instead of 4G. So you can think of TX2 as the premium version of the Jetson line of Nvidia products.

In the future, Nvidia is probably going to replace the old TX1 soon - it reflects from the pricing: TX2 is only $100 more expensive than TX1, at $599, but a volume order for 1000, would only cost $399, which would be $100 cheaper than TX1's retail price.

One interesting question we may ask. Now that the Jetson line has more memory. How would it match up with cards such as GTX 1080 or even 1080 Ti? We are curious to look at benchmarking results soon.

[nvidia.com](https://blogs.nvidia.com/blog/2017/03/07/surrounded-by-ai-devices-that-do-everything-from-flying-to-farming-nvidia-launches-jetson-tx2/)

---

[*[image not recovered: twenty_by_nine_extra_large_8312dc87-98aa-4bf5-9df5-9428b878cdf8.png]*](http://spectrum.ieee.org/automaton/robotics/artificial-intelligence/texas-holdem-ai-bot-taps-deep-learning-to-demolish-humans) 

### [DeepStack Demolish Pros](http://spectrum.ieee.org/automaton/robotics/artificial-intelligence/texas-holdem-ai-bot-taps-deep-learning-to-demolish-humans)

After Go, perhaps poker is the next frontier of A.I.. And out of all poker games, no-limit Texas Hold'em is perhaps the most important form for machines to master - it was well-known to be a game of psychology and requires complex strategy. 

As you might recall, [CMU's Libratus](http://spectrum.ieee.org/automaton/robotics/artificial-intelligence/ai-learns-from-mistakes-to-defeat-human-poker-players) was also able to beat the pros by 1.7 million US dollars. So how is DeepStack different then?

For starter, Libratus based its play with end-game solving, which requires a supercomputer to run 15 million core hours. Whereas DeepStack only used a gaming laptop. It doesn't calculate all steps ahead but only few. Instead, what DeepStack doing is similar to [AlphaGo](http://www.nature.com/nature/journal/v529/n7587/full/nature16961.html): As described in their [January arxiv paper](https://arxiv.org/abs/1701.01724), Information including pot size, public cards, and the player card ranges was fed to a 7-layer feedforward neural network. The output of the network is counterfactual values used in counterfactual regret minimization (CFR). DeepStack's FNN requires clustering of player card ranges. The last layer is used to enforce zero-sum properties.

In layman's terms, this makes DeepStack having human-like intuition on how different card-combinations valued. It turns out such knowledge seems to be as powerful as computation-heavy end-game solving. DeepStack beats 10 out of 11 pros with a significant margin of victory.

Last thing to mention, the workflow of Libratus requires human in the loop to remove repeated patterns daily. DeepStack doesn't have such requirements. So while DeepStack is less publicized, we found it at least as interesting as the Libratus effort.

(Diagram Credit: p.9 of "DeepStack: Expert-Level Artificial Intelligence in Heads-Up No-Limit Poker" by Matej Moravcik et al)

[ieee.org](http://spectrum.ieee.org/automaton/robotics/artificial-intelligence/texas-holdem-ai-bot-taps-deep-learning-to-demolish-humans)

## Blog Posts

### [Tensorflow XLA Explained](https://developers.googleblog.com/2017/03/xla-tensorflow-compiled.html)

As you might recall, [Tensorflow 1.0 was released at mid-February](http://venturebeat.com/2017/02/15/google-releases-tensorflow-1-0-with-new-machine-learning-tools/). One of the key features in Accelerated Linear Algebra [(XLA)](https://www.tensorflow.org/versions/master/experimental/xla/). In essence, what XLA does is to remove any duplicated calculation by analyzing a Tensorflow graph. So you may think of it as something similar to the optimization flag -O2 for gcc.

XLA is still an experimental feature. (See the header of this [link](https://www.tensorflow.org/versions/master/experimental/xla/)). So Tensorflow official document stresses that not all users will experience the benefit of such optimization. This makes sense because if you already specified a fairly optimized network manually, XLA wouldn't do too much for you anyway.

So what's the significance of XLA? In recent years, there has been a lot of buzz on modularization of neural networks. It's possible that in the future we will just have several existing architectures and we just decide to merge them together. Then, having an automatic optimizer for computational graph would be very useful.

[googleblog.com](https://developers.googleblog.com/2017/03/xla-tensorflow-compiled.html)

---

### [On the Origin of Deep Learning](https://arxiv.org/abs/1702.07800)

This is a fairly extensive survey of deep learning. The first author, [Haohan Wang](https://www.cs.cmu.edu/~haohanw/) is a PhD candidate at CMU's Language Technology Institute (LTI) and first-authored four papers in the domain of computational biology.

I (Arthur) found the material in-depth. For example, treatment of [Hopfield net](https://en.wikipedia.org/wiki/Hopfield_network) which starts from physical origin of the term "energy". And it is very helpful to understand the origin of Hopfield net. (Hinton's lecture helps, but I would be less confused to know "Oh, actually Hopfield network is [isomorphic to the Ising model of magnetisim](https://page.mi.fu-berlin.de/rojas/neural/chapter/K13.pdf)!")

Notice though, at this point, Wang is still constantly updating the arxiv version of the paper - the paper is now at version 4 after it was two weeks ago. I do find the paper quite enjoyable and it covers some less discussed concepts from standard on-line classes. So I recommend you all to read the paper.

[arxiv.org](https://arxiv.org/abs/1702.07800)

---

### [Prank of the Week: "Stopping GAN Violence: Generative Unadversarial Networks"](https://arxiv.org/abs/1703.02528)

Many AIDLer have shared the following paper to our forum. Just want to inform you. So FYI: this is a **prank**. Couple of very non-subtle hints: 
1. Authorship: Samuel Albanie works for "Institute of Deep Statistical Harmony",
2. "In this work, we quantify the financial, social, spiritual, cultural, grammatical and dermatological impact of this aggression and address the issue by proposing a more peaceful approach which we term Generative Unadversarial Networks (GUNs)" But then of course, there is no social data in the paper at all,
3. The github is almost empty, with python scripts which generate a fake MNIST digits.
4. And have you look at the experimental section?

Seeing it as a joke, we lol after reading the "paper". Perhaps more hilarious to us is that some other sources treat this as a legit paper and treat it as "paper of the week"-type of the material.

That just teaches all of us a lesson: faked writing is everywhere these days. So always read the paper/sources before you share them. This says for AI/DL, perhaps it also says for everything you read.

[arxiv.org](https://arxiv.org/abs/1703.02528)

## Open Source

### [AudioSet: A sound vocabulary](https://research.google.com/audioset/index.html)

Google released another impressive dataset - this time is audio-centric. In case you don't know, noise detection is very painful for tasks such as speech recognition. And if you want to use a model-based approach to solve such problem, you need to have good negative training data such as noise or general sound events. AudioSet fills in this gap.

AudioSet is an effort stemmed from YouTube content analysis - which is perhaps the most difficult speech recognition task for humanity now. [Here](https://research.google.com/pubs/pub45857.html) is a link to the original ICASSP 2017 paper. Again, Kudo to Google. We think AudioSet is a very useful resource for practitioners in speech and audio processing.

[google.com](https://research.google.com/audioset/index.html)

---

### [FAISS](https://github.com/facebookresearch/faiss/blob/master/README.md)

According to Prof. [Yann LeCun](https://www.facebook.com/yann.lecun?fref=nf) FAISS is #1 in Github's "trending in open source" list of C++ projects (TensorFlow is #3). FAISS is a very fast implementation of nearest neighbor search for dense vector and can fully utilize system's memory.

[github.com](https://github.com/facebookresearch/faiss/blob/master/README.md)

## Video

[*[image not recovered: twenty_by_nine_extra_large_b385c524-12c9-40f9-aae9-f5259e97fcd5.png]*](https://www.youtube.com/watch?v=-O01G3tSYpU) 

### [A DARPA Perspective on Artificial Intelligence](https://www.youtube.com/watch?v=-O01G3tSYpU)

Here is an educational video from DARPA which explains concepts of A.I. I found it a rare gem, because it starts from the days before statistical learning is used (what Launchbury called the "First Wave". It also doesn't dumb down in explanation. For example, John Launchbury explain machine learning with the Manifold Hypothesis, which is the key to understand why neural network is so powerful. He also talks about the challenges of the current days technology ("Second Wave"). E.g. adversarial examples, how difficult it is to come up with a general intelligent conversational system, or bot. So check it out, it only takes around 20 mins to listen it through. Finally he briefly discuss what should be the future of A.I. from DARPA's perspective ("The Third Wave"), which he defines as combining huge amount of data with context data. 

[youtube.com](https://www.youtube.com/watch?v=-O01G3tSYpU)

## Member's Question

### Question from an AIDL Member

**Q.** (Rephrases from a question asked by [Flávio Schuindt](https://www.facebook.com/flavioschuindt?hc_location=ufi)) I've been studying classification problems with deep learning and now I can understand quite well it. Activation functions, regularizeres, cost functions, etc. Now, I think its time to step forward. What I am really trying to do now is enter in the deep learning image segmentation world. It's a more complicated problem than classification (object occlusion, lightning variations, etc). My first question is: How can I approach this king of problem? [...]

**A.** You do hit one of the toughest (but hot) problem in deep-learning-based image processing. Many people confuse problems such as image detection/segmentation with image classification. Here are some useful notes. 
1. First of all, have you watched [Karpathy's 2016 cs231n](http://cs231n.stanford.edu/)'s lecture 8 and 13? Those lectures should be your starting points to work on segmentation. Notice that image localization/detection/ segmentation are 3 different things. Localization and detection find bounding boxes and their techniques/concepts can be helpful on "instance segmentation". "Semantic segmentation" requires downsampling/upsampling architecture. (see below.)
2. Is your problem more a "semantic segmentation" problem of "instance segmentation" problem? (See cs231n's lecture 13) The former comes up with regions of different meaning, the latter comes up with instances.
3. Are you identifying something which always appear? If that's the case you don't have to use flunky detection technique, treat it as a localization problem and you can solve by Backprop a simple loss function (as described in cs231n lecture 8). If it might or might not appear, then a detection-type of pipeline might be necessary.
4. If you do need to use detection-type of pipeline. Does standard segment proposal techniques work for your domain? This is crucial, because at least the beginning of your segmentation research, you have to do find segment proposals.
5. Lastly if you decide this is really a semantic segmentation problem, then most likely your major task is to adopt an existing pre-train network. Very likely your goal is to transfer learning. Of course check out my point 2 and see if this is really the case.

Artificial Intelligence and Deep Learning Weekly
