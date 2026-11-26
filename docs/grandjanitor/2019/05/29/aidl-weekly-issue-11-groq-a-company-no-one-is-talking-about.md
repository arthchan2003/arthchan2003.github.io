---
title: "AIDL Weekly Issue 11 - Groq: A Company No One is Talking About"
date: 2019-05-29
---

# AIDL Weekly Issue 11 - Groq: A Company No One is Talking About

# [Issue 11 *April 28th 2017* ](http://aidl.io/issues/11/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Perhaps the biggest news last week is about Groq, a company started by Google's ex-employees who work on Tensor Processing Unit (TPU). We talk about the company and its current principals. 

Of course, ICLR 2017 also held last week. We have two links this issue focused on the conference.

Other than Groq and ICLR 2017, we also cover: 
1. Notes on Stanford cs228n, a Bayesian network class,
2. a note from Athelas' Dhruv Parthasarathy on image segmentation,
3. another criticism of Neuralink.

As always, if you like AIDL Weekly, don't forget to subscribe and forward to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Collaborate fully](http://i.imgur.com/ds4FU08.gif) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter) 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Groq](http://www.cnbc.com/2017/04/20/ex-googlers-left-secretive-ai-unit-to-form-groq-with-palihapitiya.html)

According to the CNBC report, several ex-googlers, who are involved in the Google's [TPU](https://en.wikipedia.org/wiki/Tensor_processing_unit) project, form the company Groq, 

