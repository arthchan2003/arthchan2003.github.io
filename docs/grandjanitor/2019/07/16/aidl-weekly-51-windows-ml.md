---
title: "AIDL Weekly #51 - Windows ML"
date: 2019-07-16
---

# AIDL Weekly #51 - Windows ML

# [Issue 51 *March 9th 2018* ](http://aidl.io/issues/51/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We cover Windows ML this week. What's the platform? Is it too late for MS to come up with a unified AI platform similar to CoreML? We will discuss in our News section. 

You also see the articles from Chris Olah and Sebastian Ruder in the Blog section. Both of them are thought provoking. On resources, we share you links from OpenMined's "Awesome AI Privacy" and AIDL's own AIDL_KB.

---

As always, if you like our newsletter, feel free to forward it to your friends/colleagues!

Also, do check out our sponsor, ODSC in our Sponsor section!

This newsletter is a labor of love from us. All publishing costs and operating expenses are paid out of our pockets. If you like what we do, you can help defray our costs by sending a donation via [link](http://paypal.me/aidlio/9). For crypto enthusiasts, you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: twenty_by_nine_extra_large_4f11cf9d-b0bc-4385-8c2f-9cb352d9cf40.png]*](https://www.eventbrite.com/e/odsc-east-2018-open-data-science-conference-save-50-until-friday-tickets-39574791266?discount=AIDL50) 

### [ODSC New schedule, New speakers + 55% off ends March 16](https://www.eventbrite.com/e/odsc-east-2018-open-data-science-conference-save-50-until-friday-tickets-39574791266?discount=AIDL50)

Open Data Science Conference just released [80% of their schedule](http://bit.ly/2sYs26E) and the first round of speakers for **ODSC East 2018**. 

See the dates, times and topics ODSC’s incredible speakers will be covering.

Learn, train and engage with 200+ world class experts on **machine learning, deep learning, data visualization, data management, predictive analytics, artificial intelligence and more**.

[ODSC at Boston May 11-14](https://hubs.ly/H0b4S6S0) 
- Andreas Mueller, PhD - **Core contributor** to scikit-learn
- Arun Verma, PhD - **Head of Quant Research** at Bloomberg
- Maya Gupta, PhD - **Machine Learning R & D Lead** at Google
- Joshua Bloom, PhD - **VP of Data Analytics** at GE
- Mike Tamir, PhD - **Head of Data Science** at Uber
- Drew Conway, PhD - Renowned researcher and **Data Science Venn Diagram creator**
- [See more speakers](http://bit.ly/2oEFPKu)

**Save 55% with code AIDL55** before prices increase substantially at midnight on Friday.

[Register and save 55%](http://bit.ly/2HjNOEy)

See you there!

[eventbrite.com](https://www.eventbrite.com/e/odsc-east-2018-open-data-science-conference-save-50-until-friday-tickets-39574791266?discount=AIDL50)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### Deals

- [S&P global plans to acquired Kensho $550M](https://www.xconomy.com/boston/2018/03/07/sp-global-snaps-up-kensho-for-550m-as-wall-street-adopts-a-i/)
- [UnitPath $153M Series B, now valued at $1.1B](https://techcrunch.com/2018/03/06/uipath-confirms-153m-at-1-1b-valuation-from-accel-capitalg-and-kp-for-its-software-robots/) - finally confirmed by TechCrunch this week.
- [Starsky Robotics Raised $16.5 Million Dollars](https://www.trucks.com/2018/03/08/starsky-robotics-autonomous-trucking-tech/)

Artificial Intelligence and Deep Learning Weekly 

---

### [Windows ML](https://www.theverge.com/2018/3/7/17089860/microsoft-windows-ml-windows-10-ai-platform)

Microsoft is releasing a new AI platform, Windows ML, which allows developers to run existing ML models on various MS developer suites on multiple hardware devices. According to this [page](https://docs.microsoft.com/en-us/windows/uwp/machine-learning/overview#automatic-interface-code-generation), it sounds like the platform will focus on 3 things: 
1. Hardware acceleration - built-in into DirectX 12.
2. Local evaluation - this probably implies built-in model compression technology
3. Image processing - it makes sense, because existing MS AI application seems to focus on image recognition anyway. e.g. facial recognition.

A fair question to ask: is it too late for Microsoft to create a unified platform? Especially when MS stack against Apple's CoreML and Google's colossal AI/DL architecture? Windows still has [dominance in user-space OS](https://netmarketshare.com/operating-system-market-share.aspx?). Yet developing AI applications on Windows are also known to be slightly harder on Mac and Linux. So perhaps developers would appreciate any help from Micosoft. Similar to Apple's CoreML, if the feature can serve the existing developers well, then Windows ML is doing its job. 

[theverge.com](https://www.theverge.com/2018/3/7/17089860/microsoft-windows-ml-windows-10-ai-platform)

## Blog Posts

### [Hand-drawn neural networks by Prof. Schmidhuber](https://www.instagram.com/p/BgBFegrDoai/)

Sshared by David Ha: We couldn't help thinking .... Ah, may be Prof. Schmidhuber has a point when he "schmidhuber" other people. 

[instagram.com](https://www.instagram.com/p/BgBFegrDoai/)

---

### [Google Released a Protocol Buffer Implementation for FHIR](https://research.googleblog.com/2018/03/making-healthcare-data-work-better-with.html)

Google Research released a protocol buffer implementation for FHIR. This sounds dry, yet once you learn more about both FHIR and protocol buffers, this is a rather significant event. 

For starter, FHIR is meant to be a standard to transfer electronic health record (EHR) for patient information. The use cases of FHIR can be real-time patient information gathering, and epidemic tracking.

So what is protocol buffers then? Protocol buffers is a language-independent storage/retrieval solution which is also known to be space-efficient. Google has been pushing the solution as compared to older standards such as XML.

When you combine FHIR and protocol buffers, you end up having an efficient representation of FHIR. That allows large scale ML happens in health care applications. As healthcare becomes more a focus of AI/DL, this is an important move of Google.

As a side note, the post seems to be teasing more integration between Google's application and Tensorflow. That certainly is an exciting direction for many DLers.

[googleblog.com](https://research.googleblog.com/2018/03/making-healthcare-data-work-better-with.html)

---

### [Sebastian Ruder's "Requests for Research"](http://ruder.io/requests-for-research/)

Sebastian Ruder's "Requests for Research" is a good survey on potential research direction of deep learning. It is similar to OpenAI's [request for research](https://blog.openai.com/requests-for-research-2/) earlier this year. Ruder's blog covers the following 6 topics: 
- Task-independent data augmentation for NLP
- Few-shot learning for NLP
- Transfer learning for NLP
- Multi-task learning
- Cross-lingual learning
- Task-independent architecture improvements

[ruder.io](http://ruder.io/requests-for-research/) 

---

### [Building Blocks of Interpretability](https://distill.pub/2018/building-blocks/)

Chris Olah did it again, in this new distill article, Olah et al look three different lines of visualization researches, including feature visualization, attribution and matrix factorization together. Much like other works, Olah and others doesn't just recreate others techniques, but creatively combine different ideas and come up with something new and interesting. For example, their idea on using semantic dictionary to decompose activation is one of the examples. 

Perhaps the more interesting part is the discussion of the potential design space of visualization techniques. You would intuitively think visualization is deep, because interpretability seems to be a never-ending research. Just like Olah, we wonder if we can one day come up with tools for DNN which is truly interpretable.

Oh, don't forget to play with the examples! It gives you a lot of surprising insight of Convnet too! The post was also crossposted at both Google Research Blog and Google Open Source Blog. Google released an open source visualization library called [Lucid](https://github.com/tensorflow/lucid) as well.

(Fixed typos at 3:14 p.m. 20180309.)

[distill.pub](https://distill.pub/2018/building-blocks/)

## Open Source

### [Awesome AI Privacy](https://github.com/OpenMined/awesome-ai-privacy/blob/master/README.md)

Prepared by the OpenMined project, "Awesome AI Privacy" archives important resources of understanding issues of privacy in AI. That should be a must read for developers who want to get into applications of AI which requires understanding of privacy/security issue, such as blockchain-based implementation of AI. 

[github.com](https://github.com/OpenMined/awesome-ai-privacy/blob/master/README.md)

---

### [AIDL_KB](https://github.com/arthchan2003/AIDL_KB)

This is AIDL's own knowledge base: AIDL_KB. AIDL_KB is a community-driven project to curate useful resources for AI/DL. The first version is written by AIDLer [Jan Šablatura](https://www.facebook.com/jan.sablatura) and it's reviewed by Arthur and Prof. [Amitā Kapoor](https://www.facebook.com/kapoor.amita). Other contributors are Danielius Visockas and Adam Milton-Barker. 

We got [warm reactions from the members](https://www.facebook.com/groups/DeepNetGroup/permalink/580792035647016/). There are already 5+ pull requests we merged last few days. So come by and check it out!

[github.com](https://github.com/arthchan2003/AIDL_KB)

---

### [Hand-written Notes on deeplearning.ai](https://www.slideshare.net/TessFerrandez/notes-from-coursera-deep-learning-courses-by-andrew-ng)

Here are some well-drawn notes on deeplearning.ai by Tess Ferrandez. 

[slideshare.net](https://www.slideshare.net/TessFerrandez/notes-from-coursera-deep-learning-courses-by-andrew-ng)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 110,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760 

Artificial Intelligence and Deep Learning Weekly
