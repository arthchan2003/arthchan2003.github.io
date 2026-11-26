---
title: "AIDL Weekly #39 - Amazon The AI Powerhouse"
date: 2019-07-08
---

# AIDL Weekly #39 - Amazon The AI Powerhouse

# [Issue 39 *December 1st 2017* ](http://aidl.io/issues/39/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Its AWS re:INVENT week - this is the big annual AWS conference. Amazon had several announcements on its AI offerings. So we will take a closer look in this Issue.

In our Blogs Posts section, we have a line-up of many interesting blog posts and paper reviews this issue, including: 
- Google Vision AIY Kit,
- Stephen Merity on Understanding the Mixture of Softmaxes (MoS),
- One LEGO at a time: Explaining the Math of How Neural Networks Learn,
- Arthur's Review of Course 3 of deeplearning.ai

We also present our read on the CheXnet paper which alleged beat human radiologists. We are taking a closer look of the results.

---

Join our community for real-time discussions with this iOS app here: [https://itunes.apple.com/us/app/expertify/id969850760](http://apple.co/2z8Z7Qi)

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## News

### [AI Powerhouse: Amazon](https://www.theverge.com/2017/11/29/16715688/amazon-ai-camera-developer-enterprise-tools)

Verge ran a piece on Amazon DeepLens, a $250 AI-enabled camera, also SageMaker, an automatic transcription and translation tools. Of course, you might also heard of [Rekognition](https://techcrunch.com/2017/11/29/amazon-rekognition-video-gives-developers-access-to-real-time-video-analysis/) which now gives developers access of powerful readily-made feature such as real-time video analysis. In a nutshell, you don't have to implement YOLO yourself.

[theverge.com](https://www.theverge.com/2017/11/29/16715688/amazon-ai-camera-developer-enterprise-tools)

## Blog Posts

### [Google AIY Vision Kit](https://www.blog.google/topics/machine-learning/introducing-aiy-vision-kit-make-devices-see/)

After the Voice AIY toolkit, Google will release a new Vision AIY toolkit. You will need your own [Raspberry Pi Zero](https://www.raspberrypi.org/products/raspberry-pi-zero/), and Raspberry Camera. But the toolkit will come with VisionBonnet which has a [Intel Movidius MA2450](https://www.movidius.com/solutions/vision-processing-unit) vision processing unit.

Price: only $45. It sounds like we can all have some fun Christmas time then.

[blog.google](https://www.blog.google/topics/machine-learning/introducing-aiy-vision-kit-make-devices-see/)

---

### [Understanding the Mixture of Softmaxes (MoS)](http://smerity.com/articles/2017/mixture_of_softmaxes.html)

In this piece, our favorite writer Stephen Merity tries to explain the latest ideas of mixture of softmaxes in language modeling by Zhilin Yang, Zihang Dai, Ruslan Salakhutdinov, and William W. Cohen. As always, Merity is a quality writer and he also provided source code for you to play with.

[smerity.com](http://smerity.com/articles/2017/mixture_of_softmaxes.html)

---

### [One LEGO at a time: Explaining the Math of How Neural Networks Learn](https://omar-florez.github.io/scratch_mlp/)

A great beginner's article on back-propagation. One aspect is covered which is less well-discussed is the modularity aspect of the algorithm.

[github.io](https://omar-florez.github.io/scratch_mlp/)

---

### [A Year After Pledging Openness, Apple Still Falls Behind On AI](https://www.buzzfeed.com/daveyalba/apple-artificial-intellgence-race?utm_term=.ufbOvR81P#.yivx2P0Ea)

This is a more critical piece on Apple's current deep learning research. At least, in AIDL, members are divided on the merit of Apple's research. Check it out at this [thread](https://www.facebook.com/groups/DeepNetGroup/permalink/530581724001381/)?

[buzzfeed.com](https://www.buzzfeed.com/daveyalba/apple-artificial-intellgence-race?utm_term=.ufbOvR81P#.yivx2P0Ea)

---

### [How does Boston Dynamics' Robots work?](https://twitter.com/dennybritz/status/934665343162814464)

In this interesting conversation started by Denny Britz, he quoted [Eric Jang's speculation on Quora](https://www.quora.com/What-kind-of-learning-algorithms-are-used-on-Boston-Dynamics-robots) on how BD's backfliping robot actually work, in which he suggest that BD is not using ML in the process.

That leads to a conversation on how/when ML would really able to learn this process automatically, and Prof Pieter Abbeel chimed in.

[twitter.com](https://twitter.com/dennybritz/status/934665343162814464)

---

### [Arthur's Full Review of deeplearning.ai Course 3: Structuring Machine Learning Projects](/grandjanitor/2017/11/25/review-of-ngs-deeplearning-ai-course-3-structuring-machine-learning-projects/)

This is Arthur's review on Course 3 of deeplearning.ai. He argues that this is perhaps the most important course within the specialization. See more on why in the text.

[thegrandjanitor.com](/grandjanitor/2017/11/25/review-of-ngs-deeplearning-ai-course-3-structuring-machine-learning-projects/)

## Open Source

### [Nilearn](http://nilearn.github.io/whats_new.html)

Nilearn is a scikit-learn-based toolkit for fast processing of neuroimaging data.

[github.io](http://nilearn.github.io/whats_new.html)

---

### [Open Images V3](https://github.com/openimages/dataset)

OpenImages is now at V3, with 9 million URLS and 4.5 anchor boxes.

[github.com](https://github.com/openimages/dataset)

## Member's Question

### Are MOOC Certificates Important?

Our thought (from Arthur): For the most part, MOOC certificates don't mean too much in real life. It is whether you can actually solve problem matters. So the meaning of MOOC is really there to stimulate you to learn. And certificate serves as a motivation tool.

As for OP's question. I never got the Udacity nanodegree. From what I heard though, I will say the nanodegree will require effort to take 1 to 2 Ng's deeplearning.ai specialization. It's also tougher if you need to take a course in a specified period of time. But the upside is there are human graders that give you feedback.

As for which path to go, I think it solely depends on your finances. Let's push to an extreme: e.g. If you purely think of credential and opportunities, perhaps an actual PhD/Master degree will give you the most, but then the downside is multi-year salary opportunity costs. One tier down would be online ML degree from Georgia tech, but it will still cost you up to $5k. Then there is taking cs231n or cs224d from Stanford online, again that will cost you $4k/class. So that's why you would consider to take MOOC. And as I said which price tag you choose depends on how motivate you are and how much feedbacks you want to get.

Artificial Intelligence and Deep Learning Weekly

## Paper/Thesis Review

### [Nature ML Journal Launching in 2017](https://www.nature.com/natmachintell/)

It's online, but will it be free? We will see. Regardless, it says a lot of the importance of ML in scientific research. Though some in the community does raise concern if Nature is the best host of the new journal. Some use JMLR as an [example](https://twitter.com/yaringal/status/935141418833797120) that an academic journal could just be organized and edited by academicians themselves.

[nature.com](https://www.nature.com/natmachintell/)

---

### [CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning](https://arxiv.org/abs/1711.05225)

This is a note on CheXNet, the paper. As you know it is the widely circulated paper from Stanford, purportedly outperform human's performance on Chest X-ray diagnostic. 
- BUT, after we read it in detail, my impression is slightly different from just reading the popular news including the description on github.
- Since the ML part is not very interesting. We will just briefly go through it - it's a 121-layer Densenet, basically it means there are feed-forward connection from every previous layers. Given the data size, it's likely a full training.
- There was not much justification on the why of the architecture. Our guess: the team first transfer learning, but decide to move on to full-training to get better performance. A manageable setup would be Densenet.
- Then there was fairly standard experimental comparison using AUC. In a nut shell, CheXNet did perform better than humans in every one of the 14 classes of ChestX-ray-14, which is known to be the largest of the similar databases.
- Now here is the caveat popular news hadn't mentioned: 1, First of all, humans weren't allow to access previous medical records of a patient. 2, Only frontal images were shown to human doctors. But prior work did show when the lateral view was also shown.
- That's why on p.3 of the article, the authors note: "We thus expect that this setup provides a conservative estimate of human radiologist performance."

Reading so far should make you realize that may be it will still take a bit for deep learning to "replace radiologists".

See the original discussion at [AIDL-LD](https://www.facebook.com/groups/aidl.ld/permalink/909061255925208/).

[arxiv.org](https://arxiv.org/abs/1711.05225)
