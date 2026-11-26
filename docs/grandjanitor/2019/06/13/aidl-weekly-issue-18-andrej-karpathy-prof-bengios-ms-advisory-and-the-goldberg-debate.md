---
title: "AIDL Weekly Issue #18 - Andrej Karpathy, Prof. Bengio's MS Advisory and The Goldberg Debate"
date: 2019-06-13
---

# AIDL Weekly Issue #18 - Andrej Karpathy, Prof. Bengio's MS Advisory and The Goldberg Debate

Issue 18 *June 24th 2017* 

## Editorial

### Thoughts from Your Humble Curators

We took a short break last week, but so many happenings in our little world of AI/DL! Dr. K being hired by Tesla is certainly huge to us. So is Prof. Bengio advising Microsoft. We also follow closely the Yoav Goldberg's debate, which happens around 10 days ago. Why the interest? Because Goldberg's Debate would make you ask deep questions about our field(s), such as is NLP really solved by deep learning? Should we use arxiv as the publication platform? Does deep learning really live up to its hype on every field? We present a fairly extensive list of viewpoints in our blurb. 

On technical news, we are loving "One Model to Learn Them all" (branded as "MultiModel"), which is perhaps the first model which can learn from varieties of modalities including speech, image and text. If you are into computer vision, the late Tensorflow object detection API would also keep you entertained.

