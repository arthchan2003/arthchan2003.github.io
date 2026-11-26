---
title: "AIDL Weekly Issue 70 - Nvidia Turing, TF 2.0"
date: 2019-07-25
---

# AIDL Weekly Issue 70 - Nvidia Turing, TF 2.0

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 70 *August 20th 2018* ](http://aidl.io/issues/70/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Hey Hey! We are back. This issue we brings you two interesting stories: 
- The Nvidia Turing architecture - how much would it affect deep learning?
- Tensorflow 2.0 - what is the major change? How would that affect you?

As always, if you like our newsletter, share with your friends/colleagues!

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 168,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Tianrang $26M](https://www.chinamoneynetwork.com/2018/08/06/gaorong-capital-cmb-international-co-lead-26m-series-a-in-chinese-ai-start-up-tianrang)
- [Navya Labs $34M](https://techcrunch.com/2018/08/09/after-going-public-in-july-navya-nabs-34m-from-the-european-investment-bank-for-its-self-driving-bus/)
- [Scale $18M](https://techcrunch.com/2018/08/07/scale-whose-army-of-humans-annotate-raw-data-to-train-self-driving-and-other-ai-systems-nabs-18m/)
- [Exabeam $50M](https://venturebeat.com/2018/08/14/cybersecurity-startup-exabeam-raises-50-million-to-be-the-next-splunk/)

Also this from Techcrunch: [Artificial Intelligence Continues Its Fundraising Tear In 2018](https://news.crunchbase.com/news/artificial-intelligence-continues-its-fundraising-tear-in-2018/)

For a counter view, check out this piece on [Quanergy Systems and how they lost its ways](https://www.bloomberg.com/news/features/2018-08-13/how-a-billion-dollar-autonomous-vehicle-startup-lost-its-way).

Artificial Intelligence and Deep Learning Weekly

---

### [Nvida Turing Architecture](https://www.anandtech.com/show/13214/nvidia-reveals-next-gen-turing-gpu-architecture)

What are the implications of the new GPU architecture for deep learning? Are there new opportunities for optimizations, in either training and inference?

Perhaps the most eye-catching feature is INT4, 4-bit integers that allow certain type of models to be optimized. Using INT4 seems to be happening in the world of [FPGA design](https://www.google.com/search?q=INT4+in+deep+learning&oq=INT4+in+deep+learning&aqs=chrome..69i57.4171j0j7&sourceid=chrome&ie=UTF-8) where the lower precision integer is used for better speed and energy efficiency.

Would the popular tensor-cores be carried over? Yes it does - developers who have optimized on Volta can potentially carry them to Turing.

Turing seems to have graphics-related features so it affects the Quadro series platform, which is usually known to be slower but more stable. Another segment Turning would likely to change is the Tesla series customer - probably the whole line of P100 or even V100 would be refreshed.

[anandtech.com](https://www.anandtech.com/show/13214/nvidia-reveals-next-gen-turing-gpu-architecture)

## Open Source

### [Tensorflow 2.0 is coming](https://groups.google.com/a/tensorflow.org/forum/#!msg/announce/qXfsxr2sF-0/jHQ77dr3DAAJ)

TF 2.0 is coming and it's a major milestone. If you read what Wicke wrote, eager execution would be the key feature. Essentially, eager execution means that 2.0 will no longer use a declarative programming model, which assume that programmers will first use python to declare the definition of a network, then TF would compile the model. While achieving higher efficiency, declarative programming is difficult to debug, and more difficult to learn than its alternative imperative model.

PyTorch is perhaps the alternative mainstream package that adopts an imperative model. So TF 2.0's move might be seen as a response of PyTorch.

Another note about TF 2.0: from 2.0 TF will no longer distribute tf.contrib because individual projects have grown to the point which requires separate repos. This makes sense to us. It also gives opportunities to newer developers to join.

TF 2.0 is expected to release a preview version late this year.

[google.com](https://groups.google.com/a/tensorflow.org/forum/#!msg/announce/qXfsxr2sF-0/jHQ77dr3DAAJ)

---

### [Facebook Unsupervised MT Code](https://github.com/facebookresearch/UnsupervisedMT/blob/master/README.md)

In April we saw a [sequel](https://arxiv.org/pdf/1804.07755.pdf) of Facebook unsupervised MT work [based on monolingual corpus](https://arxiv.org/abs/1711.00043). The new work focused on unsupervised MT and works well exceedingly well in low-resource language pairs. The team just released the code under github and you can find it from the link.

[github.com](https://github.com/facebookresearch/UnsupervisedMT/blob/master/README.md)

## Video

### [Interview with Rachel Thomas](https://www.youtube.com/watch?v=RsOpnFbufcY&feature=youtu.be)

Rachel Thomas, one of the founders of fast.ai, answered 67 questions from Siraj Raval.

[youtube.com](https://www.youtube.com/watch?v=RsOpnFbufcY&feature=youtu.be)

## Member's Question

### "You know more than Silicon Valley Engineers"

([Original Link](https://www.facebook.com/groups/DeepNetGroup/permalink/698932370499648/?comment_id=698955000497385&reply_comment_id=698978993828319)) Question: (Excerpt and rewritten) At the end of the lecture 3 of Ng's Machine Learning Coursera Course, Andrew says that "if you understood what you have done so far in the course, you know much more than many of the Silicon Valley engineers that are having a lot of success" . Is it actually true?

Answer: (By Arthur) You might be around 5 years ago - that was the time machine learning was more an esoteric topic. At then, it is true that general programmers and engineers lack of basic understanding of ML concepts such as under/over-fitting, metric-driven development.

Translate to now though, you should be aware that machine learning became a mainstream topic and general CS major knows quite well ML works. You are competing with many young bright minds on your knowledge of machine learning now.

So I would probably say, given what you know so far until Lecture 3, "you have good basic understanding of machine learning". You have a good start, but my guess you still have things to learn.

Artificial Intelligence and Deep Learning Weekly

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 168,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
