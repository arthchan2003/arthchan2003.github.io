---
title: "AIDL Weekly Issue #68 - Dr. Rachel Thomas on AutoML and What ML Practitioners Actually do."
date: 2019-07-25
---

# AIDL Weekly Issue #68 - Dr. Rachel Thomas on AutoML and What ML Practitioners Actually do.

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 68 *July 30th 2018* ](http://aidl.io/issues/68/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week, we share with you the following: 
- Google's Edge TPU
- Dr Rachel Thomas' series on AutoML and what ML practitioners actually do
- A deeper look of the new connectomics work by Google

Enjoy!

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 162,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### [TPU on Edge](https://cloud.google.com/edge-tpu/)

After the success of the TPU, Google researchers decide to tape out a new chip which works on embedded device, or edge. As inference speed can be a bottleneck of many embedded devices, we expect Edge TPU will find lots of applications.

It is currently in the early access phase. If you are a developer, check it out.

[google.com](https://cloud.google.com/edge-tpu/)

## Blog Posts

### Dr. Rachel Thomas' Series on AutoML (and HumanML)

In AIDL Weekly, we usually share links from a range of sources. But this time we choose to share a series of links which are all written by Dr. Rachel Thomas at fast.ai. Reasons: First of all, Dr. Thomas covers what we ML practitioners care about - what do we really do? What are our daily activities? We found that this is an important yet not well-discussed topic. We are often asked how do we spend our time and why activities such as data cleaning and experimental design are part of our daily jobs. Dr. Thomas' Series Part I on "What do machine learning practitioners actually do?" answers all these question nice and clear. And it is suitable for all ML practitioners to read.

Second of all, Dr. Thomas dives into the what we called neural architecture search. Notable example of such search could be Google's AutoML. As you know, outlets have been sensationalizing how much AI can replace humans now. Dr. Thomas delve deep into the neural architecture search in "An Opinionated Introduction to AutoML and Neural Architecture Search" and she commented on AutoML in "Google's AutoML: Cutting Through the Hype". We found both pieces illuminating.

You can find the links here: 
- [Part 1 What do machine learning practitioners actually do?](http://www.fast.ai/2018/07/12/auto-ml-1/)
- [Part 2: An Opinionated Introduction to AutoML and Neural Architecture Search](http://www.fast.ai/2018/07/16/auto-ml2/)
- [Part 3: Google's AutoML: Cutting Through the Hype](http://www.fast.ai/2018/07/23/auto-ml-3/)

Artificial Intelligence and Deep Learning Weekly

---

### [Simple Object Tracking With OpenCV by Adrian Rosebrock](https://www.pyimagesearch.com/2018/07/23/simple-object-tracking-with-opencv/)

Here is another nice tutorial by Adrian Rosebrock. This time on object tracking. Adrian is detail-oriented and knowledgeable in computer vision. He starts from the basic principle of centroid tracking, then presents detail python code for implementation.

[pyimagesearch.com](https://www.pyimagesearch.com/2018/07/23/simple-object-tracking-with-opencv/)

---

### [Drive.ai's Simulation System](https://medium.com/@drive.ai/the-way-we-see-it-bd4458fc6809)

This week Drive.ai shares an incredibly cool link on how their on-board passenger display as well as simulation system works. One stunning number they share for any 1 hour of real driving data, it takes 800 hours to annotate it. That might explain the wide-spread use of simulation in SDC training.

[medium.com](https://medium.com/@drive.ai/the-way-we-see-it-bd4458fc6809)

---

### [Connectomics, Deep Learning and Google's work](https://ai.googleblog.com/2018/07/improving-connectomics-by-order-of.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+blogspot%2FgJZg+%28Google+AI+Blog%29)

This piece came out 2 weeks ago, but it is about a topic we care a lot - connectomics.

You ask: What is connectomes and its study, connectomics? Well. The brain can be thought the connection of neurons. Many believe that if we can trace and map out how these connections really look like, then we can truly understand the mysteries of the brain, such as how we have consciousness (or perceived notion of it), how we can higher level thinking even a lot of us don't intently train our own deep neural networks in our brain. ( :) ) This thinking follows from very early results from say [Hodgkin-Huxley model which describes the action-potential initiation and propagation within the neurons](https://en.wikipedia.org/wiki/Hodgkin%E2%80%93Huxley_model), in some sense, the belief that a physical (electrical model) could explain everything within the brain.

Anyhow, this is why connectomics, the study of these electrical wirings in the brain,is a big deal. But it is such difficult problem! Why? Just think about 1) how you acquire a brain you can study, 2) then get into the neural levels of structure of the brain, 3) then figure out how neurons are actually connected. There are many stories for the first two parts, but Google's work focus on 3. So for the sake of our discussion, we already get a slice of a brain. What we need to do is just to decide which part of is neurons from an image. This brings us to a familiar problem in deep learning - image segmentation.

If you delve into the [paper version of the work](https://www.biorxiv.org/content/early/2017/10/09/200675), you might notice that the idea of using Convnet in connectomic analysis is actually not new. So what did Google do? What the researcher found is this - usually when you apply Convnet the image segmentation in connectomics. First you use a Convnet to decide if a certain voxel (i.e. pixel) in a 3-d image is a boundary, then you use a separate algorithm to cluster all non-boundary voxel to segments. So they figure, could you make an all-in-one network for these two steps?

And they did, the result is what they called flood-filling network (FFN). Their results show that this new method works better than the past methods. Now one interesting thing though - they also found this all-in-one method could much longer run time than previous two stages method. According to the authors, that is because, 

> multiple and partially overlapping inference computations are required to segment both a single object as well as implement the sequential nature of multiple object segmentation.

Interesting to us and our readers. May be this open for some optimizations? Or did Googlers already do some optimization but want to publish a paper later on. We will see.

All-in-all, it's an interesting paper, so do check it out.

[googleblog.com](https://ai.googleblog.com/2018/07/improving-connectomics-by-order-of.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+blogspot%2FgJZg+%28Google+AI+Blog%29)

---

### [Google's Cirq](https://ai.googleblog.com/2018/07/announcing-cirq-open-source-framework.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+blogspot%2FgJZg+%28Google+AI+Blog%29)

We don't pretend we understand quantum computing and quantum machine learning. But if you want to learn more about [NISQ check out this Wikipedia link](https://quantumcomputing.stackexchange.com/questions/1885/what-is-meant-by-noisy-intermediate-scale-quantum-nisq-technology)? And [this editorial by Nathan Shammah's](https://medium.com/quantum-tech/nathans-quantum-tech-newsletter-10-1cb0e745b794) will give you a good summary on how open source software interact with quantum computing.

[googleblog.com](https://ai.googleblog.com/2018/07/announcing-cirq-open-source-framework.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+blogspot%2FgJZg+%28Google+AI+Blog%29)

## Paper/Thesis Review

### [Guide to Reading Machine Learning Research Papers](https://towardsdatascience.com/guide-to-reading-academic-research-papers-c69c21619de6)

Zubair Admed posts this gem at AIDL. The author Kyle M Shannon explains clearly on how you should read an academic paper, and we found his method illuminating.

One thing to add: some ideas such as back-propagation in neural networks, and EM in speech recognition are crucial to understand many ideas in literature. So do allocate more time to learn them before you move on to read difficult papers.

[towardsdatascience.com](https://towardsdatascience.com/guide-to-reading-academic-research-papers-c69c21619de6)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 163,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
