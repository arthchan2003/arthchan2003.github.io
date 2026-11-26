---
title: "AIDL Weekly Issue #17 - Andrew Ng's First Interview After Baidu, and More"
date: 2019-06-13
---

# AIDL Weekly Issue #17 - Andrew Ng's First Interview After Baidu, and More

# [Issue 17 *June 9th 2017* ](http://aidl.io/issues/17/index.html#start)

## Editorial

### The Organic Growth of AI - Thoughts From Your Humble Curators

The Last two months have been very eventful - GTC, F8 and Google I/O. We have AlphaGo vs the best human player. This week is a bit slower. We see Apple come up with the Core ML - this is Apple playing catch up to Google but could very well be very impactful long-term given Apple's culture of tight integration and iOS market size and position. 

Some multi-threaded happenings this past week: 
- On celebrity in the field: We saw the first interview of Prof. Andrew Ng after he left Baidu, giving yet another interesting and inspiring interview with Forbes
- On infrastructure: There is Kaggle hitting 1 million developers, and Coursera is getting its series D. Both are training grounds of budding machine learning researchers/engineers.
- On new techniques: Facebook is able to train a Resnet-50 in one hour (Wow!) DeepMind also comes up with a technique in relationship modeling which improves around absolute ~30% accuracy. The common thread of both research is that the techniques themselves are surprisingly simple.
- On our [AIDL Facebook group](https://www.facebook.com/groups/DeepNetGroup/): We have seen record sign ups in recent weeks. Just last week, we added ~1800 members, and it's continuing apace. We should be hitting 30K members in the not too distant future.

As always, if you like our newsletter, subscribe and forward it to your colleagues/friends!

---

An announcement here - one of us (Arthur) is having a vacation, so no press for AIDL Weekly next Friday, we will resume Issue #18 at Jun 23.

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Collaborate fully](http://i.imgur.com/ds4FU08.gif) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter) 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Apple Core ML](https://developer.apple.com/machine-learning/)

As we learn from WWDC 2017, Apple shows its resolve to be competitive in machine learning. Lots of press releases there - [macOS HighSierra](https://www.apple.com/newsroom/2017/06/macos-high-sierra-delivers-advanced-technologies-for-storage-video-and-graphics/); the term "machine learning" appears 6x. 

Of course, the main dish of Apple's deep learning effort is Core ML. We are still getting up to speed on the library, but it allows iOS developers to interface apps with [different machine learning libraries](https://developer.apple.com/documentation/coreml/converting_trained_models_to_core_ml). While this might be slightly late to the game, this is a great step and Apple's size might allow it to catch up very quickly. In a way, it is matching Apple's ML software capability with the likes of [TensorflowLite](https://techcrunch.com/2017/05/17/googles-tensorflow-lite-brings-machine-learning-to-android-devices/).

[apple.com](https://developer.apple.com/machine-learning/)

---

### [WWDC 2017 - Machine Learning Features from Apple ](https://www.recode.net/2017/6/5/15740882/wwdc-2017-need-to-know-apple-ios-watchos-mac-ipad-siri)

So other than CoreML, what machine learning features excite us about WWDC2017? There are two: 
- [Sirikit](https://developer.apple.com/sirikit/) This is the first time Apple allow developers to program their speech recognizer/dialogue system. From an ML-standpoint, it means that Apple is confident enough that speech recognition accuracy would not be affected even with a untuned vocabulary set. That's a big deal.
- Handwriting and search - This is a long overdue but it isn't easy stuff. Handwriting recognition (HWR) shares theoretical formulation with speech recognition, yet fewer research groups are working on it.

[recode.net](https://www.recode.net/2017/6/5/15740882/wwdc-2017-need-to-know-apple-ios-watchos-mac-ipad-siri) 

---

### [Forbes' Interview with Andrew Ng](https://www.forbes.com/sites/peterhigh/2017/06/05/ai-influencer-andrew-ng-plans-the-next-stage-in-his-extraordinary-career/#7637f5dd3a2c)

This is perhaps the first interview of Prof. Andrew Ng after his departure of Baidu. What are the takeaways? 
- While it is still unclear what he tries to do onward, it seems he is trying to form yet another initiative to support global AI development, as he stated in the interview:

> One thing that excites me is finding ways to support the global AI community so that people everywhere can access the knowledge and tools that they need to make AI transformations.

- There are several inspiring quotes from the interview, here is the one we like:

> In addition to work ethic, learning continuously and working very hard to keep on learning is essential. One of the challenges of learning is that it has almost no short-term rewards. You can spend all weekend studying, and then on Monday your boss does not know you worked so hard. Also, you are not that much better at your job because you only studied hard for one or two days. The secret to learning is to not do it only for a weekend, but week after week for a year, or week after week for a decade. The time scale is measured in months or years, not in weeks. I believe in building organizations that invest in every employee.

It echoes what we see on the AIDL forum, because too many of our members come to us and ask how you can learn quickly and get benefits from machine/deep learning. Unfortunately, there is no short-cut. You want to keep on learning, then slowly you would start to master the material and apply it real-life, albeit at work, for fun or start a business. 

---

Last thing to note: As many people point out: in the earlier version of the Forbes' interview, Peter High has mistaken NLP as neurolinguistic programming. It does affect the technical credential of Mr. High, but we still find the Prof. Ng's view interesting and inspiring.

[forbes.com](https://www.forbes.com/sites/peterhigh/2017/06/05/ai-influencer-andrew-ng-plans-the-next-stage-in-his-extraordinary-career/#7637f5dd3a2c)

---

### [Meredith Whittaker's Gender Analysis of ICML](https://twitter.com/mer__edith/status/870322857074675712)

Founder of Google Open Research, [Meredith Whittaker](https://twitter.com/mer__edith) analyzes the gender of authors from ICML. It's disturbing to see women is underrepresented in a major conference of machine learning. 

Courtesy from Jack Clark's [Import AI](http://us13.campaign-archive2.com/?u=67bd06787e84d73db24fb0aa5&id=1b059ab83f).

[twitter.com](https://twitter.com/mer__edith/status/870322857074675712)

---

### [Kaggle now reaches 1 Million Developers Signed Up for Competition](https://venturebeat.com/2017/06/07/googles-kaggle-now-has-1-million-developers-signed-up-for-ai-competitions/)

Kaggle, in many ways, is a legendary archetype. We witness the "epitome of competitions", [Netflix Kaggle Challenge](http://blog.echen.me/2011/10/24/winning-the-netflix-prize-a-summary/) which offer $1 million dollars to developers. We know about [xgboost](https://github.com/dmlc/xgboost), its popularity were in essence fanned by Kaggle. Now this is the 7th year of Kaggle, just acquired by Google and reached their 1 Millionth user. We expect nothing will change - Kaggle will still be the training ground of learners of machine learning, and we are grateful for the contributions of Kaggle and all kagglers. 

[venturebeat.com](https://venturebeat.com/2017/06/07/googles-kaggle-now-has-1-million-developers-signed-up-for-ai-competitions/)

---

### [Coursera raised $64M in Series D](http://www.bizjournals.com/sanjose/news/2017/06/07/coursera-funding.html)

The home of our most favorite on-line classes, including Andrew Ng's *Machine Learning* and Hinton's *Neural Network Machine Learning*, is raising $64M in Series D. 

[bizjournals.com](http://www.bizjournals.com/sanjose/news/2017/06/07/coursera-funding.html)

---

### [SDC Timeline for 11 Automakers](https://venturebeat.com/2017/06/04/self-driving-car-timeline-for-11-top-automakers/)

Ever feel confused about development of self-driving car? I know we do. This VB's article summarizes the promise and progress of 11 top automakers in the planet. 

[venturebeat.com](https://venturebeat.com/2017/06/04/self-driving-car-timeline-for-11-top-automakers/)

## Blog Posts

### [AI Inside? Humor](http://www.commitstrip.com/en/2017/06/07/ai-inside/?)

We don't want to spoil a joke. But Commit Strip did a great job to tell you what most "AI" companies are really selling these days. 

[commitstrip.com](http://www.commitstrip.com/en/2017/06/07/ai-inside/?)

---

### [CNTK 2.0](https://blogs.microsoft.com/next/2017/06/01/microsoft-releases-open-source-toolkit-to-accelerate-deep-learning/#sm.00000bouna1k3ycsbybe6mxm983vb)

[CNTK 2.0](https://github.com/Microsoft/CNTK) is now at general availability. While not as popular as her peers such as Tensorflow or Theano, it is still a powerful toolkit and some [third-party studies](https://arxiv.org/pdf/1608.07249.pdf) show that it has much better performance (5x-10x) in LSTM than other toolkit. 

2\.0 is more a culmination of several release candidates beforehand. But the key features seems to be Keras backend support and Java frontend. Both are interesting. Supporting keras means CNTK 2.0 can be easily replace existing engines like TF and Theano. Whereas Java support would allow CNTK 2.0 to compete with java framework such as deeplearning4j. In a nutshell, it makes CNTK 2.0 stand out among the dozens, if not a hundred of deep learning toolkits.

[microsoft.com](https://blogs.microsoft.com/next/2017/06/01/microsoft-releases-open-source-toolkit-to-accelerate-deep-learning/#sm.00000bouna1k3ycsbybe6mxm983vb)

---

### [Exploring LSTM](http://blog.echen.me/2017/05/30/exploring-lstms/)

Looking at Edwin Chen's profile, you know that he is deep in several fields which require sophisticated mathematics: ASR in MSR, quantitive trading and ML in Google. One of his many interesting articles was [Winning the Netflix Prize: A Summary](http://blog.echen.me/2011/10/24/winning-the-netflix-prize-a-summary/) which is on the techniques by the winning Netflix Prize team; And I (Arthur) greatly enjoy his writing. 

This time Edwin Chen helps us to explore the idea of LSTM, which is always very non-trivial to understand. How do you approach such concept? Karpathy's [Unreasonable Effectiveness of Recurrent Neural Network](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) is a modern classic, but it's hard to get too much insight into what LSTM is.

The article you should probably read first is Chris Olah's [Understanding LSTM Networks](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) which give you a nice visualization how LSTM "evolved" from a vanilla RNN. It also make you easily read equations from standard LSTM literature.

Then there is Richard Socher's lecture on LSTM. Socher's approach is to first teach gated recurrent unit (GRU). He remarks that while GRU is developed later, it has a much more logical structure. Whereas it's never trivial why LSTM need all the gates in the first place. So that seems to be artificial.

So what is the merit of Chen's article then? He chose not to avoid the complexity of LSTM, but discover with his reader on how different cell gates behaves. That was the gist of the very long visualization he puts in the article.

I found his take interesting, I would recommend his along with Karpathy's, Colah's and Socher's treatment for people who want to understand LSTM.

[echen.me](http://blog.echen.me/2017/05/30/exploring-lstms/)

---

### [Imagnet 1k in 1 hour](https://research.fb.com/publications/imagenet1kin1h/)

About a year ago, I heard that Google can train an Imagenet with Alexnet architecture in 1 day. That for an amateur like me is fairly amazing - my not-so-optimized setup at home would take around 5.5 days. And I have around 3-4 thoughts on how to speed it up, but 2-3 days is probably the limit. My guess is in a large company, with other experts's help, I can also make the time to be around 1 day. 

Yes, training neural network from scratch is a super painful process. Spreading computations across GPUs is already tough, not to say spreading computation across machines. Google is probably the first group which comes up with ideas which get [parallelization working across multiple machines with multiple GPUs](https://static.googleusercontent.com/media/research.google.com/en//archive/large_deep_networks_nips2012.pdf). Yet their results are not widespread. For example, [Tim Dettmers](http://timdettmers.com/) actually advise beginners to stay away from a mult-card system, because making deep learning works is still difficult.

This makes Facebook's results quite amazing - the key insights here is Facebook was able to reduce the number of minibatches per machine by *using a large mini-batch*. But then wouldn't you need to retune the learning rate? They found there is a simple linear relationship between batch size and learning rate : 

> Linear Scaling Rule: When the minibatch size is multiplied by k, multiply the learning rate by k.

This is surprising. In fact, according to the [paper](https://arxiv.org/pdf/1608.07249.pdf), Alex Krizhevsky, of Alexnet fame, is the first person who tried out this rule, but he couldn't quite get it working with a large batch (1% absolute loss when batch size goes from 128 to 1024). The authors, on the other hand, argues that you can't quite amplify the learning rate by k in the first few epochs, you need to *warmup* this amplification *gradually*. That sounds like a breakthrough insight.

Lo and behold, that's what they did, they were able to train a Resnet-50 using 32 machines each with 8 GPUs, their actual implementation has more into it and I won't spoil here. But it's definitely one of the papers you want to check out.

[fb.com](https://research.fb.com/publications/imagenet1kin1h/)

---

### [DeepMind's Neural Approach on Relational Reasoning. ](https://deepmind.com/blog/neural-approach-relational-reasoning/)

DeepMind doesn't seem to stop after AlphaGo, and here's a very interesting result from their visual reasoning system. It covers both relational neural network (RN) and visual interaction network (VIN). For me RN is immensely interesting. Why? For the most part, DeepMind author is suggesting you don't impose a function with the scope of objects, rather you just always model pairwise relationship. (i.e. the function g in the [paper](https://arxiv.org/pdf/1706.01427.pdf)) As the authors suggest, the formulation simply baked the constraints directly into the model, with similar spirit as convolution neural network in computer vision. Again, this is a surprisingly simple thought, but DeepMind see good results which surpass human performance. 

[deepmind.com](https://deepmind.com/blog/neural-approach-relational-reasoning/)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing) 

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## Member's Question

### Udacity DL class vs Hinton's ?

AIDL Member [Fru Nck](https://www.facebook.com/profile.php?id=100009333795058&fref=nf) asked (rephrase): *Can you tell me more about the Hinton's Coursera class vs the Google's Udacity class on deep learning?* 

Here are couple of great answers from other members:

By [Karan Desai](https://www.facebook.com/karand3sai): "Former focuses more on theory while latter gets you through Tensorflow implementations better, keeping the concepts a little superficial. In my opinion both courses were made to serve different purposes so there isn't a direct comparison. Meanwhile you can refer to [Arthur's blog](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)."

By [Aras Dar](https://www.facebook.com/arasdar?fref=ufi): "I took them both. For the beginners, I highly recommend Udacity and after Udacity, you understand Hinton's course much better. Hinton's course is more advanced and Udacity course is built for beginners. Hope this helps!"

Afterthought from me: I didn't quite take the Udacity class. But by reputation, it is more a practical class with many examples. If you only take Ng's, Hinton class is going to confuse you. In fact it confuses many PhDs I know. So go for the Udacity class and few others first before you dive into Hinton's.

Artificial Intelligence and Deep Learning Weekly
