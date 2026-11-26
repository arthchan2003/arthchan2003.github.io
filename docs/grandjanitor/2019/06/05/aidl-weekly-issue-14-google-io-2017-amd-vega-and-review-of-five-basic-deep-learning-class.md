---
title: "AIDL Weekly Issue 14 - Google I/O 2017, AMD Vega and Review of Five Basic Deep Learning Class"
date: 2019-06-05
---

# AIDL Weekly Issue 14 - Google I/O 2017, AMD Vega and Review of Five Basic Deep Learning Class

# [Issue 14 *May 19th 2017* ](http://aidl.io/issues/14/index.html#start)

## Editorial

### The Two Battlefronts of Nvidia

This week, we cover Google I/O: TPU v2 is a monster, equivalent to 32 P100s. Then there is new free TPU research clusters, TensorFlow lite which is a package for easy TF development on embedded device, automatic search of network architecture. All the amazing features! 

Google could have taken quite a bit of attention away from Nvidia GTC by announcing TPU v2 last week, as The Next Platform's Nicole Hemsoth nicely put it: 

> > [......] we have to harken back to Google’s motto from so many years ago… “Don’t be evil.” Because let’s be honest, going public with this beast during the Volta unveil would have been…yes, evil.

In other news, AMD also announced a competing product, the Radeon RX Vega. However, AMD has been having a hard time against Nvidia due to software issues (more details in this issue) even when its specs are slightly better and the card is cheaper. This is the power of the software moat. Hardware commoditizes fast but software makes things sticky.

---

Other than Google I/O and AMD new GPU card, we also include several nice resources and links this week including: 
- Arthur's Review on Five Basic Deep Learning Classes
- Adit Despande's github on using Tensorflow.