So what do we know about Groq? Really. Not much. But let's see what we find...... 
- Groq has a [website](http://www.groq.com/), it has a physical address, currently it is located in the same building of Palihapitiya's [Social and Capital](http://www.socialcapital.com/).
- According to the [SEC filing](https://www.sec.gov/Archives/edgar/data/1686725/000168672516000002/xslFormDX01/primary_doc.xml), other than Palihapitiya, there are two more key personals in the companies. The first is CEO [Douglas Wightman](https://www.linkedin.com/in/dougwightman/) who was at Google X, which focused on moonshot projects.
- Then there is [Jonathan Ross](https://www.linkedin.com/in/jonathan-ross-12a95156/). He was listed as one of the authors of the paper ["In-Data Center Performance Analysis of a Tensor Processing Unit"](https://arxiv.org/abs/1704.04760).
- According to the CNBC report, Palihapitiya claims that he hired 8 out of 10 original TPU engineers. Together with Ross' presence, it's no doubt that Groq is also building another TPU-like chip.

So how should we see the event? One plausible explanation is that while TPU is an important project, it doesn't has enough traction within Google. That causes an exodus of developers. Groq happens to be able to capture them. The next question is would they succeed?

Compare to software development, hardware engineering is known to be a much harder field to invest. In the case of TPU, what is its real-life use cases? Perhaps the first important direction is production-scale deep learning inference, which will be a huge bottleneck for years to go. If the company can really come up with a chip which has equivalent to TPU, then companies other Google can start to compete.

Finally, would Groq pull another [Otto](https://medium.com/waymo/a-note-on-our-lawsuit-against-otto-and-uber-86f4f98902a1)?. In the case of hardware engineering, without the previous design, it seems to be very difficult for Groq to pull off a new product soon. It's true that California's Law allow employee's work outside of work being protected from IP lawsuit. But how much of hardware work can be done outside Google? We doubt.

It's no doubt to us though, this is just the dawn of the Great Chip War (See this fascinating write-up [from Wired](https://www.wired.com/2017/04/race-make-ai-chips-everything-heating-fast/)).

[cnbc.com](http://www.cnbc.com/2017/04/20/ex-googlers-left-secretive-ai-unit-to-form-groq-with-palihapitiya.html)

---

### [Another Criticism on Musk's Neuralink](https://www.technologyreview.com/s/604254/with-neuralink-elon-musk-promises-human-to-human-telepathy-dont-believe-it/)

Here is a piece by Tech. Review's Antonio Regalado calls Musk's idea "isn't going to happen". His assumption is that Musk is going to use surgical implant on patients, which normally can cause life-risking complications. Of course, such experiments would be scrutinized by regulators. 

Compared to the IEEE piece we discussed in [Issue 10](http://aidl.io/issues/10#start). Regaldo's piece didn't quite consider the idea of [neuralace](https://www.quora.com/What-is-Neural-Lace-1) in Neuralink. But he considered several recent results of BCI in his piece, which make his criticism worthwhile for your time.

[technologyreview.com](https://www.technologyreview.com/s/604254/with-neuralink-elon-musk-promises-human-to-human-telepathy-dont-believe-it/)

## Blog Posts

[*[image not recovered: twenty_by_nine_extra_large_12bd8d6f-5a12-456a-9eb4-af4fa1cd032e.jpg]*](https://twitter.com/egrefen/status/856498198495580162/photo/1) 

### [Best way to understand regularization](https://twitter.com/egrefen/status/856498198495580162/photo/1)

Enough said. Courtesy by Edward Grefenstette. 

[twitter.com](https://twitter.com/egrefen/status/856498198495580162/photo/1)

---

### [cs228 notes](https://ermongroup.github.io/cs228-notes/)

This notes is for Stanford's Graphical Model class or cs228 2016-2017. As you know, the same course was taught by Daphne Koller back 5 years ago at [Coursera](https://www.coursera.org/learn/probabilistic-graphical-models), and it was known to be a very difficult class. So these notes are useful for learners who try to go through the class. 

One thing new about the 2016 class is its stress on how graphical model can be used in topics of deep learning. For example, the part about how to [train variational autoencoders](https://ermongroup.github.io/cs228-notes/extras/vae/) would worth your time.

[github.io](https://ermongroup.github.io/cs228-notes/)

---

### [A Brief History of CNNs in Image Segmentation: From R-CNN to Mask R-CNN](https://blog.athelas.com/a-brief-history-of-cnns-in-image-segmentation-from-r-cnn-to-mask-r-cnn-34ea83205de4)

Image segmentation has always been a topic of computer vision. And recent advance of [MaskRCNN](https://arxiv.org/abs/1703.06870) (discussed in [Issue 6](http://aidl.io/issues/6#start)) brought a lot of excitement to the community. This piece from Dhruv Parthasarathy, gives a fairly concise history of MaskRCNN from its origin of RCNN, and is widely circulated within Facebook and Twitterverse. 

Btw, another good source of learning about image segmentation is Kapathy's cs231n Lecture 8 and 13. Johnson has done a very nice job to describe relationship between object segmentation and detection models such as the RCNN family.

[athelas.com](https://blog.athelas.com/a-brief-history-of-cnns-in-image-segmentation-from-r-cnn-to-mask-r-cnn-34ea83205de4)

---

### [ICLR 2017](https://research.googleblog.com/2017/04/research-at-google-and-iclr-2017.html)

ICLR 2017 was held at Toulon France from Apr 24 to 26. The link points to a list of Google's papers, which include two best papers. I (Arthur) found that [openreview.net forum](https://openreview.net/group?id=ICLR.cc/2017/conference) has more interesting discussion. But if you are want to see summaries, check out [here](https://smerity.com/articles/2016/iclr_2017_submissions.html) [here] and some statistics [here](https://prlz77.github.io/iclr2017-stats/). 

[googleblog.com](https://research.googleblog.com/2017/04/research-at-google-and-iclr-2017.html)

---

### [The GAN Zoo](https://deephunt.in/the-gan-zoo-79597dc8c347)

Here is list of GANs, collected by Avinash Hindupur, it seems to be one of most comprehensive lists we've seen so far. Another companion literature list could be [really-awesome-ganhttps](https://github.com/nightrome/really-awesome-gan). 

[deephunt.in](https://deephunt.in/the-gan-zoo-79597dc8c347)

---

### [DeepMind CEO on Kasparov](http://www.nature.com/nature/journal/v544/n7651/full/544413a.html)

Deep Mind CEO, Demis Hassabis, review the book [Deep Thinking](https://www.amazon.com/Deep-Thinking-Machine-Intelligence-Creativity/dp/161039786X) written by Gary Kasparov, which would be released in May 2, 2017. Hassabis, himself a world-class chess player (with Elo Rating 2300 when he was 13), wrote about Kasparov's chess prowess, and his later embrace of the technology which defeat him. 

In these days, any chess engine in your pocket can beat Magnus Carlsen. But it still left you in wonder extraordinary humans like Kasparov can intuit how super-engineered machine works and tell us more about its limitation. That's why we are looking forward for his book and you should definitely check out Hassabis' review.

[nature.com](http://www.nature.com/nature/journal/v544/n7651/full/544413a.html)

---

### [Ethics NLP's accepted papers. ](http://www.ethicsinnlp.org/accepted-papers)

This happened about 3 weeks ago, but we found it interesting enough to bring up - Ethics in NLP is a conference with focused on ethical challenges in NLP. So some sample paper includes "Gender and Dialect Bias in YouTube’s Automatic Captions" and it could be helpful for researchers who want to understand intrinsic bias of machine learning algorithms. 

[ethicsinnlp.org](http://www.ethicsinnlp.org/accepted-papers)

## Video

### [ICLR 2017 Facebook Page (+Videos)](https://www.facebook.com/iclr.cc/)

Here is a page for ICLR 2017 conference, and you will find all live-stream videos in the page. 

[facebook.com](https://www.facebook.com/iclr.cc/)