As always, if you find our newsletter useful, make sure you subscribe and forward to your colleagues/friends!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](http://cur.at/a1a4pgP?m=web)

[Collaborate fully](http://cur.at/Luohydo?m=web) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](http://cur.at/EMjwWvq?m=web). Just [\#GetStuffDone](http://cur.at/mBdw2a?m=web) 

[cyclops.io](http://cur.at/a1a4pgP?m=web)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship)

## News

### [Tesla hires Andrej Karpathy](http://cur.at/IR2vm86?m=web)

Tesla is hiring our beloved teacher of cs231n, Dr. Andrej Karpathy, away from Open.ai. Karpathy would become the Director of AI and Autopilot Vision at Tesla. And according to piece from TC, he will closely work with Jim Keller, who now overseeing both software and hardware division. How should we see the whole event? 
- If you really think about it, Dr. K only work in an industrial research setting for about a year. Yet he is now overseeing a major A.I. functionality of Tesla. Normally you would expect such position to be filled by a Professor-level personal. But for a freshly PhD? This event is simply extraordinary.
- The first thing to mention is perhaps Dr. K himself, a young scholar in the field of deep learning, his skill is known to be proficient in multiple subfields of deep learning - albeit computer vision, his unreasonably popular article on ["Unreasonable Effectiveness of RNN/LSTM"](http://cur.at/5uwmoUe?m=web), his foray into topics such as [reinforcement learning](http://cur.at/m0hKBZA?m=web) and [generative models](http://cur.at/A05h7sq?m=web). Even his software such as [convnet.js](http://cur.at/UhKhN9G?m=web) and [arxiv-sanity](http://cur.at/K6helMW?m=web) are super well-received. Of course, he is also an early pioneer of [image captioning](http://cur.at/IwUx146?m=web). We know that this guy is a real deal, has the right stuffs and has it all in deep learning.
- But the whole event also shows certain desperation of Tesla : wouldn't a professor level of expertise make more sense? Would Dr. K has enough industrial experience to tackle the AI challenges of Self Driving Car?
- Despite his skill, we believe Dr. K is facing a tremendous challenge - there is certainly a huge technical problems of how to really get Tesla to go beyond Level 2 of autonomy. Tesla is also facing fierce competitions from Waymo and 10+ car vendors.
- But then, Tesla's gamble does make sense - Dr. K is not only a deep learning researcher, he is also a beloved teacher of many AI/DLers. His star power not only gain respect for Tesla, but will help to attract more talents in the future.

In any case, we congratulate Dr. K for joining Tesla. We only hope that he can still lecture on deep learning from time to time. 

[techcrunch.com](http://cur.at/IR2vm86?m=web)

---

### [Yoshua Bengio Now Advises Microsoft (But He is Still Neutral!)](http://cur.at/r0HtOuo?m=web)

Wow, this widely-circulated Wired piece was saying Prof. Bengio is working for Microsoft now. But the Good Professor quickly [correct the rumor](http://cur.at/VCsRw1b?m=web). (Thanks to [Zubair Ahmed](http://cur.at/OlnltBJ?m=web) who informs us!) But then the article does explains why he chose Microsoft. In a way, it is to balance the other two powers in deep learning - Google already has Prof. Hinton and Facebook has Prof. LeCun, and it's fair there is duopoly of the two houses in deep learning. 

Just to be clear. Microsoft, in particular MSR ,has never been weak in deep learning in the first place. e.g. The Cognitive Toolkit stands out among deep learning toolkits. And we all know that MSR is one of the sites which achieve [human parity in the notoriously difficult Switchboard task](http://cur.at/1vlVWZP?m=web).

Yet you may say Microsoft lacks of a strategic theme like Google and Facebook on deep learning. As you might perceive from Google I/O 2017 and F8, both sites give you a sense strong presence in the DL space. Nowadays developers know about Tensorflow and TPU from Google, or PyTorch from Facebook, how many people know about DL works done by Microsoft?

Would Prof. Bengio's advisory role change MS' role in deep learning? Only time will tell. The Wired piece trace several personals from Microsoft and it's worthwhile for your time.

[wired.com](http://cur.at/r0HtOuo?m=web)

---

### [Does Uber Knows Its Acquisition Has Taken Alphabet Files?](http://cur.at/5Es6O8A?m=web)

It sounds like the case. From Uber's filing at Jun 8: 

> On or about March 11, 2016, Mr. Levandowski reported to Mr. Kalanick, Nina Qi and Cameron Poetzscher at Uber as well as Lior Ron that he had identified five discs in his possession containing Google information. Mr. Kalanick conveyed to Mr. Levandowski in response that Mr. Levandowski should not bring any Google information into Uber and that Uber did not want any Google information. Shortly thereafter, Mr. Levandowski communicated to Uber that he had destroyed the discs.

It's one thing an ex-Waymo employee stealing IP, but it's another that Uber knows it. We will wait to see the consequence for the now beleaguered company. 

[recode.net](http://cur.at/5Es6O8A?m=web)

---

### [Andrew Ng's DeepLearing.ai](http://cur.at/IIKSVU?m=web)

No details yet, but we are all excited! 

[deeplearning.ai](http://cur.at/IIKSVU?m=web)

## Blog Posts

### [A Guide to the Goldberg Debate. ](http://cur.at/jYbmevK?m=web)

When Yoav Goldberg said, 

> for f\*ks sake, DL people, leave language alone and stop saying you solve it.",

he actually started three separate debates. 
1. First it's his criticized the paper ["Adversarial Generation of Natural Language"](http://cur.at/4SWHrM0?m=web) by Rajesar et al. and ["Controllable Text Generation"](http://cur.at/kwC9Iwn?m=web) by Hu et al. He was asking if the authors were overselling their papers.
2. Perhaps more importantly, it is whether we should see his commentary as back-paddling the deep learning community. You can trace the debate from Goldberg's [clarification](http://cur.at/LLiHAIe?m=web), then [Prof. Lecun's Response](http://cur.at/nsyqAim?m=web) and again [Goldberg's response to Lecun's repsonse](http://cur.at/iOQObzu?m=web)
3. Then the last is whether the practice of arxiv publishing and flag-planting is problematic. e.g. Is it right to publish incomplete results so that you can easily claim merit later? Even when others are able to present the idea in a more complete form?

Other than the exchange between Goldberg and Prof. LeCun, here are couple of interesting viewpoints which you should look at before you judge the matter: 
- The view of Fernando Pereira, a Google VP and Engineering Fellow, who was giving [a more historical perspective](http://cur.at/hgintS8?m=web) of computational linguistic and NLP community evolved from 1980s.
- [Zhiti Hu](http://cur.at/23zzdQn?m=web)'s graceful [response](http://cur.at/UwuTTtJ?m=web) to Goldberg on "Controllable Text Generation",
- [Nikos Paragios's thought back in 2016](http://cur.at/vPJdHXw?m=web) and he expressed similar concern about deep learning's influence on computer vision.

What do we think then? First off, it's important to notice that Goldberg is actually a deep learning practitioner. So while his criticism stems the standpoint of more conventional NLPers, he also truly understand the power and limitation of deep learning. That's why many of his technical criticism on the two papers are dead on. We should also appreciate he initiated an open debate. This also carries to his criticism on deep learning in general. 

But then, how come Goldberg's post got such strong reaction then? It has to do with his criticism being abrasive, and language strong and harsh. So even he has tried to clarified and re-clarified, he never alter his original text to soften this tone. May be it has to do with Goldberg is not living/teaching in an English-speaking country. May be it has something to do with his general dark yet humorous writing. (Check out his [web site](http://cur.at/cq2pXd4?m=web)?)

[medium.com](http://cur.at/jYbmevK?m=web)

---

### [Berkeley BAIR Blog](http://cur.at/ERzzSYi?m=web)

Berkeley just release a new blog site called "Berkeley Artificial Intelligence Research" (BAIR) blog which we found it fairly interesting. It's comparable to blogs from OpenAI or DeepMind, yet from an academic institution. 

[berkeley.edu](http://cur.at/ERzzSYi?m=web)

## Open Source

### [Object Detection with Tensorflow](http://cur.at/wevhgdE?m=web)

If you have ever worked on object detection, the current state of deep learning software should make you feel rather frustrated. For starter, unlike object classification, even large toolkits don't always have examples on how to do object detection correct. And you would think that standard models such as [RCNN](http://cur.at/yTLaGbJ?m=web) and [YOLO](http://cur.at/NLD6RoF?m=web) is easy to use. But very quickly you find them to be limited in terms of software and interface. 

Now all has changed with [Tensorflow Object Detection API 1.0](http://cur.at/jjBpAfI?m=web), not only it includes standard models. It has utilities to allow you to train your own detector, which used to take much plumbing work.

[googleblog.com](http://cur.at/wevhgdE?m=web)

---

### [Google MultiModel](http://cur.at/h3t1KaJ?m=web)

Google MultiModel is based on Google Brain's paper [*One Model to Learn it All*](http://cur.at/wimEf6n?m=web). To us, this is a very interesting paper. But it is also the type of paper which can be easily misunderstood if you don't dive deep. 
- The first easy impression is to assume this is just another form of multi-task learning (MKL). Yet past multi-task learning effort *seldom integrate data input from multi-modalities*. So for example, how would you integrate visual and speech data into your network? Past MKL really doesn't address the issue. So even theoretically you can simply call MultiModel as one type of MKLs, there is a huge qualitative difference.
- Then many critics were very caught up with the fact that MultiModel can't catch up with the best results in different domains. Unfortunately, *that's not the point of the paper at all*. The paper is more a POC to show that combining different modalities is feasible. And such feasibility opens up amazing opportunities - can you now train a MultiModel, and improve your image captioning by adding speech data? It makes sense because speech data could give you phonetic language model information. In the past, doing such training would be very hard and two experts from ASR and CV would need to talk. Now you just need to pass a model around and perhaps do a transfer learning, then you are done.

If you ask about my criticism on the paper, I would like to see whether adding certain ML tasks into the mix would *degrade* the combined performance. That happens in human language learning. E.g. Even polyglot is known to be able to fluently speak 5 languages at the same time (\*). Would that happen to machines? Or would learning speech recognition degrades performance of computer vision, perhaps because modalities are different? I think those are interesting questions to ask. 
- See [Babel No More](http://cur.at/sx9wMx8?m=web)

[googleblog.com](http://cur.at/h3t1KaJ?m=web) 

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://cur.at/KWyJB2d?m=web)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing) 

[dishcraft.com](http://cur.at/KWyJB2d?m=web)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship)

## Video

### [AIDL Weekly Office Hour with Bonsai.ai's Mark Hammond](http://cur.at/aAVQwOM?m=web)

We have a wonderful session with Mark Hammond, who has a Caltech neuroscience undergraduate degree, worked for Microsoft as a developer in mid 90s, and after several gigs, he is now the CEO of Bonsai.ai. Several highlights of our chat: 
- Mark shared the business model of Bonsai.ai, which can be summarized as human-guided reinforcement learning. Many people seem to compare Bonsai.ai and Keras because both are wrappers of deep learning toolkits. Yet the two cannot be more different, Bonsai.ai's abstraction allows Machine Teaching to happens, whereas Keras is more an abstraction of different types of neural network layers.
- Mark also shared his view on the differences between the current AI craze and the Web hype back in mid-90s.
- And how much computational neuroscience and machine learning overlapped? He is not seeing clear line here, but there seems to be more overlapping of the two fields lately.

We certainly learn a lot from Mark, and love Bonsai.ai Here are several links of Bonsai if you are interested to learn more: 

Link to Bonsai's [QuickStart guide](http://cur.at/2QYCZRp?m=web).

Link to Bonsai's [Getting Started page](http://cur.at/pUoDec4?m=web), where interested users can apply for the Early Access Program.

More information on the [Early Access Program](http://cur.at/kFTlMhb?m=web).

[youtube.com](http://cur.at/aAVQwOM?m=web)
