---
title: "AIDL Weekly #52 - AmoebaNet"
date: 2019-07-16
---

# AIDL Weekly #52 - AmoebaNet

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 52 *March 17th 2018* ](http://aidl.io/issues/52/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

The most interesting news this week is Google publishing new results from AutoML called AmoebaNet, we will take a look in the Literature Review section. 

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

This newsletter is a labor of love from us. All publishing costs and operating expenses are paid out of our pockets. If you like what we do, you can help defray our costs by sending a donation via [link](http://paypal.me/aidlio/9). For crypto enthusiasts, you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Atomwise Raised $45M Series A](https://techcrunch.com/2018/03/07/atomwise-which-uses-ai-to-improve-drug-discovery-raises-45m-series-a/)
- [Voci $8M Series B](https://www.bizjournals.com/pittsburgh/news/2018/03/12/cmu-spinoff-raises-8m.html) We are biased on this one - Voci is Arthur's long-time employer.

Artificial Intelligence and Deep Learning Weekly 

---

### [Tensorflow: the most loved framework. ](https://insights.stackoverflow.com/survey/2018/)

In SO's Developer Survey of 2018. Tensorflow is the most loved framework, Torch/PyTorch comes third. This survey includes all other non-DL frameworks as well. So it says something about DL's popularity. 

[stackoverflow.com](https://insights.stackoverflow.com/survey/2018/)

## Blog Posts

### [Google's DeepLab-v3+](https://research.googleblog.com/2018/03/semantic-image-segmentation-with.html)

Google is releasing the semantic image segmentation routine behind Pixel2. Semantic image segmentation is instrumental in Pixel's [motion stabilization routine](https://research.googleblog.com/2018/03/behind-motion-photos-technology-in.html). And all of these interesting technology can now be repeated by the public through DeepLab-v3+. The github comes with a demo which can do [inference](https://github.com/tensorflow/models/blob/master/research/deeplab/deeplab_demo.ipynb) right out of the box. 

[googleblog.com](https://research.googleblog.com/2018/03/semantic-image-segmentation-with.html)

---

### [Review of "Deep Learning for Computer Vision with Python"](http://www.zubairahmed.net/2018/03/13/review-of-deep-learning-for-computer-vision-with-python-starter-bundle/)

Here is a review written by one of the AIDL moderators, Zubair Ahmed on Rosebrook's "Review of Deep Learning For Computer Vision". 

[zubairahmed.net](http://www.zubairahmed.net/2018/03/13/review-of-deep-learning-for-computer-vision-with-python-starter-bundle/)

---

### [Unity's ML-Agents v0.3](https://blogs.unity3d.com/2018/03/15/ml-agents-v0-3-beta-released-imitation-learning-feedback-driven-features-and-more/)

It's much lesser known, but Unity's ML-Agents is getting their words out there as a new platform of reinforcement learning. v0.3 is a major update, which include behavior cloning as well as what the platform called multi-brain training. i.e. To train multiple agent at the same time. 

[unity3d.com](https://blogs.unity3d.com/2018/03/15/ml-agents-v0-3-beta-released-imitation-learning-feedback-driven-features-and-more/)

---

### [Challenges When Using Machine Learning in Genomic Data ](https://www.wired.com/story/can-machine-learning-find-medical-meaning-in-a-mess-of-genes/)

This Wired's interview with Prof. Barbara Engelhardt shed light on difficulties of applying ML on fields in biology. “We don’t have much ground truth in biology." as Engelhardt said. 

You can think the first issue is lack of labeled data which is the key of using techniques such as deep learning to provide a good performance. But then the deeper issue here is that traditionally scientific discovery requires a knowledgeable scientist, and who can teach natural science to machine?

It's not a surprise that the general consensus believe healthcare and biology is the new frontier of ML because there are still many problems to solve.

[wired.com](https://www.wired.com/story/can-machine-learning-find-medical-meaning-in-a-mess-of-genes/)

## Paper/Thesis Review

### [Regularized Evolution for Image Classifier Architecture Search](https://arxiv.org/pdf/1802.01548.pdf)

This is a read on "Regularized Evolution for Image Classifier Architecture Search" which is the paper version of AmoebaNet, the latest result in AutoML (Or this page: https://research.googleblog.com/2018/03/using-evolutionary-automl-to-discover.html) 
- If you recall, Google already has several results on how to use RL and evolution strategy (ES) to discover model architecture in the past. e.g. Nasnet is one of the examples.
- So what's new? The key idea is so-called regularized evolution strategy. What does it mean?
- Basically it is a tweak of the more standard tournament strategy, commonly used as the means of selecting individual out of a population. (https://en.wikipedia.org/wiki/Tournament_selection)
- Tournament is not too difficulty to describe: Choose random individuals from the population, then choose the best candidate according to certain optimizing criterion. You can also use a probabilistic scheme to decide whether to use the second or third best candidate. You might also think of it as throwing away the worst-N-candidate.
- The AutoML calls this original method by Miller and Goldberg (1995) as non-regularized evolution method.
- What is "regularized" then? Instead of throwing away the worst-N-candidates. The author proposed to throw away the oldest-trained candidate.
- Now you won't see a justification of why this method is better until the "Discussion" section. Okay, let's go with the authors' intended flow. As it turns the regularized method is better than non-regularized method. e.g. In CIFAR-10, the evolved model is ~10% relatively better either man-made model or NasNet. On Imagenet, it performs better than Squeeze-and-Excite Net as well as NasNet. (Squeenze-and-Excite Net is the ILSVRC 2017's winner.)
- One technicality when you read the paper is the G-X dataset, they are actually the gray-scale version the normal X data. e.g. G-CIFAR-10 is the gray-scale version of CIFAR-10. The intention of why the authors do it are probably two folds: 1) to scale the problem down, 2) to avoid overfitting to only the standard testsets of the problems.
- Now, these are all great. But how come the "regularized" approach is better then? How would the authors explain it?
- We don't want to come up with a hypothesis. So let us just quote the last paragraph here: "Under regularized evolution, all models have a short lifespan. Yet, populations improve over longer timescales (Figures 1d, 2c,d, 3a–c). This requires that its surviving lineages remain good through the generations. This, in turn, demands that the inherited architectures retrain well (since we always train from scratch, the weights are not heritable). On the other hand, non-regularized tournament selection allows models to live infinitely long, so a population can improve simply by accumulating high-accuracy models. Unfortunately, these models may have reached their high accuracy by luck during the noisy training process. In summary, only the regularized form requires that the architectures remain good after they are retrained."
- And also: "Whether this mechanism is responsible for the observed superiority of regularization is [a] conjecture. We leave its verification to future work."

[arxiv.org](https://arxiv.org/pdf/1802.01548.pdf) 

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 110,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760 

Artificial Intelligence and Deep Learning Weekly
