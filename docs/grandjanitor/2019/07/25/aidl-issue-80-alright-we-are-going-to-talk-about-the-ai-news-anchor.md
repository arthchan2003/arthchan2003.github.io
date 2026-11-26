---
title: "AIDL Issue 80 - Alright..... We are Going to Talk About the AI News Anchor....."
date: 2019-07-25
---

# AIDL Issue 80 - Alright..... We are Going to Talk About the AI News Anchor.....

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 80 *November 12th 2018* ](http://aidl.io/issues/80/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we cover two topics: first off, why Facebook fails to build their own speech recognizer. It is surprising to see an organization like Facebook to have so much troubles to build and grow one machine learning technology. What are the reasons behind? We will quote the Forbes' article as well as give out some of our own opinions. 

Also.... since we got around 10 post submission on the much hyped AI news anchor, we are going to talk about it too. What is it really? Is it "intelligent"? And what is the true impact of such technology?

As always, if you find this newsletter useful, feel free to share it with your friends/colleagues.

---

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 178,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [appzen $35M](https://techcrunch.com/2018/10/30/appzen-nabs-35m-for-ai-that-audits-expenses-in-real-time-for-non-compliance-and-fraud/)
- [neo4j $80M](https://venturebeat.com/2018/11/01/neo4j-raises-80-million-for-next-generation-graph-databases/?fbclid=IwAR0KjjzLWB6XODJ7RGc7Hn-Huh_Kqt2PV7lqyrYMuwAtCv_S91yhEnM2Gy0)
- [Taranis $20M Series B](https://techcrunch.com/2018/11/06/precision-farming-startup-taranis-gets-20m-series-b-for-its-crop-monitoring-tech/)
- [DeepMap $60M](https://techcrunch.com/2018/11/01/deepmap-a-maker-of-hd-maps-for-self-driving-raised-at-least-60m-at-a-450m-valuation/)

Correction: Early version of this item states that Precision got $20M Series B, the correct company name should be Taranis. 

Artificial Intelligence and Deep Learning Weekly

## Factchecking

### [The "First" AI News Anchor](https://www.scmp.com/tech/innovation/article/2172235/xinhua-news-agency-debuts-ai-anchors-partnership-search-engine-sogou)

Last week, we learn that Chinese state-run news agency, Xinhua, is deploying an AI news anchor. In our experience, sensational news like this can easily mislead the public. e.g., just on our forum [AIDL](https://www.facebook.com/groups/DeepNetGroup/) alone, we see 10 post submissions on the same news. And we also see this well-timed [piece from MIT review](https://www.technologyreview.com/the-download/612401/this-is-fake-news-chinas-ai-news-anchor-isnt-intelligent-at-all/) which argues that, "the anchor isn’t intelligent in the slightest. It’s essentially just a digital puppet that reads a script". 

In this piece, we will focus on three aspect of the news. The first is, is it really that shocking to see an AI news anchor like this? Or had we already seen similar research work before? Second, do machine programs like this think like what do? Can they really replace human news anchor? The last is what is the impact this kind of automatic news delivery machines in our future.

On the first count, what is this AI news anchor actually? In essence, it is just an audio-to-video synthesizer. Given an audio, the machine can generate video monologue which seems like a human news anchor is speaking. Such highly realistic synthesized monologue has been researched for a while. For example, just last year, researchers from Washington University has published similar work which create a video from President Obama based on audio alone, all you need to do is to have large amount of video and a clever frame picking algorithm. There are many nuances of such work. For example, making the lip realistic has always been a tough technical problem. We recommend you to take a look of this [original paper](https://grail.cs.washington.edu/projects/AudioToObama/).

There were also similar commercial effort such as [Lyrebird](https://lyrebird.ai/). In a nutshell, if you follow deep learning development in the last few years, this piece of news shouldn't surprise you at all. You may replicate this work if you happen to have a lot of video footages from a news anchor. Since Xinhua is state-run, it is not a surprise that large amount of footages is available for a specific anchor, in this case, his name is Zhang Zhao.

If an AI news anchor is technologically feasible, then the next question is whether such machine is "intelligent" as in our common sense. The answer is: of course not. As we just mentioned, the anchor is more like an audio-to-video converter. Since it is just a converter, you should not expect the anchor would exhibit other human anchors' behaviors. For example, they would not have a friendly banter with their coanchors, nor they would improvise when there is an unexpected situation during broadcasting This means the machine is really not how we human think of as an intelligent news anchor. All it is, as MIT review suggest, "a digital puppet that reads a script".

The final point is what is the implication of such technology. The strength of an automatic news machine, of course, is that unlike humans it will never got exhausted. And such technology could have many interesting applications. For example, for poor area where setting up physical news stations is a problem, machine news anchor can come in and fill the void. Of course, the downside is they are also easy subject of misuse. e.g. Malicious party can just use them to spread disinformation. Remember DeepFake? There has been concerns on whether hackers would deep-learning based video synthesis to affect [US mid-term election](https://www.wired.com/story/will-deepfakes-disrupt-the-midterm-election/).

We believe though, the first step to stop misusing a technology such as DeepFake is to understand what the technology really is. Hopefully this article helps you to do so.

[scmp.com](https://www.scmp.com/tech/innovation/article/2172235/xinhua-news-agency-debuts-ai-anchors-partnership-search-engine-sogou)

## Blog Posts

### [Why Facebook Failed to Build Their Own Speech Recognizer](https://www.forbes.com/sites/parmyolson/2018/10/30/on-mute-how-facebook-fell-behind-on-voice-technology/#fe4b2693b507)

One of us (Arthur), has been working in the speech recognition industry, so we are quite aware that Facebook is developing their own recognizer. Yet, it is also painfully clear from the article that FB's direction of development is misguided, and it is doomed to fail. So we are writing this item to analyze the cause, and what Facebook could potentially do. 

To start off, what's so special about automatic speech recognition (ASR) in the business of machine learning then? If you delve deep, speech as a pattern is subtle and hard to model. By itself, currently it is usually seen as speech as a sequence of n-dimensional vector. So modeling is usually done by non-trivial models such as hidden Markov model (HMM) or in deep learning long short term model (LSTM). Even now, training a good ASR model with 10000+ hours, takes a lot of resources to do well: first of all, data collection has to be based on the specific accent of the your market. e.g. an US English models would not work too well in other English-speaking countries.

Then there is data labeling, or in the case of speech recognition parlance, *transcription*. How do you find the linguistic experts to transcribe data? Unlike image recognition, crowd sourcing might give your poor quality transcripts, and results in poorly-performing models. So do you want to hire transcribers in-house? Would that fit to your budget? And who is going to manage them?

So say you have transcribed data, you are only half-way there. Unlike the workflow of image recognition training, many practical speech recognition training still consists of multiple steps. (Seq-to-seq type of training works but it takes a lot of data.) As a result, training is still a magical step which takes specialists to tend. e.g. What if the training fails? Do you need to fix the source code? And how do you interpret various failure modes in training? None of these questions are trivial. ASR source code are usually complex program which require programmers understand deep coding topics such as dynamic programming, numerical optimization or matrix computation. Many of them are written in low-level language such as C/C++ (i.e. not python), and takes an experienced coder to maintain. That's why most company job postings on speech recognition usually requires master or doctor degrees from the candidates.

Once you can create and maintain a speech recognizer. The final question is how do you grow its capability. For example. It's hard to estimate the time cost of training a recognizer in different languages. So how long should you setup your goal? If engineers fail to train a recognizer on time, what should you do? Those are difficult questions. For example, in our opinions, if it takes time for a team to fix bugs but they get it right in a production system, it worths for all the time it takes. But in our fast-paced world of development, not all the companies would/could give so much time to tend a recognizer. Not to say, the best speech recognizer, in our opinions, implement the most advanced mathematical model.

Let's go back to the case of Facebook: from the article, we learn that product managers would switch domains of a speech recognizer in half a year basis. And it can go from news transcription to voice dialogue. For us who work in the business for long time, such switching of tasks, is the most nightmarish scenario. Half a year might not even give you enough time to collect data. Not to say, you might need to tailor-made product features based on one type of domain. e.g. There are a lot of differences between speech recognition which can run offline and run on live. Have the Facebook product manager ever consider these issues? We don't think so.

What we would suggest to Facebook to do .... if they are serious about building a speech recognizer..... is to form a cross-departmental team with a powerful and an influential team leader. Members of the team, even for managers, should have strong understanding of how a recognizer should be built. We understand it is tough, but such team might give Facebook a real chance to at least sustain the effort in speech recognition, and perhaps when stars align, comes up with a product which is on-par with Google, Amazon or Apple.

Our two cents.

[forbes.com](https://www.forbes.com/sites/parmyolson/2018/10/30/on-mute-how-facebook-fell-behind-on-voice-technology/#fe4b2693b507)

---

### Google AI Blogs Last Two Weeks

- [Humpback detection](https://ai.googleblog.com/2018/10/acoustic-detection-of-humpback-whales.html)
- [AdaNet](https://ai.googleblog.com/2018/10/introducing-adanet-fast-and-flexible.html)
- [BERT](https://ai.googleblog.com/2018/11/open-sourcing-bert-state-of-art-pre.html)

Artificial Intelligence and Deep Learning Weekly 

---

### [Spinning AI](https://spinningup.openai.com/en/latest/index.html?fbclid=IwAR3lRObwMhZZ5BwZHXScTcRmeIJ5p6WONs_TfOyMmYlEfCivYnKosc6DURk)

OpenAI release Spinning AI last week. It's mind-blowing because it's perhaps the first time we see a major institution released a course related to deep reinforcement learning. 

Looking into details of Spinning AI, the goal is to bridge the gap between papers and actual RL implementation. So in some sense, it is more a tutorial you can follow while taking on-line class such as [David Silver's RL class](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html). The tutorial is in great detail, we also saw a fairly extensive bibliography which seems to more relevant than standard RL textbooks and resources existing.

As for support, Open AI promise to give high bandwidth support for Spinning AI. We hope they can sustain the effort because Open AI as an organization occasionally drop initiatives such as OpenAI Gym.

[openai.com](https://spinningup.openai.com/en/latest/index.html?fbclid=IwAR3lRObwMhZZ5BwZHXScTcRmeIJ5p6WONs_TfOyMmYlEfCivYnKosc6DURk)

---

### [Multi-object tracking with dlib by Adrian Rosebrock](https://www.pyimagesearch.com/2018/10/29/multi-object-tracking-with-dlib/?fbclid=IwAR3aIMiOzE9Coto0Fb-IYFgd1Bor8R1VGpN3Wd4ngX63EzRfKjApSuLU_PQ)

This post expands Adrian's previous tutorial to track multiple objects. 

[pyimagesearch.com](https://www.pyimagesearch.com/2018/10/29/multi-object-tracking-with-dlib/?fbclid=IwAR3aIMiOzE9Coto0Fb-IYFgd1Bor8R1VGpN3Wd4ngX63EzRfKjApSuLU_PQ)

## About Us

### About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 179,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. 

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
