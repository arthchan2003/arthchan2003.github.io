---
title: "AIDL Weekly #38 - The FaceID Hack"
date: 2019-07-08
---

# AIDL Weekly #38 - The FaceID Hack

# [Issue 38 *November 17th 2017* ](http://aidl.io/issues/38/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Our main story this week is the FaceID hack. Is it a valid hack? How much should we care? We will take a closer look.

In other sections, we cover Karpathy's "Software 2.0", CheXnet and other topics.

---

Join our community for real-time discussions with this iOS app here: [https://itunes.apple.com/us/app/expertify/id969850760](http://apple.co/2z8Z7Qi)

As always, if you like our newsletters, feel free to subscribe and forward it to friends!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: original_ratio_extra_large_7aa23e59-e1a5-4049-919c-22398da2c1a7.png]*](https://goo.gl/uavZB7)

## News

### [The FaceID Hack](https://techcrunch.com/2017/11/13/apple-face-id-bkav-hack/)

We all learned last week, iPhoneX FaceID was purportedly hacked by a Vietnamese security company bkav. But then the more mainstream reports all suggest that we shouldn't be too worried about the hack. So let's take a closer look of the matter.

In this [Youtube video](https://www.youtube.com/watch?v=i4YQRLQVixM) shows a mask spoofing FaceID. The mask is a combination of a 3D mask with 2D printing of the eyes and the mouth. Later, Bkav also did a [live-demo with BBC](http://www.bbc.com/news/av/technology-41992610/face-id-iphone-x-hack-demoed-live-with-mask-by-bkav).

However, once you ask how one might this as an exploit, it's much tougher than it looks. First of all, Bkav refused to create a new mask after the request of BBC reporters. And according to the engineers who work on it, the whole process require 9 hours and the user has to be present so that the 2D+3D mask can be adjusted.

Another part which doesn't make sense is that Apple seemed to have tested FaceID extensively with masks as well. So, if Bkav refuses to replicate the process, it's hard to say definitively if FaceID is hackable.

[techcrunch.com](https://techcrunch.com/2017/11/13/apple-face-id-bkav-hack/)

## Blog Posts

### [Jensen Huang is Fortune 2017 Businessperson of the Year](https://blogs.nvidia.com/blog/2017/11/16/jensen-huang-fortune-2017-businessperson-of-the-year/?ncid=so-fac-nsfnjhsr-27025)

For his role as the leader of Nvidia and its impact of artificial intelligence and deep learning. Also see the fortune.com's [write up](http://fortune.com/2017/11/16/nvidia-ceo-jensen-huang/).

[nvidia.com](https://blogs.nvidia.com/blog/2017/11/16/jensen-huang-fortune-2017-businessperson-of-the-year/?ncid=so-fac-nsfnjhsr-27025)

---

### [Software 2.0 By Andrej Karpathy](https://medium.com/@karpathy/software-2-0-a64152b37c35)

Andrej Karpathy wrote a new piece on why neural network is actually the new software. Some question whether we really reach the point where DNN can just replace programming. That's a valid question, yet if you read the article closely, Karpathy was really arguing for using neural network as a skill to build several ML components such as ASR, CV and translation, which traditionally would require huge amount of programming effort, but now it can be significantly reduced by deep learning.

We think that Karpathy here is playing the role of futurist, much like some of his past articles, e.g. [Short Story on AI](http://karpathy.github.io/2015/11/14/ai/) in which he speculate how AI will look like when we scale up supervised learning.

[medium.com](https://medium.com/@karpathy/software-2-0-a64152b37c35)

---

### [How (and why) to create a good validation set by Rachel Thomas](http://www.fast.ai/2017/11/13/validation-sets/)

This is a new article by Prof. Rachel Thomas who discuss the how to create a good validation. She delves deeper than the usual "train-validation-test" set type of discussion, and ask when a random validation set might not work. We found it a thought-provoking piece.

[fast.ai](http://www.fast.ai/2017/11/13/validation-sets/)

---

### [CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning](https://stanfordmlgroup.github.io/projects/chexnet/)

This is a project from Stanford which shows that pneumonia detection can be done by deep learning in the level of radiologists.

The model is trained on the recently released ChestX-ray14 which has 14 types of diseases annotated for each of 110k images. The architecture is a 121-layer [Densenet](https://arxiv.org/abs/1608.06993). The authors show that CheXNet exceed the ability of human radiologists for both specificity and sensitivity. The original paper can be found [here](https://arxiv.org/pdf/1711.05225.pdf).

[github.io](https://stanfordmlgroup.github.io/projects/chexnet/)

## Open Source

### [Cornell NLVR dataset](http://lic.nlp.cornell.edu/nlvr/)

Here is a dataset opened by Cornell on using natural language to reason visually. There is a leaderboard as well.

[cornell.edu](http://lic.nlp.cornell.edu/nlvr/)

---

### [numpy is planning to drop python 2.7 support](https://github.com/numpy/numpy/blob/master/doc/neps/dropping-python2.7-proposal.rst)

As many deep learning scripts are using numpy, and many of you know that python library compatibility issues are really difficult to solve. So that's why numpy dropping 2.7 support is potentially a big issue for many projects and you deserve to know.

[github.com](https://github.com/numpy/numpy/blob/master/doc/neps/dropping-python2.7-proposal.rst)

## Video

### [Robot Learning 2017](https://www.youtube.com/watch?v=xfyK03MEZ9Q)

Here are the 8 hours feed of Robot Learning 2017 (RL 2017).

[youtube.com](https://www.youtube.com/watch?v=xfyK03MEZ9Q)

---

### [What's New, Atlas?](https://www.youtube.com/watch?v=fRj34o4hN4I)

Speaking about robotics, check out this super cool video from Boston Dynamics on the latest development of Atlas?

[youtube.com](https://www.youtube.com/watch?v=fRj34o4hN4I)
