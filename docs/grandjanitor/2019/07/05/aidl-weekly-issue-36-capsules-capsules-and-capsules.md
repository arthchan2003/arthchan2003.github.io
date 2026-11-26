---
title: "AIDL Weekly Issue 36 - Capsules, Capsules and Capsules"
date: 2019-07-05
---

# AIDL Weekly Issue 36 - Capsules, Capsules and Capsules

# [Issue 36 *November 5th 2017* ](http://aidl.io/issues/36/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We were out last week. The hottest news this week is all about Prof. Hinton's capsule models! 

Prof. Hinton and students just released an arxiv paper on how the idea of capsule can be used and specifically how it can outperform MNIST as well as its more difficult cousins, affMNIST and MultiMNIST, which had distorted MNIST with affined transform and heavy overlapping. So we dedicate this issue on capsules. We provide our own analysis in the thesis/paper review section, highlight a popular link from Wired, and cover the latest developments. So far, we already know of two implementations which attempt to repeat the result.

Other than that, check out other interesting links such as ex-Google Brain Resident David Ha's work on evolution strategy, and our piece on "Unsupervised Machine Translation Using Monolingual Corpora".

---

**Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

As always, if you like our newsletter, feel free to subscribe/share the letter to your colleagues.

We will host our own show at the [AI World events: "Attack of the AI Startups"](https://www.meetup.com/Boston-AIDL-Meetup/events/243474567/). If you live in the New England area, feel free to join!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Attack of the AI Startups ](https://aiworld.com/sessions/mlai/)

We will be hosting an AIDL Meetup at the AI World Conference in Boston on Dec 12 at 6:15pm where some cutting-edge AI companies will present. We got FREE tickets for you all! Come join us in person if you can!! 

Attack of the AI Startups - https://aiworld.com/sessions/mlai/ at AI World - aiworld.com

All attendees need to register to attend. To register, please go to: https://aiworld.com/live-registration/ To receive your FREE expo pass (thru Nov 15), use priority code: AIWMLAIX

To receive a $200 discount off of your 1, 2 or 3 day VIP conference pass, use priority code: AIWMLAI200

AI World is the industry's largest independent event focused on the state of the practice of enterprise AI and machine learning. AI World is designed to help business and technology executives cut through the hype, and learn how advanced intelligent technologies are being successfully deployed to build competitive advantage, drive new business opportunities, reduce costs and accelerate innovation efforts.

The 3–day conference and expo brings together the entire applied AI ecosystem, including innovative enterprises, industry thought leaders, startups, investors, developers, independent researchers and leading solution providers. Join 100+ speakers and 75+ sponsors and exhibitors and thousands of attendees. Other than that, we also include some of our analyses on two paper as well as multiple interesting links for blogs and open source resources. So check it out!

As always, if you like our newsletter, subscribe/forward it to your colleagues!

[aiworld.com](https://aiworld.com/sessions/mlai/)

---

## News

### [Sony AIBO is back! And Powered by Deep Learning!](https://www.theverge.com/circuitbreaker/2017/10/31/16588878/sony-aibo-2017-announced-price-release-date)

Deep learning is revitalizing one of the most iconic product: Sony AIBO. The new AIBO, priced at ~$1730, will have sensors and run deep learning algorithm to recognize images and sounds. 

[theverge.com](https://www.theverge.com/circuitbreaker/2017/10/31/16588878/sony-aibo-2017-announced-price-release-date)

---

### [Course 4 of deeplearning.ai is here!](https://www.coursera.org/learn/convolutional-neural-networks)

Alright, ML nerds, Course 4 of deeplearning.ai is finally here! Course 4 looks good. It's all about image classification with Convnet, object detection and fun exercises such as transfer learning and face verification. 

[coursera.org](https://www.coursera.org/learn/convolutional-neural-networks)

---

### [Wired's Coverage of Hinton's Capsules Theory](https://www.wired.com/story/googles-ai-wizard-unveils-a-new-twist-on-neural-networks/)

Here is a more popular account of Prof. Hinton's capsules theory. Notice that Wired assume the OpenReview paper is from students and Hinton as well. But at this point we really don't have any confirmation yet. 

[wired.com](https://www.wired.com/story/googles-ai-wizard-unveils-a-new-twist-on-neural-networks/)

## Blog Posts

[*[image not recovered: twenty_by_nine_extra_large_f6a574fe-daef-466a-af49-734d4c7154ab.png]*](http://research.nvidia.com/publication/2017-10_Progressive-Growing-of) 

### [Nvidia's Progressive Growing of GAN](http://research.nvidia.com/publication/2017-10_Progressive-Growing-of)

Here is one very impressive results you probably saw last week - GAN is now able to generate very realistic celebrity images (trained using the CelebA-HQ database). So how does it work? 

Turns out it has a lot to do how the training is done. The authors start with using a GAN with both generator and discriminator with only 4 units. The training then progressively doubles the size of units and eventually increasing it to 1024 units. Doing so, the authors claims, helps to generate fine details.

What else is in the recipe? There are two we spotted: 
1. The authors used facial landmarks to crop an image in the CelebA-HQ dataset.
2. Then the various normalization scheme

[nvidia.com](http://research.nvidia.com/publication/2017-10_Progressive-Growing-of)

---

### [The State of ML and Data Science Report from Kaggle](https://www.kaggle.com/surveys/2017)

This is a great survey by Kaggle on data scientists and ML experts. What is their demographics? What tool do they use? And what is their most favorite machine learning algorithm? They are all answered in the report. 

[kaggle.com](https://www.kaggle.com/surveys/2017)

---

### [A Visual Guide to Evolution Strategies](http://blog.otoro.net/2017/10/29/visual-evolution-strategies/)

We often learned a lot just by reading what Google Resident David Ha share in his Facebook and LinkedIn feed. He has impressive experience in different sub-fields of machine learning. His seemingly casual experiments on reinforcement learning is one of the most interesting to read and understand. 

This time, David himself wrote an extensive guide on evolution strategies, which compares various methods such as genetic algorithm (GA), covariance matrix adaptation evolution strategy (CMA-ES), REINFORCE and even OpenAI [latest strategy](https://blog.openai.com/evolution-strategies/). It's certainly eye-opening for us. As in many of David's work: code is released. So Enjoy!

[otoro.net](http://blog.otoro.net/2017/10/29/visual-evolution-strategies/)

---

### [Arthur's Full Review of deeplearning.ai Course 2](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/)

Here is Arthur's review of deeplearning.ai Course 2. This time he focus on why learning the details of deep learning could be a good thing for beginners of DL. 

[thegrandjanitor.com](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/)

## Open Source

### [Implementation of CapsNet](https://github.com/naturomics/CapsNet-Tensorflow)

Here is one of the first implementations which attempts to reimplement CapsNet. 

[github.com](https://github.com/naturomics/CapsNet-Tensorflow)

---

### [A PyTorch Implementation](https://github.com/timomernick/pytorch-capsule)

And here is a PyTorch implementation. 

[github.com](https://github.com/timomernick/pytorch-capsule)

## Paper/Thesis Review

### [What We Know About Capsules So Far](https://www.facebook.com/groups/aidl.ld/permalink/896377267193607/)

We wrote the previous piece on Monday on our [Literature Discussion](https://www.facebook.com/groups/aidl.ld/) group. But then it triggered very interesting discussion which we learnt couple of things: 
1. Hinton and students might have published another paper on ICLR 2018. It's very likely to involve EM as the routing mechanism.
2. There are already two available implementations of CapsNet. (See the Implementation Section.)

[facebook.com](https://www.facebook.com/groups/aidl.ld/permalink/896377267193607/) 

---

### [Capsules](https://arxiv.org/abs/1710.09829v1)

This is the Hinton's new invention of capsules algorithm. Here is a write up: It's TL;DR but we doubt we completely grok the idea anyway. 
- The first mention of "capsule" is perhaps in the paper ["Transforming Auto-encoders"](http://www.cs.toronto.edu/~fritz/absps/transauto6.pdf) which Hinton and students coauthored.
- It's important to understand what capsules try to solve before you delve into the details. If you look at Hinton's papers and talks, capsule is really an idea which improve upon Convnet. Hinton has two major complaints.
- First, the general settings of Convnet assumes that one filter is being used across different locations. This is also known as "location invariance". In this setting, the exact location of a feature doesn't matter. That has a lot to do with robust feature parameter estimation. It also drastically simplify backprop with weight sharing.
- But then location invariance also removes one important information of an image: the apparent location.
- Second assumption is max pooling. As you know, pooling usually removes a high percentage of information from the previous layer. In early architectures, usually pooling is the key to shrink the size of a representation down. Of course, later architectures had changed. But pooling is still an important component.
- So the design of capsule has a lot of do to tackle problems of max pooling: Instead of losing information, can we "route" pixel values from previous layer correctly so that they are in optimal use?
- Generally "capsule" represents a certain entity of an image, "such as pose (position, size, orientation), deformation, velocity, albedo, hue, texture etc". Notice that they are not hard-wired and automatically discovered.
- Then there is how the low level information can "route" to higher level. The mechanism is intriguing in this current implementation:
- First, your goal is to calculate a softmax in the form of exp(b*{ij} / Sum_k exp(b*{ik} where b\_{ij} is the output of lower level capsule i to a higher level capsule j. This is something you can train.
- Then what you do is iteratively estimate b\_{ij}. This appears in Procedure 1. The 4 steps are: a, calculate the softmax weight b. b, compute the prediction vector from a capsule i, then form a weighted sum, c, squash the weighted sum d, update softmax weight b based on the squash value and weighted sum.
- So why the squash function, our guess is it is to normalize the value computed in b. According to Hinton, a good function is v_j = |s_j|^2 / (1 + |s_j|^2) \* s_j / |s_j|
- The rest of the architecture actually looks very much like a Convnet. The first layer was a Convnet with ReLU activation.
- Would this work? The authors say yes. Not only it reaches the state of art benchmark of MNIST. It can also tackle more difficult tasks such as CIFAR-10, SVNH. In fact, the authors found that in both task they already achieve better results when first Convnet was first used to tackle these tasks.
- It also works well for two tasks called affMNISt and multiMNIST. First is MNIST go through affine transform, second is MNIST regenerated with many overlappings. This is quite impressive, because you will need to use much data augmentation and effort of object detection to get these cases working.
- The part, we have some doubts - is this model more complex than convnet? It's possible that we are just fitting a more complex model to get better results.
- Nice thing about the implementation: it's in Tensorflow, so we can play with it in the near future. Have fun!

[arxiv.org](https://arxiv.org/abs/1710.09829v1) 

---

### [Unsupervised Machine Translation Using Monolingual Corpora ](https://arxiv.org/abs/1711.00043)

This is an impressive paper by FAIR authors which claims that one only need to use monolingual corpora to train a usable translation model. So how does it work? Here are some notes. 
- For starter, indeed you don't need to use a parallel corpora, but you still need a bidirectional dictionary to generate translation. You also need to have monolingual corpora in both languages. That's why the title is about monolingual corpora (plural) but not monolingual corpus (singular).
- Then, there is the issue of how you actually create translation. It's actually much simpler than you thought, first imagine there is a latent language which both your source and target languages mapped to.
- How do you train? So let's just use the source language as an example first. What you can do is create an encoder-decoder architecture which translate your source to the latent space, then translate it back. Using BLEU score, you can then setup an optimization criteria.
- Now this doesn't quite do the translation. Now you apply the same procedure on both source and target language. Don't you now have a common latent space? One you train up such common latent subspace, in actual translation, what you need to do is to first map the target language in the common latent space, then map it back to the source language.
- Many of you might recognize that such encoder-decoder scheme which map the language to itself as very similar to autoencoder. Indeed, the authors in the paper actually use a version of autoencoder: [denoising autoencoder(dA)](http://deeplearning.net/tutorial/dA.html) to train the model.
- The final interesting idea I spot is to idea of iterative training. In this case, you can imagine that you can first train an initial translator, but then use its output as the truth and retrain another one. The authors found tremendous gain in BLEU score in the process.
- The results are stunning if you consider no parallel corpus is involved. BLEU score is around 10 points lower, but do remember: deep learning has pretty much improved BLEU scores by absolute 7-8 points anyway from the classical phrased based translation models.

Member Ben Davis also wrote a fairly good summary for the paper. Check it in our [thread](https://www.facebook.com/groups/aidl.ld/permalink/897911800373487/)? 

[arxiv.org](https://arxiv.org/abs/1711.00043)
