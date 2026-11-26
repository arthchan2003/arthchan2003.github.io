---
title: "AIDL Weekly Issue #19 - Fact-Checking - Does Facebook AI Create Its Own Language?"
date: 2019-06-17
---

# AIDL Weekly Issue #19 - Fact-Checking - Does Facebook AI Create Its Own Language?

## Editorial

### Thoughts From Your Humble Curators

This weekend is the Forth of July long weekend. So news are getting lighter. Yet development of AI and deep learning never stops - we just learned that Prof. Bengo becomes "Officer of the Order of Canada", Prof. Ng is joining the board of Drive.ai; Frank Chen from a16z is telling us VC will not care about AI startups in few years. Of course, we all learned that "Not Hotdog" from Silicon Valley is an actual deep learning apps. All of these events are covered in this issue. 

We also have two more new segments for you - The first is Fact-Checking. Routinely, we look at news posted on [AIDL](https://www.facebook.com/groups/DeepNetGroup/) and decide if they are faked. This time we fact-check the claim "Facebook AI Created Its Own Unique Language", which is widely circulated from popular tech outlets last week.

Another interesting feature is "Member's Submission". This time we have Neel Shah, an active member of AIDL, tells us more about research trend in India.

As always if you like our newsletter, feel free to subscribe and forward it to your colleagues/friends!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Collaborate fully](http://i.imgur.com/ds4FU08.gif) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter) 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Prof. Andrew Ng is Joining the Board of Drive.ai](http://money.cnn.com/2017/06/27/technology/startups/driveai-andrew-ng/index.html)

This is probably the first official role of Prof. Ng after [his departure from Baidu](https://www.theverge.com/2017/3/22/15020064/baidu-ai-andrew-ng-resigns). What do we think about Prof. Ng joining Drive.ai's board? Are there any technical reasons why Ng join the board? 

We think one important reason is that Drive.ai adopts an all-in-one approach in their steering and navigation system. In long run, such approach is likely to outperform a multi-stage approach. That's perhaps why Ng says Drive.ai is "one horse worth betting on".

Of course, what everyone is more interested now is [deeplearning.ai](https://www.deeplearning.ai/). So far no one knows what it is, but this [TC piece](https://techcrunch.com/2017/06/23/deeplearning/) probably did the best job in digging.

[cnn.com](http://money.cnn.com/2017/06/27/technology/startups/driveai-andrew-ng/index.html)

---

### [No Investors Are Going To Look For AI Startups In Few Years](https://machinelearnings.co/in-a-few-years-no-investors-are-going-to-be-looking-for-ai-startups-90274c91f5c9)

[Frank Chen](https://twitter.com/withfries2) shows himself not just a partner of a16z, but an advocate of AI. His [A16Z AI Playbook](http://aiplaybook.a16z.com/docs/guides/dl) is a highly readable guide for general tech audience on what AI is. 

This time, Frank opines on the prospect of AI startup. He believe that in few years, AI would be like other technologies, such as Web and Mobile, become so ubiquitous that every one just expect your company has the best solution available.

Where did we hear this view before? Oh, Bonsai's [Mark Hammond](https://www.linkedin.com/in/markisaachammond/) just told us the same in our last [Office Hour](https://www.youtube.com/watch?v=-0hkSq_x-AY)! Indeed, we agree with both Frank and Mark. There are just too much influx of talents into the AI/ML field. This would probably increase competition and commoditize many AI SaaS APIs, and eventually lower their price. Eventually, it becomes everybody game to use state-of-the-art AI system. Just look at our coverage of the "Not Hotdog" system by Tim Anglade, you will notice that using deep learning is no longer just the game for elite researchers.

[machinelearnings.co](https://machinelearnings.co/in-a-few-years-no-investors-are-going-to-be-looking-for-ai-startups-90274c91f5c9)

---

### [NYT On Prof. Geoffrey Hinton](https://www.nytimes.com/2017/06/23/world/canada/the-man-who-helped-turn-toronto-into-a-high-tech-hotbed.html?smid=fb-share)

We don't need to tell you too much about Prof. Hinton. This is a great piece from NYT about the good professor. (You know he wanted to be a carpenter when he was young?) 

[nytimes.com](https://www.nytimes.com/2017/06/23/world/canada/the-man-who-helped-turn-toronto-into-a-high-tech-hotbed.html?smid=fb-share)

---

### [Prof. Yoshua Bengio named "Officer of the Order of Canada"](https://www.theglobeandmail.com/news/national/order-of-canada2017/article35500532/)

Congrat Prof. Bengio! 

[theglobeandmail.com](https://www.theglobeandmail.com/news/national/order-of-canada2017/article35500532/)

## Factchecking

### Fact-Checking : "Facebook AI Created Its Own Unique Language"

This time we check the claim "Facebook AI Created Its Own Unique Language". Is it true? Did Facebook really create an AIese? 

When you hear such extraordinary claims from popular outlets, you should be alerted and feel suspicious. The next thing you should do is to look at the sources. In this case, the paper referred to is ["Deal or No Deal? End-to-End Learning for Negotiation Dialogue"](https://arxiv.org/abs/1706.05125) by FAIR.

So what did Facebook researchers actually do? First of all, their goal was to create bots which can negotiate. What they do first is to train a seq2seq model based on an *English* database. Of course, such bots would speak *English*, rather than any made-up language such as [Esperanto](https://en.wikipedia.org/wiki/Esperanto) or [Toki Pona](https://en.wikipedia.org/wiki/Toki_Pona).

What is this machine language everyone refers to then? As it turns out, the researchers find that 

> ... that models trained to maximize the likelihood of human utterances can generate fluent language, but make comparatively poor negotiators, which are overly willing to compromise.

So they use different strategies to evolve the bot such that they are better in negotiation. Of course, this evolution would result in a slightly different language from English, but it is more appropriate to call it a *speaking mode* rather than *a unique language*. Calling it a unique language seems to imply a difference like between English and French. Yet the difference we see here is more like English we use in chatting versus in a business setting.

AIDL Weekly rate this claim as **False**.

(20170728: The original link of the paper hosted at Amazon s3 was gone, so we replace it with the more updated version, retrieved from arxiv, as of today.)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### ["Not Hotdog"](https://medium.com/@timanglade/how-hbos-silicon-valley-built-not-hotdog-with-mobile-tensorflow-keras-react-native-ef03260747f3)

If you ever watch the show [Silicon Valley](http://www.hbo.com/silicon-valley), you would notice how realistic the show is, and how real-life technology and startups culture appear in the show. Since this is AI-**DL** Weekly, you know that I (Arthur) am going to talk about "Not Hotdog", developed by the character Jing Yang. In the show, he sold his apps "Not Hotdog" from Seefood to Periscope and made 50 million dollars. 

The surprising thing is "Not Hot Dog" is actually built by real-life deep learning tools. That's the story Tim Anglade told us on how he used Tensorflow and Keras to build the two-class classifier. The two classes are "HotDog" and ..... "Not HotDog". Lets' just call the network HotDogNet.

Have you ever train a ConvNet like HotDogNet before? In these days, it's simple to do and a great interesting experience! All you need to do is to use transfer learning. The idea is to train a pre-existing model with a small set of training data. Lecture 7 of cs231n 2016 would teach you how that works.

The merit of Anglade's work is to put HotDogNet into the right context. For example, how would you fit the model into a small device? He chose to use [Squeezenet](https://github.com/DeepScale/SqueezeNet). And to actually come up with App so that "Jing Yang" can use it, you also need to write a GUI.

Anglade is quite humble: 

> The app was developed in-house by the show, by a single developer, running on a single laptop & attached GPU, using hand-curated data. In that respect, it may provide a sense of what can be achieved today, with a limited amount of time & resources, by non-technical companies, individual developers, and hobbyists alike. In that spirit, this article attempts to give a detailed overview of steps involved to help others build their own apps.

While the app only recognizes two classes, it does show how you can apply deep learning for fun and entertainment. As Anglade suggested, even developers of non-technical companies can achieve a lot with existing deep learning toolkits. That's exactly the appeal of the current deep learning technology.

[medium.com](https://medium.com/@timanglade/how-hbos-silicon-valley-built-not-hotdog-with-mobile-tensorflow-keras-react-native-ef03260747f3)

## Open Source

### [OpenAI Releases High-performance Python library for Robotic Simulation using MuJoCo](https://blog.openai.com/faster-robot-simulation-in-python/)

It seems very impressive: MjSimPool interface shows a 400% speedup, and ~200% over an optimized using Python's multiprocessing package. It could be very useful if you try to do RL with MuJoCo. 

[openai.com](https://blog.openai.com/faster-robot-simulation-in-python/)

---

### [O'Reilly "Put AI To Work" Conference](https://conferences.oreilly.com/artificial-intelligence/ai-ny/public/schedule/proceedings)

There is not many big conferences lately, but there are few small ones. O'Reilly AI is one of them, here are the proceedings and the slides. 

[oreilly.com](https://conferences.oreilly.com/artificial-intelligence/ai-ny/public/schedule/proceedings)

## Video

### [The 3rd Research and Applied AI Summit (RAAIS) Live Stream](https://www.youtube.com/watch?v=eErBCxyYejQ&app=desktop)

Another one which catches our eyes is RAAIS. Once again it's a small conference with interesting AI results. 

> Founded in 2015 by Nathan Benaich, this community-focused showcase exists to accelerate the future of AI technology. We seek to inspire AI entrepreneurs and researchers to solve the world's most important problems.

[youtube.com](https://www.youtube.com/watch?v=eErBCxyYejQ&app=desktop) 

## Member's Submission

### [Research trends of AI in India by Neel Shah](https://neelshah18.github.io/project/2017-03-15-Scopus-analysis/)

This is the first submission article The Weekly published. The author is the Neel Shah, a very active member of AIDL, and he was guided by [Malaikannan Sankarasubbu](https://www.facebook.com/malaikannan) (CTO of datalog.ai), [Dr. Jacob Minz](https://www.linkedin.com/in/jacob-minz-16762a3/) and [Anirban Santara](https://www.linkedin.com/in/anirbansantara/). Neel was interested to learn research trends in India, including the fields of physics, mathematics, computer science, quantitative biology, quantitative finance and statistics. The results is quite telling and relevant to us AIDL audience: "learning", "neural", "network" are the few leading keywords. 

Neel's research this time only focus on India, but he promised to do similar analysis on U.S. institutions in the future. If you are interested in repeating his results - all scripts are published [here](https://github.com/NeelShah18/scopus-analysis-for-indian-researcher).

[github.io](https://neelshah18.github.io/project/2017-03-15-Scopus-analysis/)
