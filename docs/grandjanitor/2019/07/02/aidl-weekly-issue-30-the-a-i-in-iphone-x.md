---
title: "AIDL Weekly Issue 30 - The A.I. in iPhone X"
date: 2019-07-02
---

# AIDL Weekly Issue 30 - The A.I. in iPhone X

# [Issue 30 *September 15th 2017* ](http://aidl.io/issues/30/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Perhaps the biggest AI news last week is the release of iPhone X, which now includes FaceID and A11 Bionic. We will take a closer look at the two technologies this week.

Other than that, we will also take a look of the interesting winning entry of 2017 Imagenet Squeeze and Excitation Network and the MILABOT in our paper review section.

---

As always, if you like our newsletter, feel free to subscribe and forward the letter to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## News

### [iPhone X and Artificial Intelligence](https://www.theverge.com/2017/9/13/16300464/apple-iphone-x-ai-neural-engine)

Apple released iPhone X last week, which critics billed it as the [future of smart phone](https://www.theverge.com/2017/9/12/16291244/new-iphone-x-photos-video-hands-on). Indeed, it is a beautiful device, a 5.8 inches OLED screen with 1125 x 2436 resolution (,which Apple called it "super retina display). It will cost a hefty $999, but it does give you a feeling that Apple is innovative again.

Of course, at the Weekly, what we mostly care is AI and deep learning. So what's new there? Perhaps the two features which are noteworthy are FaceID and A11 Bionic chips. Let's take a closer look?

*FaceID* : This is the new function which allows users to authenticate with their faces. Of course, there is an obvious issue about using face to authenticate - e.g. What if you face changes? According to [Apple](https://www.apple.com/iphone-x/), FaceID is supposed to adapt to your face over time.

Does it work? Oh well, it doesn't seem to work well at demo time on [Federighi's face](https://arstechnica.com/gadgets/2017/09/apple-says-face-id-didnt-actually-fail-during-its-iphone-x-event/). Apple's explanation is that because the phone was passed around so many times to different people off-stage, since FaceID tries to authenticate many people's faces without success, it ends-up require Federighi's passcode authentication. It does sound like a reasonable explanation.

*A11 Bionic Chip* : which also consists of new Neural Engine. We think the best piece is from [Mashable](http://mashable.com/2017/09/14/inside-apple-a11-bionic-and-silicon-team/#Qr3q2MRiiOqJ) which summarizes this "chip in the chip" well. The first thing to notice is that A11 Bionic was developed around 3 years ago. That was also the time we generally believe that Apple AI development was quiet. So such bet shows that Apple was serious about AI earlier than we thought.

Perhaps, as many critics said (as the Verge piece we quote), *A11 Bionic* suggests Apple is taking a very different approach to take on AI - rather than doing cloud-based processing just like Google and Amazon do, Apple's approach is edge-based. Such approach require control of the hardware stack and it's cost intensive. But you end-up have complete controls of your product and you don't need to rely external technologies (such as Nvidia GPU).

Corrections at 20170916 at 12:35 p.m.: The article previously states that "FaceID adapted to many different staffs' faces, but fail to respond to Federighi's. ", but the problem is not due to adaptation, but that Face ID actually trying to authenticate the other persons' faces, and after many failures, it requires passcode authentication. Thanks Jin Hon Tan to point it out.

[theverge.com](https://www.theverge.com/2017/9/13/16300464/apple-iphone-x-ai-neural-engine)

## Blog Posts

### [Open AI Gym Toolkit Website Closing Down](https://www.reddit.com/r/MachineLearning/comments/6zvlm2/d_openai_closing_down_gym_toolkit_website/)

One incredible resource from Open AI Gym is its toolkit website. Unfortunately, it was closed down without notice. That caused grieves to many RLers - many found invaluable insights on the leader board as well as write-up from different participants. The only reason we know so far is from [Greg Brockman on Twitter](https://twitter.com/gdb/status/907855318591438848) citing there is a lack of maintenance of the site.

Just like us, many RLer thinks it's sad to see the website, so many come forward to help maintenance. We hope the site can be live again as it is an invaluable resource for the community.

[reddit.com](https://www.reddit.com/r/MachineLearning/comments/6zvlm2/d_openai_closing_down_gym_toolkit_website/)

---

### [Third Quick Impression on deeplearning.ai's HODL](/grandjanitor/2017/09/11/my-third-quick-impression-on-hodl-interviews-with-pieter-abbeel-and-yuanqing-lin/)

Written by Arthur. This time mostly on Pieter Abbeel and Yuanqing Lin.

[thegrandjanitor.com](/grandjanitor/2017/09/11/my-third-quick-impression-on-hodl-interviews-with-pieter-abbeel-and-yuanqing-lin/)

---

### [Udacity introduces AI Challenger, a $300k Global AI Competition for Students](https://blog.udacity.com/2017/09/ai-challenger-global-ai-competition.html)

Udacity introduces a global AI competition for a $300k prize tag. One thing to note: it involves an sub-imagenet-scaled database for human skeletal system keypoints, which features 300k images across over 700k persons.

There are 5 tracks of the competition, details is still unknown to us but we will keep you posted.

[udacity.com](https://blog.udacity.com/2017/09/ai-challenger-global-ai-competition.html)

## Open Source

### [Tensorboard API](https://research.googleblog.com/2017/09/build-your-own-machine-learning.html)

Google just released the Tensorboard API which allows customization of its visualization capability. So far, it looks quite impressive. For example, the Beholder application showcased in the post can show live gradient information when the model is being trained.

[googleblog.com](https://research.googleblog.com/2017/09/build-your-own-machine-learning.html)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing)

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## Paper/Thesis Review

### [Imagenet 2017 winner: Squeeze and Excitation Network](https://arxiv.org/abs/1709.01507v1)

One work which caught our eyes is that the paper version of Imagenet 2017's winner is finally released. And we are talking about squeeze and excitation network, which gives ~25% relative improvement from the 2016 participants, which translates to absolute improvement from 2.95% to 2.25%.

So the first question is should we care about Imagenet after 2015? That's when all the big houses such as Google and Microsoft left the game. Our answer is yes. In fact, 25% of relative improvement is still an impressive improvement in machine learning. In speech recognition, for example, improvement of 15% relative of the state of the art is usually well sought by all sites.

Then the impressive part of the technique: it is more an add-on for a large class of transformation. So you can use it on many different architecture such as ResNet or Inception.

What is the essence of the technique? The authors use more obscure terms such as "squeeze" and "excitation" to describe their technique. Once you look closer though - it is actually a kind of attention models on channel information, similar to the spirit of the attention model found in seq2seq model's decoder. And just like other attention models, it can be trained end-to-end. The author then extends many of the existing architectures such as Resnet and Inception modules using S&E techniques which results in SE-Resnet and SE-Inception, which is how they got the better results.

It's a pity that the paper didn't get more attention (pun intended). But then that's the reality of large scale ML evaluation - once big houses left the game, the thrill is gone.

[arxiv.org](https://arxiv.org/abs/1709.01507v1)

---

### [A Deep Reinforcement Learning Chatbot](https://arxiv.org/abs/1709.02349v1)

When thinking of building bot, you may think of building a pure rule-based system or a pure seq2seq system, both won't work out well. You need to create some kind of glue code to combine several systems together. You can certainly code it manually. But more than often, a RL approach is used, and MILABOT is one such modern example. RL is used to select the right responses from an ensemble of models. The idea is not new, but the study's scale and scholarship are what caught our attention.

[arxiv.org](https://arxiv.org/abs/1709.02349v1)

- 

©2017-2019 Artificial Intelligence and Deep Learning Weekly | [Sponsorship](http://aidl.io/sponsorship/index.html)