As always, if you like our letter, feel free to [subscribe](http://aidl.io/) and forward it to your colleagues!! We also just reach 20000 members in our [AIDL forum](https://www.facebook.com/groups/DeepNetGroup/), so come join us!

Artificial Intelligence and Deep Learning Weekly

---

### A Correction on Issue #13 Editorial

About the Editorial of Issue 13: [Peter Morgan](https://www.facebook.com/peter1morgan) is kind enough to correct us - both Nervanna and TPU are based on ASIC, rather than FPGA. We have corrected the web version since. 

Artificial Intelligence and Deep Learning Weekly

## Sponsor

## News

### [Second Generation of TPU](https://www.nextplatform.com/2017/05/17/first-depth-look-googles-new-second-generation-tpu/)

Imagine this, [Nvidia P100](http://www.nvidia.com/object/tesla-p100.html) is probably the best GPU you can buy last year, you bought one, but realize there is yet another device which is as fast as 32 P100 combined! So here is TPU v2, a monster device quietly developed last 2 years and it's only released after v1's specification is opened. We chose the article from The Next Platform, because it has the best writeup. 

[nextplatform.com](https://www.nextplatform.com/2017/05/17/first-depth-look-googles-new-second-generation-tpu/)

---

### [Free Tensorflow Research Cloud with 1000 TPUs](https://research.googleblog.com/2017/05/introducing-tensorflow-research-cloud.html)

If you were Google, perhaps an important question you would ask is how to sell the powerful TPU. Google's natural strategy is cloud. The way they market and test the water is through opening 1000 TPUs to public. So here's the free sign-up links for everyone: not only researchers, but anyone who has computational need. 

It says a lot of Google's cloud strategy - TPU is an important differentiator between Google and its competitors such as Amazon and lately Nvidia. Google tends to think that inference will be where the cost/compute/power bottlenecks will be.

[googleblog.com](https://research.googleblog.com/2017/05/introducing-tensorflow-research-cloud.html)

---

### [Tensorflowlite](https://www.theverge.com/2017/5/17/15645908/google-ai-tensorflowlite-machine-learning-announcement-io-2017)

While Tensorflow is very versatile in building AI-based tools, it is also notoriously difficult to port its code to embedded platform. Tensorflowlite is going to change that. We don't have too much detail yet, but we expect convenience features, or utilities, which can quickly transform models onto Android. 

[theverge.com](https://www.theverge.com/2017/5/17/15645908/google-ai-tensorflowlite-machine-learning-announcement-io-2017)

---

[*[image not recovered: twenty_by_nine_extra_large_89d16b8e-9010-4185-8ef3-2410bbbc2e96.jpeg]*](http://hothardware.com/news/amd-radeon-rx-vega-unveiled-13-tflops-16gb-hbm2-4k60) 

### [AMD Radeon RX Vega](http://hothardware.com/news/amd-radeon-rx-vega-unveiled-13-tflops-16gb-hbm2-4k60)

In the last issue ([issue 13](http://aidl.io/issues/13#start)) , we argued that Nvidia has incredible moat on deep learning hardware. Here's AMD's counterstrike! And so far it looks respectable. The most noticeable feature is the 16G on-board memory. That's a new in the industry. 

Would AMD makes researchers switch? It's still hard to say, as we argued last issue, Nvidia has both hardware and software advantage. It's hard to move away from CUDA from existing development. Since many CUDA core libraries are close source, it's hard for AMD to come up with an equivalent architecture using say OpenCL.

[hothardware.com](http://hothardware.com/news/amd-radeon-rx-vega-unveiled-13-tflops-16gb-hbm2-4k60)

## Blog Posts

### [Learning Deep Learning: The "Basic Five" - Five Beginner Classes on Deep Learning](/grandjanitor/2017/05/13/learning-deep-learning-the-basic-five-five-beginner-course-on-deep-learning/)

One of us (Arthur) wrote an article of on five basic classes of deep learning. That includes some discussion on why these classes are important, what you can learn from them, and what you can do after taking the classes. The list includes, 
1. Andrew Ng's Coursera Machine Learning,
2. Fei-Fei Li and Andrew Karpathy's Convolutional Neural Networks for Visual Recognition or Stanford cs231n 2015/2016,
3. Richard Socher's Deep Learning and Natural Language Processing or Stanford cs224d,
4. David Silver's Reinforcement Learning,
5. Hinton's Neural Network and Machine Learning.

[thegrandjanitor.com](/grandjanitor/2017/05/13/learning-deep-learning-the-basic-five-five-beginner-course-on-deep-learning/) 

---

### [Google AutoML](https://research.googleblog.com/2017/05/using-machine-learning-to-explore.html)

Architecture search becomes more a respectable research. Perhaps an interesting results was [Zoph and Le](https://arxiv.org/abs/1611.01578) published last year - it comes up with state of the art results on CIFAR-10, which 0.09% more accurate and 5% faster. This is stunning because before most automatic tuning methods are slightly worse than human tuning. 

You can go into the details of how reinforcement learning is applied to such problem, but I want to point out one important trend here: architecture search is also applied on CIFAR-100, which usually requires one more order of computation. So if we continue to develop, the next target would be *Imagenet*. That would mean such search become a staple in all top research. You might find them in widespread use in the future.

[googleblog.com](https://research.googleblog.com/2017/05/using-machine-learning-to-explore.html)

## Open Source

### [Adit Despande's Github](https://github.com/adeshpande3/Tensorflow-Programs-and-Tutorials)

[Adit Despande](https://adeshpande3.github.io/) wrote several popular introductory blog posts in the space of deep learning in the past. The one which is the most memorable perhaps is "The 9 Deep Learning Papers You Need To Know About" ([Part 1](https://adeshpande3.github.io/adeshpande3.github.io/A-Beginner's-Guide-To-Understanding-Convolutional-Neural-Networks/), [Part 2](https://adeshpande3.github.io/adeshpande3.github.io/A-Beginner's-Guide-To-Understanding-Convolutional-Neural-Networks-Part-2/), [Part 3](https://adeshpande3.github.io/adeshpande3.github.io/The-9-Deep-Learning-Papers-You-Need-To-Know-About.html)). Recently, he also published a github about Tensorflow. The examples include GAN, RNN and CNN, which are more advanced variations of neural networks. 

[github.com](https://github.com/adeshpande3/Tensorflow-Programs-and-Tutorials)

---

### [Coarse Discourse dataset](https://research.googleblog.com/2017/05/coarse-discourse-dataset-for.html)

Google recent release the "Coarse" dataset - it's fairly interesting because it is the biggest dataset of online forum discussion, other the turns, there are also annotations on discourse types, which include announcement, question, answer, agreement, disagreement, appreciation, negative reaction, elaboration, and humor. That seems to be a very useful set if you want to do either conversation bot, or text classification type of applications. 

[googleblog.com](https://research.googleblog.com/2017/05/coarse-discourse-dataset-for.html)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing) 

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## Video

### [Google IO Playlist](https://www.youtube.com/playlist?list=PLOU2XLYxmsIKC8eODk_RNCWv3fBcLvMMy)

Here is the playlist for all Google IO 2017. 

[youtube.com](https://www.youtube.com/playlist?list=PLOU2XLYxmsIKC8eODk_RNCWv3fBcLvMMy)

## Member's Question

### Thought/Anecdote from a participant of GTC 2017

[Ajay Juneja](https://www.facebook.com/ajayjuneja) share this on AIDL: "Thoughts from the admin of the Self-Driving Car group this week (I attended the Nvidia Conference): 
1. Bi-LSTMs (Bi directional LSTMs) are everywhere, and working quite well. If you aren't using them yet, you really should. For those of us from the mechanical engineering world, think of them a bit like making closed-loop feedback control systems.
2. The convergence of AI, VR, AR, Simulation, and Autonomous Driving. It's happening. Need to generate good data for your neural nets, quickly? Build a realistic simulator using Unreal Engine or Unity, and work with gaming developers to do so. Want to make your VR and AR worlds more engaging? Add characters with personality and a witty voice assistant with emotion to them, while using cameras and audio to determine the emotional state of the players. Want to prototype a new car or building or surgery room? Build it in VR, create a simulator out of it. We need to cross pollinate these communities and have everyone working together :)
3. Toyota signed with Nvidia. That's 8 of 14 car companies... and they have signed the 2 largest ones (VW and Toyota). I hear rumblings from the AI community saying "If you want to build a self driving car TODAY, your choices are Nvidia and... nothing. What can I actually buy from Intel and Mobileye? Where are the engineers to support it? Qualcomm may have something for the 845 but they are drunk on mobile profits and again, no one knows their tools."

500K Nvidia Developers vs. next to nothing for Intel and Qualcomm's solutions. 

I believe Nvidia has its moat now."

Artificial Intelligence and Deep Learning Weekly

## About Us
