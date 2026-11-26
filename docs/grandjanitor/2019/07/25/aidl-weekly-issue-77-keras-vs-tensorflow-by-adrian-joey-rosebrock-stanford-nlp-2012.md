---
title: "AIDL Weekly Issue #77 - Keras vs Tensorflow by Adrian Joey Rosebrock Stanford NLP 2012"
date: 2019-07-25
---

# AIDL Weekly Issue #77 - Keras vs Tensorflow by Adrian Joey Rosebrock Stanford NLP 2012

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 77 *October 15th 2018* ](http://aidl.io/issues/77/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we cover two recent Google's results: one on metastatic breast cancer detection, the other on their recent ActiveQA system. 

As always, if you find this newsletter useful, feel free to share it with your friends/colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 177,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [LoadSmart $21M](https://venturebeat.com/2018/10/09/loadsmart-raises-21-6-million-for-ai-freight-booking/)
- [Micron $100M](https://www.reuters.com/article/us-micron-tech/chipmaker-micron-to-invest-100-million-in-artificial-intelligence-companies-idUSKCN1MK2SU)
- [Machinify $10M](https://techcrunch.com/2018/10/08/machinify-raises-10-million-to-help-businesses-use-ai-to-monetize-data/)
- [Robosense $45M](https://www.chinamoneynetwork.com/2018/10/11/chinese-self-driving-lidar-provider-robosense-raises-45m-in-biggest-funding-round-among-local-peers)
- [Humu and Nudge](https://qz.com/work/1415395/after-two-years-in-stealth-mode-the-former-head-of-hr-at-google-reveals-his-new-startup/)

Artificial Intelligence and Deep Learning Weekly 

## Blog Posts

### [Keras vs Tensorflow by Adrian Joey Rosebrock](https://www.pyimagesearch.com/2018/10/08/keras-vs-tensorflow-which-one-is-better-and-which-one-should-i-learn/)

Joey Rosebrock wrote another useful article for beginners: should you even compare Keras and Tensorflow? This is one FAQ in AIDL as well. And of course, the answer is *no*. Because Keras is a layer which build on top of Tensorflow, and we think Joey once again gave very good answer in his post. 

A good question here is what's the impact if you have misconceptions in deep learning, like you feel there is a difference between Keras and Tensorflow? We believe these misconceptions are detrimental to your learning. Generally, it's always better to learn a technical topic from its first principle. e.g. in deep learning, you should learn up ideas such as optimization, gradient descent, the forward and backward propagation first. Then on the basic of Tensorflows, and eventually realize Keras is just a layer. Going through this path will take you more time, but you understanding would be real. You will also ask more relevant questions, thus get closer to finishing a task, a project, or perhaps really get a job in machine learning.

[pyimagesearch.com](https://www.pyimagesearch.com/2018/10/08/keras-vs-tensorflow-which-one-is-better-and-which-one-should-i-learn/)

---

### [Stanford NLP 2012 ](https://www.youtube.com/playlist?list=PLoROMvodv4rOFZnDyrlW3-nI7tMLtmiJZ&disable_polymer=true&app=desktop)

Natural language processing (NLP) has been rapidly changed last 5 years. But then the basics hadn't changed much - it's useful to learn up parsing, stemming, basic IBM models. One good beginner to intermediate course in NLP is perhaps Jurafsky NLP class in 2012. Here is the official Stanford Online playlist. You may find it useful to watch it with the 2rd edition of Jurafsky's book: [Speech and Language Processing](https://www.amazon.com/Speech-Language-Processing-Daniel-Jurafsky/dp/0131873210?keywords=dan+jurafsky&qid=1539621275&sr=8-1&ref=sr_1_1). 

The issue of the course, viewing from modern perspective, is that it is not deep learning-based. But then, you still need fair amount of knowledge in NLP to learn better for the current days deep learning algorithm.

[youtube.com](https://www.youtube.com/playlist?list=PLoROMvodv4rOFZnDyrlW3-nI7tMLtmiJZ&disable_polymer=true&app=desktop)

---

### [Applying Deep Learning to Metastatic Breast Cancer Detection](https://ai.googleblog.com/2018/10/applying-deep-learning-to-metastatic.html)

This is a recent blog post on how Google applies deep learning to metastatic breast cancer detection. The post is quite readable, and point you to two relevant papers. The idea is quite simple: use deep learning to detect spreading (*metasized*) cancer from images. So this is what the first paper "Applying Deep Learning to Metastatic Breast Cancer Detection" talks about. The paper details the development of LYNA which is essentially a visualization system for doctors. And the selling point is easy to understand: machine can look at images pixel by pixel, so this should save doctor's time. 

This is the theory, so what Google's author did is to test out if this workflow is really better. It boils down to the second paper: "Impact of Deep Learning Assistance on the Histopathologic Review of Lymph Nodes for Metastatic Breast Cancer". They did a study on 6-board certified pathologists, and ask will using system make them save time? It does, Google authors said, and the per-slide review time goes down from 2 minutes and 1 minutes.

If you look at the article, authors of the post was very cautious on whether if the technology is useful yet: 

> While encouraging, the bench-to-bedside journey to help doctors and patients with these types of technologies is a long one. These studies have important limitations, [...]

This somber tone is oddly assuring.

One more thing, does this paper has any to do with DeepMind's work on breast cancer as well? (As we reported in last issue?) It doesn't seem to be the case. Currently Alphabet's research on ML application on medical imaging seems to come from two institutions: DeepMind and Verily. While DeepMind was involved in the DeepMind-RoyalFree event in the past, Verily's researchers seems to be more sober in tones when it comes to whether machine learning can really be used in medical imaging. It happens here in their breast cancer detection research. It also happens in their research of detecting cardiovascular disease through retinograph. (As we discussed in Issue [49](http://aidl.io/issues/49).)

[googleblog.com](https://ai.googleblog.com/2018/10/applying-deep-learning-to-metastatic.html)

---

### [ActiveQA](https://ai.googleblog.com/2018/10/open-sourcing-active-question.html)

We learned about ActiveQA this week through [Venturebeat](https://venturebeat.com/2018/10/10/google-open-sources-activeqa-an-ai-agent-that-learns-to-ask-good-questions/) and the reporting is quite faithful. So we just want to add a few things for our subscribers: 
- QA machines are not chatbots, so while the Google's system is quite powerful, you can't quite use it to come up with a bot which converses with humans. But then as it is advertised, ActiveQA is powerful to come up with natural sounding and clarifying questions.
- Looking at the details from the original [paper](https://ai.google/research/pubs/pub46733), there are many interesting technical tidbits. For example, neural MT is used in modeling the rephrase of a questions, but its training is funny: they first train a neural MT model based on bilingual language pairs, then recondition the final model for single-language retraining. So this applied the idea of [zero-shot translation](https://ai.googleblog.com/2016/11/zero-shot-translation-with-googles.html) but it's more suitable for tasks like rephrasing which has less training data.
- The github is Tensorflow-based package and you may train the seq2seq reformulation models, as well as the Convnet answer-selection models. It feels more like a research codebase, rather than a general framework.

[googleblog.com](https://ai.googleblog.com/2018/10/open-sourcing-active-question.html) 

---

### [Open AI Scholars 2019](https://blog.openai.com/openai-scholars-2019/)

New OpenAI Scholars for 2019 Winter is opened to public. Open AI, as a non-profit, has produced many impressive research results in the past few years. And their Open AI Scholars program also come up with several interesting [final projects](https://blog.openai.com/openai-scholars-2018-final-projects/). 

Successful applicants can remotely with mentors from the institutes, and you are guarantee to have an interview with OpenAI after finishing the program. Sound s like a great opportunities for our subscribers.

[openai.com](https://blog.openai.com/openai-scholars-2019/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 177,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. 

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
