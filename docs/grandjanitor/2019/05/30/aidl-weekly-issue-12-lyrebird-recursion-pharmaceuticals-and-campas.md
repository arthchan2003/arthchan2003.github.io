---
title: "AIDL Weekly Issue #12 - Lyrebird, Recursion Pharmaceuticals, and Campas"
date: 2019-05-30
---

# AIDL Weekly Issue #12 - Lyrebird, Recursion Pharmaceuticals, and Campas

# [Issue 12 *May 5th 2017* ](http://aidl.io/issues/12/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We start to see how machine intelligence can be applied in controversial manner, two related pieces this week: 
- Lyrebird - which astounded us by not only mimicking multiple politicians, but they claim only one minute of training data is enough.
- Campas - which provides sentence judgement based on software.

We also discuss Recursion Pharmaceuticals and what makes deep learning particularly useful in the company. 

As always, if you like our newsletter, remember to subscribe and forward to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Collaborate fully](http://i.imgur.com/ds4FU08.gif) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter) 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Some Thoughts on Lyrebird](https://techcrunch.com/2017/04/25/lyrebird-is-a-voice-mimic-for-the-fake-news-era/)

Lyrebird is perhaps the biggest news item last week. If you go to Lyrebird's [web site](https://lyrebird.ai/), you could click on several impressive demos, including a faked conversation between Obama, Clinton and Trump. 

Now Lyrebird claims that they can create a new voice sample with 1 minute of the voice. This sounds like an astounding claim. Is that really true? We believe the answer is **yes**. We can just recall [Wavenet](https://deepmind.com/blog/wavenet-generative-model-raw-audio/), a work done by DeepMind last year on using [casual convolution neural network](https://arxiv.org/pdf/1609.03499.pdf) to model voice and music. The key of the paper, other than the interesting dilated network, lies on the fact that the model can be *conditioned*. That is you can use extra variables as inputs of the model and guide the generation.

We brought up Wavenet because it is a simple way to understand such systems. Wavenet's principle is quite similar to our familiar image recognition systems. For example, similar to an image recognition, you can probably use little data to train a new model, you just have to apply [transfer learning](http://cs231n.github.io/transfer-learning/)-type of techniques. That makes us believe Lyrebird's 1-minute training claim is feasible.

What is Lyrebird's actual architecture then? Given the founder list, it's likely we are talking about [Jose Sotelo](https://mila.umontreal.ca/en/person/jose-sotelo/)'s [char2wav](https://openreview.net/pdf?id=B1VWyySKx). which is more an attention-based encoder-decoder architecture with extension.

char2wav is a fairly new work. Unlike Wavenet's paper, we don't quite see any mean-opinion score numbers yet in the author's ICLR 2017 paper. That might mean the authors do not have the most optimized system yet. This thought seems to add up. If you compare Lyre's demo with Wavenet's, while both are impressive, Lyrebird's demo still have certain chirpiness.

For now, the Lyrebird's team is still preparing the API. Our guess is it would take the guys a while. For starter, you need to come up with the production logic of how to do transfer learning. For premium customers, you would guess Lyrebird would allow them to upload audios longer than one minute. So all are interesting, but hard to work out in coding. We will see how good the team is then?

Oh, of course, there are privacy issues, but it is analyzed to the death. So we won't bring it up here. But hopefully through this blurb, you have a more a insider look of Lyrebird's controversial technology.

[techcrunch.com](https://techcrunch.com/2017/04/25/lyrebird-is-a-voice-mimic-for-the-fake-news-era/)

---

### [Recursion Pharmaceutical](https://finance.yahoo.com/news/deep-learning-luminary-yoshua-bengio-143000537.html)

One interesting trend in the last few months is how deep learning permeate fields other than the three conventional use-cases: speech recognition, computer vision and statistical machine translation. 

Health care is one of the fields which many luminaries think that deep learning would revolutionize next. For example, Prof. Geoffrey Hinton recently said, 

> “I think that if you work as a radiologist you are like Wile E. Coyote in the cartoon. You’re already over the edge of the cliff, but you haven’t yet looked down. There’s no ground underneath.”

Of course, many healthcare-related innovations so far is actually based on computer vision. For example, in radiology, deep learning is very useful in analyzing X-ray photos. In the case of Recursion, they use deep learning on huge amount of high-resolution cell-data. So that sounds like a good and well-defined use-cases for deep learning.

Perhaps an interesting question here is other than image-processing type of applications such as radiology or brain imaging. Are there any other use cases for deep learning in health care? One interesting paper lately is on how to apply [Convnet on EEG](https://arxiv.org/abs/1703.05051), so the key is perhaps how you can re-cast a problem to some existing deep-learning use-cases, instead of investigating a new architecture from scratch.

[yahoo.com](https://finance.yahoo.com/news/deep-learning-luminary-yoshua-bengio-143000537.html)

---

### [Sent to Prison by An Algorithm](https://www.nytimes.com/2017/05/01/us/politics/sent-to-prison-by-a-software-programs-secret-algorithms.html)

This piece from NYT discusses the issue of using software in sentencing, it centers around a product called [Compas](http://www.equivant.com/) by the company Northpointe Inc., which creates assessment reports for sentencing judges. 

The legal community seems to be divided on whether algorithmic sentencing is a good idea. We like Justice Bradley's view in the article: It makes sense to allow sentencing judges to use a algorithm sentencing but they should fully understand the software's limitation.

Perhaps devils is in the details, understanding the limitation of a machine learning algorithm is a non-trivial problem. Just to ask how the algorithm was trained, how much data was used, how balanced are the classes requires quite some expertise and fair understanding of machine learning.

In the case of Compas and many similar products, there is a further ramification: for IP reason, they refuse to open the algorithm. So practically the issue boils down to how you can blackbox-test an algorithm's fairness. It seems to us if the issue is not impossible, a very difficult one.

[nytimes.com](https://www.nytimes.com/2017/05/01/us/politics/sent-to-prison-by-a-software-programs-secret-algorithms.html)

---

### [Richard Socher Profile](https://www.forbes.com/sites/gilpress/2017/05/01/emerging-artificial-intelligence-ai-leaders-richard-socher-salesforce/#33a27cbd7f9a)

This Forbes's piece profile our beloved Lecturer of [cs224d](http://cs224d.stanford.edu/), Richard Socher, and his work so far in MetaMind and Salesforce. 

[forbes.com](https://www.forbes.com/sites/gilpress/2017/05/01/emerging-artificial-intelligence-ai-leaders-richard-socher-salesforce/#33a27cbd7f9a)

## Blog Posts

### [Updating Google Maps with Deep Learning and Street View](https://research.googleblog.com/2017/05/updating-google-maps-with-deep-learning.html)

Reading Google blog articles often teaches you something new, and this new research on Google Maps is one of those. 

For starter, we can only appreciate how strong Google's classifier is - it can automatically update the address of a location and business name just by text on the wild, which is known to be a difficult problem given that view can be presented in different angles, and text can be blurry.

Then there is the innovation of modeling on the deep learning front, as described by the [paper](https://arxiv.org/pdf/1704.03549.pdf), it presents a novel method on how to make a location-dependent attention mechanism.

Finally, Google is kind enough to open the [database](https://github.com/tensorflow/models/blob/master/street/README.md) to the public. That's the part I appreciate Google the most - Many companies would just do all these cutting edge research and keep the data set.

[googleblog.com](https://research.googleblog.com/2017/05/updating-google-maps-with-deep-learning.html)

---

### ["Liar, Liar Pants on Fire": A New Benchmark Dataset for Fake News Detection](https://arxiv.org/abs/1705.00648)

Here is a database related to faked news classification - LIAR, introduced by [William Wang](https://www.cs.ucsb.edu/~william/), the annotation is based on decade-long short sentences from Politifact.com. By now this is probably the bigger data set one can use for faked news classification research. In the paper, Wang also used a new algorithm which can integrate meta-text into a Convnet. 

[arxiv.org](https://arxiv.org/abs/1705.00648)

---

[*[image not recovered: twenty_by_nine_extra_large_fe255f8a-753f-41ff-b2c6-ba4ce491287a.png]*](https://medium.com/@nikasa1889/the-modern-history-of-object-recognition-infographic-aea18517c318) 

### [History of Object Detection - Infographics](https://medium.com/@nikasa1889/the-modern-history-of-object-recognition-infographic-aea18517c318)

This impressive graphic is created by [Dang Ha The Hien](https://medium.com/@nikasa1889/the-modern-history-of-object-recognition-infographic-aea18517c318). You can hardly called it infographics, but more like a very condensed summary of object recognition in a poster. Of course, all goodies of object recognition such as Alexnet is here, but then the newer material such as [SSD](https://arxiv.org/abs/1512.02325) and [MaskRCNN](https://arxiv.org/abs/1703.06870) can also be found here. 

[medium.com](https://medium.com/@nikasa1889/the-modern-history-of-object-recognition-infographic-aea18517c318)

## Open Source

### [Facebook ParlAI Framework](https://github.com/facebookresearch/ParlAI)

As some of you might know, machine learning-based dialogue system is usually domain-specific. That makes the new ParlAI framework from Facebook interesting because it allows multiple dialogue data sets to be processed and evaluated. It sounds like a huge time-saver. 

[github.com](https://github.com/facebookresearch/ParlAI)

## Video

### [PyTorch in 5 Minutes](https://www.youtube.com/watch?v=nbJ-2G2GXL0&feature=youtu.be)

Here is a great video from [Siraj Raval](https://www.youtube.com/channel/UCWN3xxRkmTPmbKwht9FuE5A) who discussed some cool features of PyTorch. We like Siraj because he can present difficult technical material to beginners. For example, in this 5-minute reading, Siraj teaches us how PyTorch and Tensorflow differ. And he also demonstrates a simple 2-layer network in his video. For researchers who are interested in working on neural network, PyTorch presents a great alternative to Tensorflow. So check it out! 

[youtube.com](https://www.youtube.com/watch?v=nbJ-2G2GXL0&feature=youtu.be)

## Member's Question

### Difference Between ML Engineer and Data Scientist?

Q: (From [Gautam Karmaker](https://www.facebook.com/gautam.karmakar.92)) *Guys, what is the difference between ML engineer and a data scientist? How they work together? How their work activity differ? Can you walk through with an use case example?"* 

A: (From Arthur, redacted)

"Generally, it is hard to decide what a title means unless you know about the nature of the job, usually it is described in the job description. But you can asked what are these terms usually imply. So here is my take:

*ML* vs *data*: Usually there is the part of testing/integrating an algorithm and the part of analyzing the data. It's hard to say how much the proportion on both sides for each job. But high dimensional data is more refrained form simple exploratory analysis. So usually people would use the term "ML" more, which mostly means running/tuning an algorithm. But if you are looking at table-based data, then it's like to be "data" type of job. IMO, that means at least 40% of your job would be manually looking at trends yourself.

*Engineer* vs *scientist*: In larger organization, there is usually a difference between the one who come up with the mathematical model (*scientist*) vs the one who control the production platform (*engineer*). e.g. If you are solving a prediction problem, usually *scientist* is the one who train, say the regression models, but the *engineer* is the guy who turn your model to create the production system. So you can think of them as the "R" and the "D" in the organization.

Both *scientist* and *engineer* are career tracks, and they are equally important. So you would find a lot of companies would have "junior", "senior", "principal", "director", "VP" prefixed the both track of the titles.

You will sometimes see terms such as *programmer* or *architect* replacing "engineer"/"scientist". *Programmer* implies their job is more coding-related, i.e. the one who actual write code. *Architect* is rare, they usually oversee big picture issues among programmers, or act as a balance between R&D organizations."

Artificial Intelligence and Deep Learning Weekly

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 19,000+ members and host a weekly ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. 

[Share on Twitter](http://ctt.ec/oecC4) | [Share on Linkedin](https://www.linkedin.com/shareArticle?mini=true&url=http%3A//aidl.io&title=Check%20out%20the%20AIDL%20newsletter%20for%20the%20week's%20most%20relevant%20and%20impactful%20developments%20in%20%23AI%20and%20%23DeepLearning%20http%3A//aidl.io&summary=&source=)

Artificial Intelligence and Deep Learning Weekly

- [Previous issue April 28th 2017](http://aidl.io/issues/11/index.html#start)
- 12 of 86
- [Next issue May 12th 2017](http://aidl.io/issues/13/index.html#start)

©2017-2019 Artificial Intelligence and Deep Learning Weekly | [Sponsorship](http://aidl.io/sponsorship/index.html)
