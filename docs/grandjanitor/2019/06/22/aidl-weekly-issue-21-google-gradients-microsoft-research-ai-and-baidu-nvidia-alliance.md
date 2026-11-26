---
title: "AIDL Weekly Issue #21 - Google Gradients, Microsoft Research AI and Baidu-Nvidia Alliance"
date: 2019-06-22
---

# AIDL Weekly Issue #21 - Google Gradients, Microsoft Research AI and Baidu-Nvidia Alliance

[Issue 21 *July 14th 2017* ](http://aidl.io/issues/21/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week, we learn about Gradient Ventures, MS new research (MSRAI) initiative and Nvidia-Baidu Alliance.

On the technical side, we discuss Google's paper which revisit "Unreasonable Effectiveness of Data", learn more about how the funny stick-man MuJoCo humanoids learn to walk with DeepMind's reinforcement learning. And finally there are two articles from Arthur on the differences between deep and machine learning, as well as fact-checking whether "post-quantum computing" has anything to do with consciousness.

---

As always, if you like our letter, subscribe and forward it to your friends/colleagues!

Artificial Intelligence and Deep Learning Weekly

## News

### [Google's Gradient Ventures](https://www.blog.google/topics/machine-learning/introducing-gradient-ventures/)

Google started a new VC firm, called Gradient Ventures. So what's interesting about the firm (beside the relevant, great name) ?

If you take a look at the list of [Founding Partners and Advisors](https://gradient.google/team), most of them are engineers. On the advisor front, you find Prof. Daphne Koller and Dr. Peter Norvig, both of whom are famous in teaching AI/ML classes. So Gradient's structure is very different from traditional fund which mostly run by career VCs.

The goal of Gradient is also fairly interesting. As reported by [CNBS news](http://www.cnbc.com/2017/07/10/google-launches-gradient-ventures-to-invest-in-a-i-start-ups.html), sometimes Google would put Google engineers into the startup to help out a project, and there are explicit rule to disallow them to bring back any IP back to Google. Another perk is that startup could access the vast amount of data accumulated by Google if they got invested by Gradient. That gives an extra edge for both the startups and Google.

We think this could be a boon to the A.I. startup ecosystem as there are few companies in the world who know the space better. That said, we can't help but be skeptical about Google's motive here - how this can be anything but a funnel for Google acquisitions or a funnel for figuring out where Google to apply its A.I. prowess next. Recall that Google invested in Uber too before deciding to compete with it. So, startups, do your due diligence.

[blog.google](https://www.blog.google/topics/machine-learning/introducing-gradient-ventures/)

---

### [Microsoft Research AI](https://techcrunch.com/2017/07/12/microsoft-creates-an-ai-research-lab-to-challenge-google-and-deepmind/)

As we learned this week, MS is pushing forward Microsoft Research AI (MSRAI) This is clearly a measure to counter research labs such as Google's Brain and DeepMind, Facebook's FAIR and OpenAI. Microsoft already owns one research company with similar style - [Maluuba](http://www.maluuba.com/). So, what does MRAI offer that's different?

The first thing to notice is Microsoft Research (MSR) has always been a strong contender in AI and ML in the first place. Most notable is that they are one of the few groups come up with a deep-learning-based speech recognition system. MS' aim perhaps is to create a specialized task force, with the scale larger than a single research department, on the field of AI/ML/DL. MSRAI seems to be the case.

Perhaps another differentiator of MSRAI: Once you look at the other five companies we mentioned - all of them focused on artificial *special* intelligence. Whereas MSRAI's effort seems to focus on the *general* intelligence, the holy grail of our field. So the type of collaboration MSRAI is involved in is also different from other sites. e.g. She is working with [MIT’s Center for Brains, Minds and Machines](https://cbmm.mit.edu/).

[techcrunch.com](https://techcrunch.com/2017/07/12/microsoft-creates-an-ai-research-lab-to-challenge-google-and-deepmind/)

---

### [Baidu-Nvidia Alliance](https://insidehpc.com/2017/07/nvidia-baidu-partner-accelerate-ai/?_lrsc=bab68be6-feaa-47c6-9d3f-c2a610715def&ncid=so-lin-lt-798)

On the news of AI alliance, perhaps we should talk about the Baidu-Nvidia Alliance happened around a week ago. As we knew, both companies are important players in deep learning. Nvidia dominates in terms of deep learning hardware, and we all know Baidu is the "Google of China". So their alliance is very significant.

Three important gists about the deal. 
- Baidu will adopt [Nvidia Volta](https://www.nvidia.com/en-us/data-center/volta-gpu-architecture/) in large scale on its cloud platform.
- Baidu will pick up [Nvidia PX](http://www.nvidia.com/object/drive-px.html) on its self-driving car initiative. In China, Baidu certainly has advantage.
- Nvidia, on the other hand, will help optimize Baidu's deep learning framework, [Paddle-Paddle](http://www.paddlepaddle.org/).

So far, it seems to indicate the alliance is more beneficial to Nvidia than to Baidu. One can imagine the Baidu's Nvidia adoption would expand Nvidia dominance even towards China. Yet Nvidia's effort seems to focus on merely helping making Peddle-peddle to be faster. Perhaps, this event signifies the power of Nvidia's leverage in the AI space again, just like we reported on [Issue 13](http://aidl.io/issues/13#start) and [Issue 14](http://aidl.io/issues/14#start).

[insidehpc.com](https://insidehpc.com/2017/07/nvidia-baidu-partner-accelerate-ai/?_lrsc=bab68be6-feaa-47c6-9d3f-c2a610715def&ncid=so-lin-lt-798)

## Factchecking

### [A Closer Look At "The Post-Quantum Mechanics Of Conscious Artificial Intelligence"](/grandjanitor/2017/07/10/a-closer-look-at-the-post-quantum-mechanics-of-conscious-artificial-intelligence/)

From time to time, we will receive members asking how advanced computing methods such as quantum computing would help AI/deep learning. From what we see so far, while there are many interesting work in the field, there are also many unproved theories floating around. In this article, one of us (Arthur) takes a look of a the video ["The Post-Quantum Mechanics Of Conscious Artificial Intelligence"](https://www.youtube.com/watch?v=WqCQbOVYH1I). Does it really have any real-life impact of AI? Or are we talking about some unsubstantiated theory? You can find out the details from the post.

[thegrandjanitor.com](/grandjanitor/2017/07/10/a-closer-look-at-the-post-quantum-mechanics-of-conscious-artificial-intelligence/)

## Blog Posts

### [Revisiting Unreasonable Effectiveness of Data in Deep Learning Era](https://research.googleblog.com/2017/07/revisiting-unreasonable-effectiveness.html)

From time to time, Google would stun us with scale. This time we learn about JFT-300, a 300 million images, 18k categories image database. But before you are too excited about the dataset, you should note that data by itself is chosen algorithmically based on web labels and user comments. As a results, the labels are not as clean as evaluation data set such as Imagenet - around 20% of the labels are wrong.

That doesn't make the data is not useful. Because with 10x to 100x of data of your current dataset, you can ask cut questions such as: If you increase the amount of data, would you get better results? And how would it scale? Following this thought, Google Research was able to figure out that performance scale with the order of magnitude of data, and more surprisingly it beats some state of the art results.

[googleblog.com](https://research.googleblog.com/2017/07/revisiting-unreasonable-effectiveness.html)

## Open Source

### [Tensorflow Neural Machine Translation Tutorial](https://github.com/tensorflow/nmt)

This is new tutorial of seq2seq based translation model on raw Tensorflow. If you ever played with TF, you know that the official tutorial sets already have [one tutorial on seq2seq](https://www.tensorflow.org/tutorials/seq2seq), so what make this tutorial special then? According to this [blog message](https://research.googleblog.com/2017/07/building-your-own-neural-machine.html). Part of it is that it can replicate some of the features of [Google neural machine translation (GNMT)](https://research.google.com/pubs/pub45610.html). For example, techniques such as attention mechanism wasn't available in the original tutorial. There is also a detail method to replicate a strong baseline on WMT14. It can also be applied in other problems such as text summarization.

[github.com](https://github.com/tensorflow/nmt)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing)

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## Video

### [DeepMind Teaching A.I. Agents Locomotion](https://www.youtube.com/watch?v=hx_bgoTF7bs&feature=youtu.be)

Here is a widely-circulated DeepMind's video, and the version you saw probably come from popular outlets. The technique DeepMind researchers uses are detailed [here](https://arxiv.org/abs/1707.02286) and it's surprisingly simple, the researcher train agents with different structures, using different landscapes. The funny thing is that the reward is super simple - the displacement along the x-axis! In the case of humanoids, they would try to terminate an episode if the min. distance between head and feet if it is below a certain threshold.

So what's the technical merit of the work then? Physics-based character animation is a tough problem because it requires reinforcement learning in large scale. Since policy gradient methods has high variance, usually [trust region policy optimization (TRPO)](https://arxiv.org/abs/1502.05477) or [proximal policy optimization (PPO)](https://people.eecs.berkeley.edu/~pabbeel/nips-tutorial-policy-optimization-Schulman-Abbeel.pdf) are used. One of the important merit of the paper is perhaps the researchers has implemented a distributed version of PPO in the work (or DPPO).

And the fact that DeepMind can train a humanoid to learn locomotion is also significant. Unlike other agent types, like *Planar Walker* or "Quadruped", humanoid has more degree of freedoms.

So in a way, it is more a scaling work DeepMind is doing. But that's how things work in machine learning. Impressive results are awaiting for you once you have enough machines, data, and perhaps more importantly in this case, an scalable learning algorithm.

[youtube.com](https://www.youtube.com/watch?v=hx_bgoTF7bs&feature=youtu.be)

## Member's Question

### [What is the Difference Between Deep Learning and Machine Learning?](/grandjanitor/2017/07/09/what-is-the-difference-between-deep-and-machine-learning/)

This is written by one of us (Arthur). When a new member asked about the difference between DL and ML, we were surprised by many well-intentioned yet misleading answers. For example, many claim the fact DL uses a lot of data is the key differentiator from ML, and such answer is fairly misleading. Both ML and DL can use a lot of data, it's just DL is *more effective in utilizing more data*. Unfortunately, there are too many articles floating around took up this misleading claim.

Since what is "deep" is a fairly fundamental concept in deep learning, this article is likely to help you. Enjoy!

[thegrandjanitor.com](/grandjanitor/2017/07/09/what-is-the-difference-between-deep-and-machine-learning/)
