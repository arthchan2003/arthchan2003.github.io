---
title: "AIDL Weekly #13 - Special Issue on GTC 2017"
date: 2019-06-05
---

# AIDL Weekly #13 - Special Issue on GTC 2017

# [Issue 13 *May 12th 2017* ](http://aidl.io/issues/13/index.html#start)

## Editorial

### The Moat of Nvidia - Thoughts From Your Humble Curators

There are many tech conferences each year. But none impressed us as much as GTC 2017. We curated 4 pieces about the conference, but in this Editorial, we'd to explain the incredible moat of Nvidia. And, we think this moat is getting stronger. 

First, by "moat", we mean competitive advantage. So what's Nvidia's moat? Some of you might quickly point out its hardware platforms such as its GTX, Quadro and Teslas (or Pascal or Volta) series of GPU cards, and software platform, CUDA. Beyond the obvious IP and chip design moat, there is also powerful software lock-in. Indeed, as developers, we compile code with CUDA daily. CUDA is an easy to learn extension of C and is quick to produce results. The surrounding rich software support makes it easy to get up and running, and has high switching costs, once enough efforts has been spent on top of it.

But increasingly, Nvidia is branching out into new areas of computing, creating new moats. It just tripled its data center business in a [yoy basis](http://www.nasdaq.com/article/nvidia-nvda-q1-earnings-revenues-top-outlook-strong-cm787164). It has to do with the fact that they own both the hardware/software platform. And deep learning is not going anywhere soon.

Now, this moat is further strengthening in GTC 2017. Why? First, it announced that it is going to train 100k developers just this year, creating more potential customers steeped in their wares. This is a smart move - behaviors are hard to change. Secondly, they announced a new cloud platform initiative (curated under "Nvidia GPU Cloud"), which makes it easier for newcomers to start building on Nvidia's platform. Now, it remains to be seen what the competitive dynamics would be with other large cloud platforms like Google, Amazon, and Microsoft which are also Nvidia's customers. Nvidia might just see its own platform more as an educational platform and not necessarily a major revenue contributor like AWS long-term.

Currently, there are two potential competitors of Nvidia, one is AMD, but AMD is still struggling to come up with a new GPU to compete. Then there is a ASIC-platform, but most of them are still under development (Intel's Nervanna) or proprietary (Google's TPU). So virtually Nvidia is monopolizing the deep learning computing platform.

In this issue, we further analyze on Nvidia's training plan, the new V100, new partners on Drive PX and its Cloud move. We also cover Medical Imagenet and other news.

As always, if you like our letters, please subscribe and forward it to your colleagues!

Edit at 20170514: [Peter Morgan](https://www.facebook.com/peter1morgan) is kind enough to correct us - both Nervanna and TPU are based on ASIC, rather than FPGA. We have corrected the web version since.

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Collaborate fully](http://i.imgur.com/ds4FU08.gif) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter) 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Nvidia's Plan to Train 100000 Developers](https://venturebeat.com/2017/05/09/nvidia-plans-to-train-100000-developers-on-deep-learning-ai-in-2017/)

The first surprising announcements from GTC 2017 is Nvidia's plan to train 100k developers in 2017, which is around 10 times Nvidia's Deep Learning Institute (DLI) is training now. As on-line courses go, currently Nvidia's deep learning courses only occupy a very small space. On-line venues such as Coursera and EdX provides solid DL classes and you can count up to ~15 classes on that space. 

But Nvidia does has a distinct advantage - it is the home of all GPUs and with their move into the cloud space, they can provide learners/developers enough machines. This happens to be the weakness of a lot of on-line classes - because many beginning developers just don't have access of GPUs for their course work. Unfortunately, without GPU processing, some of the slightly difficult tasks in deep learning would take intractable amount of time to complete.

[venturebeat.com](https://venturebeat.com/2017/05/09/nvidia-plans-to-train-100000-developers-on-deep-learning-ai-in-2017/)

---

### [Nvidia GPU Cloud](http://nvidianews.nvidia.com/news/nvidia-launches-gpu-cloud-platform-to-simplify-ai-development)

Another stunning news from Nvidia during GTC2017 is its move into cloud computing. The product is currently dubbed as Nvidia GPU Cloud (NPC). As the [CNBC report](http://www.cnbc.com/2017/05/10/nvidia-to-compete-against-amazon-and-google-in-cloud.html) suggested Nvidia is not rebuilding the whole cloud data structure, rather they are building NPC but let other companies such as Amazon and Google to run it. 

The first question you should ask is whether this is a viable business model. If you think about the current cloud platform, while companies such as Amazon and Google control the cloud, not all of them (except Google) have the right hardware to attract developers to train deep learning models. So they are still partially relying on Nvidia to provide GPU on their platforms.

During NPC is developed, this situation is unlikely to change, in fact Nvidia would continue to have an advantage. Nvidia simply owns yet another layer of the computing platform - and this time on the lucrative cloud.

And you could see how the whole GTC 2017 play out and how Nvidia has a nice syndicated strategy - NPC will enjoy a nice customer base in 2017 - because we just learn that Nvidia is also going to train 100k members in its platform.

[nvidia.com](http://nvidianews.nvidia.com/news/nvidia-launches-gpu-cloud-platform-to-simplify-ai-development)

---

[*[image not recovered: twenty_by_nine_extra_large_d0b8a40d-b3ae-47ca-a969-6f076871374b.jpg]*](https://devblogs.nvidia.com/parallelforall/inside-volta/) 

### [Inside Volta](https://devblogs.nvidia.com/parallelforall/inside-volta/)

Finally, it is V100, an update of the Nvidia's most powerful line of GPU cards. Of course, the first thing you notice is that it is faster. But in what sense? And how real it is? For that, you only need to take a look of its speed of GEMM. 

What is GEMM? GEMM is a BLAS command, or GEneral Matrix to Matrix Multiplication. Computation such as back-propagation can mostly rewritten as a matrix and matrix multiplication computation. That's why GEMM is also thought as the [heart of deep learning](https://petewarden.com/2015/04/20/why-gemm-is-at-the-heart-of-deep-learning/).

From Nvidia's result, wow, V100 is not only 80% faster than P100 on F32 computation. It is around 8x faster when you use FP16 as inputs (!).

Btw, Caffe2 already support FP16 as input and you may look at how much speed gain by V100. We also curate one piece on how Facebook gain tremendous speed on machine translation using CNN, I believe they will keep this record next year if they also switch to FP16 calculation. The rest of the blog post has details on several amazing aspects of the GPU, so it deserves your time to take a quick look.

[nvidia.com](https://devblogs.nvidia.com/parallelforall/inside-volta/)

---

### [Toyota uses Nvidia Drive PX](https://venturebeat.com/2017/05/10/toyota-will-use-nvidias-drive-px-supercomputer-for-autonomous-vehicles/)

If you think Nvidia only sells high-end GPUs, think again. It also sells embedded platforms such [Tx2](http://www.nvidia.com/object/embedded-systems-dev-kits-modules.html) as well as car platforms such as [Drive PX](http://www.nvidia.com/object/drive-px.html). 

Of course, Drive PX focuses on self-driving, which is a growing robustly. Wired just curated a piece (see next item) on the top companies in the space. For years to come, Nvidia would enjoy another advantage from deep learning : SDC.

[venturebeat.com](https://venturebeat.com/2017/05/10/toyota-will-use-nvidias-drive-px-supercomputer-for-autonomous-vehicles/)

---

### [263 companies on SDC](https://www.wired.com/2017/05/mapped-top-263-companies-racing-toward-autonomous-cars/)

As we curate news on deep learning lately, we found that if there is 10 pieces of news a day, 3 of them are about self-driving car. Wired create a cool infographics which shows a whopping 263 companies in the space. It shows how much opportunity in the space. 

[wired.com](https://www.wired.com/2017/05/mapped-top-263-companies-racing-toward-autonomous-cars/)

## Blog Posts

### [FAIR's Novel Approach to Neural Machine Translation](https://code.facebook.com/posts/1978007565818999/a-novel-approach-to-neural-machine-translation/)

To understand Facebook's method of neural machine translation, you need to first understand how CNN and LSTM are really used in the industry. Obviously CNN is used in image classification and RNN/LSTM is used in time-series data such as SMT or text classification. Of course there are cross-overs. For example, CNN is sometimes used in text classification and RNN can be used in images. But those are more research-based systems or as an alternative models for model combination. 

So in what sense the two models are different then? One single word: speed. CNN is much more easy to parallelized. As a result it is much faster. Whereas LSTM always require calculation of previous time points, so it's harder to parallelize calculation on the whole time series. So LSTM in practice is usually one magnitude slower. That's why in fields such as speech recognition, ideas such as time difference neural network (TDNN) is emerging because it has much better parallelization property.

So back to Facebook, the amazing about this novel approach of SMT is that they are able to make *CNN* works in time data and the performance is actually better than using LSTM. To make the idea works, FAIR researchers have implemented a refined attention model, also known as multi-hop model, as well as a good gating mechanism. They achieve BLEU score which better previous LSTM systems. Because they are using CNN, they are also able to parallelize tremendously in both GPU and CPU platforms.

What this research taught us perhaps is that which architecture to use is less rigid than we thought - it's up to brilliant researchers to come up with a method which has the best accuracy/speed trade-off.

[facebook.com](https://code.facebook.com/posts/1978007565818999/a-novel-approach-to-neural-machine-translation/)

---

[*[image not recovered: twenty_by_nine_extra_large_fcd0d5ad-f581-46f2-abc3-92dfeab29e88.png]*](https://www.technologyreview.com/s/604332/mind-reading-algorithms-reconstruct-what-youre-seeing-using-brain-scan-data/) 

### [Mind Reading Algorithms through Deep Learning with fMRI.](https://www.technologyreview.com/s/604332/mind-reading-algorithms-reconstruct-what-youre-seeing-using-brain-scan-data/)

Here is a widely-circulated work on "mind-reading", or generally how one could re-generate original stimulus images based on the fMRI. The paper version can be found [here](https://arxiv.org/pdf/1704.07575.pdf). 

It is certainly a very interesting work on deep learning but the model has a component of graphical model (GM). So the deep learning is more on representation of perceived images and the GM part was fMRI activity patterns. If you look at the diagram, the proposed model, deep generative multiview model (DGMM) does produce much better images than previous methods.

(The top line is the original. While the bottommost line is generated by DGMM.)

[technologyreview.com](https://www.technologyreview.com/s/604332/mind-reading-algorithms-reconstruct-what-youre-seeing-using-brain-scan-data/)

## Open Source

### [Medical Image Net](http://langlotzlab.stanford.edu/projects/medical-image-net/)

As we reported in [Issue 12](http://aidl.io/issues/12#start), deep learning is permeating into the medical imaging domain. Of course, one of the bottlenecks in using deep learning is availability of large database. That makes Medical Image Net are huge deal. Currently the Langlotzlab is planning to collect from within/outside [Stanford Medicine](http://med.stanford.edu/). The [image database](http://langlotzlab.stanford.edu/imaging-datasets/) includes chess radiographs, tumor radiographs, mammographs, and 4.4 million Stanford exams. 

The lesser known about the database is that it also has a [NLP component](http://langlotzlab.stanford.edu/nlp-datasets/) that includes multiple types of medical reports which is invaluable for research such as automatic diagnostic.

If there is one news which worth 10 posts, I (Arthur) chose this one. The database is still under collection. But for years to come, the community will make much progress based on this work.

[stanford.edu](http://langlotzlab.stanford.edu/projects/medical-image-net/)

---

[*[image not recovered: twenty_by_nine_extra_large_04fa8b11-75f9-4af4-b8b0-307ea4631a8b.png]*](https://caffe2.ai/blog/2017/05/10/caffe2-adds-FP16-training-support.html) 

### [Caffe2 adds FP16](https://caffe2.ai/blog/2017/05/10/caffe2-adds-FP16-training-support.html)

Facebook just released FP16 support for Caffe2. FP16 is known to give higher throughput yet gives very similar accuracy as in FP32. The more interesting part is that it also support the very new NVidia V100. (Also in this Issue.) 

[caffe2.ai](https://caffe2.ai/blog/2017/05/10/caffe2-adds-FP16-training-support.html)

---

### [AIY Voice Kit](https://aiyprojects.withgoogle.com/)

Google and AIY Projects comes up with a DIY VoiceKit project based on [Raspberry Pi 3](https://www.adafruit.com/product/3055?gclid=CNGn2ubV5tMCFdeNswodQoUCMQ). If you take a look of the page, it only takes 12 components to build, voice recognition is based on Google Cloud Speech API. So this should be a great fun project for a weekend. 

[withgoogle.com](https://aiyprojects.withgoogle.com/)
