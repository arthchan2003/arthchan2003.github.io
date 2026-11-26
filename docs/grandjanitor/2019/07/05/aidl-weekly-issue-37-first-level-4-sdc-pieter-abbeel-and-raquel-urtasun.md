---
title: "AIDL Weekly Issue 37 - First Level 4 SDC, Pieter Abbeel and Raquel Urtasun"
date: 2019-07-05
---

# AIDL Weekly Issue 37 - First Level 4 SDC, Pieter Abbeel and Raquel Urtasun

# [Issue 37 *November 12th 2017* ](http://aidl.io/issues/37/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

The biggest news last week: Waymo was putting the first Level 4 SDC on the ground. We also learned that Pieter Abbeel has left OpenAI and started his own robotic startup, Embodied Intelligence. Wired profiled Uber's new head of their Toronto's team, Raquel Urtasan. We cover all these pieces in our News section. 

The rest of this issue should be very interesting as well: First is the new Distill article by (Chris) Olah, Mordvintsev and Schubert, which is an excellent review on visualization. Then, there is Google PhD Fellow Anirban Santara gave us his take on how to build a career in ML. AIDL-LD members, Ben Davis, gave us a nice summary of a paper on image fusion schemes. And you may feel interested in the two papers published by the Salesforce Einstein's Lab last week, both on NNMT, which Arthur reviewed this week.

---

Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

As always, if you like our newsletter, feel free to subscribe/share the letter to your colleagues.

We will host our own show at the AI World events: "Attack of the AI Startups". If you live in the New England area, feel free to join!

Artificial Intelligence and Deep Learning Weekly

---

### [Attack of the AI Startups ](https://aiworld.com/sessions/mlai/)

We will be hosting an AIDL Meetup at the AI World Conference in Boston on Dec 12 at 6:15pm where some cutting-edge AI companies will present. We got FREE tickets for you all! Come join us in person if you can!! 

Attack of the AI Startups - https://aiworld.com/sessions/mlai/ at AI World - aiworld.com

All attendees need to register to attend. To register, please go to: https://aiworld.com/live-registration/ To receive your FREE expo pass (thru Nov 15), use priority code: AIWMLAIX

To receive a $200 discount off of your 1, 2 or 3 day VIP conference pass, use priority code: AIWMLAI200

AI World is the industry's largest independent event focused on the state of the practice of enterprise AI and machine learning. AI World is designed to help business and technology executives cut through the hype, and learn how advanced intelligent technologies are being successfully deployed to build competitive advantage, drive new business opportunities, reduce costs and accelerate innovation efforts.

The 3–day conference and expo brings together the entire applied AI ecosystem, including innovative enterprises, industry thought leaders, startups, investors, developers, independent researchers and leading solution providers. Join 100+ speakers and 75+ sponsors and exhibitors and thousands of attendees. Other than that, we also include some of our analyses on two paper as well as multiple interesting links for blogs and open source resources. So check it out!

As always, if you like our newsletter, subscribe/forward it to your colleagues!

[aiworld.com](https://aiworld.com/sessions/mlai/)

## News

---

### [First Level 4 SDC in US](https://www.theverge.com/2017/11/7/16615290/waymo-self-driving-safety-driver-chandler-autonomous)

This is huge. So this is the first Level 4 SDC on the road. Level 4 is commonly known as "mind off", which means human supervision is not necessary. Deploying a Level 4 on the road shows that Waymo is confident about their technology. 

Phoenix was chosen because restrictions of SDC is nada at this point. But then cities around the States is frantically changing laws so that they can be the new hub of SDC. In this rate, we can expect SDC deployment would spread across united states soon.

[theverge.com](https://www.theverge.com/2017/11/7/16615290/waymo-self-driving-safety-driver-chandler-autonomous)

---

### [Pieter Abbeel left OpenAI, started Embodied Intelligence](https://www.wired.com/story/embodied-intelligence-want-to-really-teach-a-robot-command-it-with-vr/)

We are surprised by another superstar researcher leaving OpenAI. Back in June, we learned that Andrej Karpathy join Teslas as a director of AI. This time, RL expert Pieter Abbeel left OpenAI and started his own company Embodied Intelligence. 

How should we see this? There should be at least three perspectives. The first is that OpenAI wasn't able to keep many star researchers decided. That's perhaps because it is a non-profit institution, and funding for her seems to be scarce. Remember the web version of OpenAI gym? Researchers at OpenAI seems to give up its maintenance because of [lack of resources](https://www.reddit.com/r/MachineLearning/comments/6zvlm2/d_openai_closing_down_gym_toolkit_website/) (Also see Weekly Issue 30(http://aidl.io/issues/36#start) for more coverage.)

Then it is the question about whether one should develop AI via research or via deploying real-life production system. In the case of both Karpathy and Abbeel, they chose to come up with commercial solutions. Perhaps the difference is one decided to work for a S&P 500 company, one decided to start his own company.

As for Abbeel's decision itself, it is certainly an interesting space he got into. Embodied Intelligence's business model is to create solution which allow robotics arm to adapt more quickly. Their solution is, AFAWK, using VR to accelerate learning. The space though is rather hot and crowded, as [Spectrum](https://spectrum.ieee.org/automaton/robotics/artificial-intelligence/ai-startup-embodied-intelligence) reported, there are other companies existing including [Kindred.ai](https://www.kindred.ai/), [Kinema Systems](http://www.kinemasystems.com/), and [RightHand Robotics](https://www.righthandrobotics.com/). Arguably, they lack of brilliance of Abbeel and his OpenAI's colleagues, but then you got to ask if $7 million ([as reported by NYT](https://www.nytimes.com/2017/11/06/technology/artificial-intelligence-start-up.html)) for such investment-intensive application such as robotics.

[wired.com](https://www.wired.com/story/embodied-intelligence-want-to-really-teach-a-robot-command-it-with-vr/)

---

### [Meet Raquel Urtasun](https://www.wired.com/story/meet-the-woman-making-ubers-self-driving-cars-smarter-cheaper/)

Who is Raquel Urtasan? You might wonder. As it turns out Raquel Urtasan was an Associate Professor of University of Toronto before she joined Uber as the head of Uber's Toronto's SDC group. While her PhD was more on [human motion models](http://www.cs.toronto.edu/~urtasun/publications/urtasun_thesis_3541.pdf), her tenure at UoT was more focused on how to use deep learning in computer vision and SDC. 

Urtasan's philosophy of SDC is very different from the mainstreams such as Waymo's. She advocates the use of cameras instead of the more expensive LIDAR as the main sensors of SDC. For example, she and her students have many papers on using deep learning to create coherent images as well as utilizing different type of mapping images in SDC. (See her [publication page](http://www.cs.toronto.edu/~urtasun/publications/publications.html).

Coincidentally, she joins when Waymo just started their high-profile lawsuit against Uber and Levandowski, which as you know is all about whether Levandowski is stealing trade secret of Waymo on LIDAR. Performance of Uber's SDC was also known to be lagging with [high disengagement rate](http://www.businessinsider.com/uber-self-driving-cars-disengagements-once-a-mile-humans-leaked-data-2017-3).

Will Urtasun succeed? It's hard to say, LIDAR and cameras are generally complementary technologies. You can imagine sometimes you need information from one of them. So it's very hard to say which technology will prevail. Of course, those who support to use camera as the only sensor would face another problem: LIDAR's cost of production is [reducing](http://www.businessinsider.com/googles-waymo-reduces-lidar-cost-90-in-effort-to-scale-self-driving-cars-2017-1), would there be one day LIDAR is as commonplace as camera?

For Uber though, Urtasan's hire is a kind of change of heart, with camera-based technology, they will not prone to compete with giants such as Waymo who had invested on LIDAR-based technology for more than 10 years. Camera-based technology could give Uber an "out", and gives a chances for her SDC research to grow again.

[wired.com](https://www.wired.com/story/meet-the-woman-making-ubers-self-driving-cars-smarter-cheaper/)

## Blog Posts

### [Feature Visualization - A Distill Article. ](https://distill.pub/2017/feature-visualization/)

If not the best, this is one of the best review of feature visualization in a convolutional neural network. For years, our go-to tutorial on visualization is usually Johnson's lecture in cs231n. But then we never seen visualization can achieve stunning quality like the Distill authors (Olah, Mordvintsev and Schubert) did. 

Notice it is not just a review article, the authors also introduce a new criterion to improve diversity of visualization. We are also happy that Distill continues to maintain high quality in its publication.

[distill.pub](https://distill.pub/2017/feature-visualization/)

---

### [Andrew Ng: "Enough Papers!"](https://medium.com/@Synced/andrew-ng-says-enough-papers-lets-build-ai-now-6b52d24bcd58)

Prof. Ng reportedly said, 

> We have enough papers. Stop publishing, and start transforming people’s lives with technology.

Sounds like many young researchers already agree with him, just look at Andrej Karpathy? And Pieter Abbeel, who we cover this issue. 

[medium.com](https://medium.com/@Synced/andrew-ng-says-enough-papers-lets-build-ai-now-6b52d24bcd58)

---

### [MS or Startup in Deep Learning by Anirban Santara](https://medium.com/@nrbnsntr/ms-or-startup-job-which-way-to-go-to-build-a-career-in-deep-learning-2d62a5b10f9e)

At AIDL, we frequently got questions on how to start an DL and data science career. Here is the take of Google PhD Fellow Anirban Santara on whether you should take a Master or join a startup to build such career. 

[medium.com](https://medium.com/@nrbnsntr/ms-or-startup-job-which-way-to-go-to-build-a-career-in-deep-learning-2d62a5b10f9e)

## Open Source

### [Models from NASNet](https://github.com/tensorflow/models/tree/master/research/slim/nets/nasnet)

This is based on the work of the paper ["Learning Transferable Architectures for Scalable Image Recognition"](https://arxiv.org/abs/1707.07012). The variants are trained on CIFAR-10 and Imagenet and can be used in varieties of applications. 

[github.com](https://github.com/tensorflow/models/tree/master/research/slim/nets/nasnet)

## Paper/Thesis Review

### [Weighted Transformer](https://einstein.ai/research/weighted-transformer)

This is one of the two papers SalesForce Einstein lab published last week. Both of them requires understanding of MT, NNMT and purely attention-based NNMT. Since this first one is not too difficult to understand, I would just give you some background on NNMT first. 

When NNMT was first perceived. The original form starts with an Encoder of the text, convert it to what usually known as a "thought vector". The thought vector will then decode by the Decoder. In the original setting, both Encoder and Decoder are usually LSTMs

Then there is the idea of attention. Well, you can think of it as more like an extra layer just on the thought vector on the decoder side. The goal is decide how much attention you want to pay on the thought vector.

Now of course, people have then played with various architecture for these Enc-Dec structure. The first to notice is that such structure usually has a giant LSTM or CNN. But notice that no one really like them! LSTM is hard to parallelize and CNN can consume a lot of memories.

That makes Google work mid of this year, ["Attention is all you need" ](https://arxiv.org/pdf/1706.03762.pdf) a stunning and useful result. What the authors were saying is proposing is to just use the idea of attention to create a system, they call it transformer. There are multiple tricks to get it work but perhaps the most important one is "multi-head attentions", in a way this is like the concepts of channels in Convnet, but now instead of doing one single attention, we are now attend in multiple places. Each head will learn to attend differently.

Naturally the method is fast because you can also parallelize it, but then Google's researchers also find it to be *better* in the BLEU score. That's why top house are switching to purely attention-based method these days.

Now finally I can talk about what the Salesforce paper is about. In the original Google's paper, representation learned by multi-attention heads are only concatenate with each other to form one "supervector" But then the authors of the paper decide to use another set of weighting. This again, further improve the performance on WMT14 by 0.4 BLEU score, which is quite significant.

[einstein.ai](https://einstein.ai/research/weighted-transformer)

---

### [Non-Autoregressive Neural Machine Translation](https://einstein.ai/research/non-autoregressive-neural-machine-translation)

This is the second of the two papers from Salesforce, "Non-Autoregressive Neural Machine Translation" . Unlike the "Weighted Transformer, I don't believe it improves SOTA results. But then it introduces a cute idea into a purely attention-based NNMT, I would suggest you my previous post before you read on. 

Okay. The key idea introduced in the paper is fertility. So this is to address one of the issues introduced by a purely attention-based model introduced from "Attention is all you need". If you are doing translation, the translated word can 1) be expanded to multiple words, 2) transform to a totally different word location.

In the older world of statistical machine translation, or what we called IBM models. The latter model is called "Model 2" which decide the "absolute alignment" of source/target language pair. The former is called fertility model or "Model 3". Of course, in the world of NNMT, these two models were thought to be obsolete. Why not just use RNN in the Encoder/Decoder structure to solve the problem? (Btw, there are totally 5 types IBM Models. If you are into SMT, you should probably learn it up.)

But then in the world of purely attention-based NNMT, idea such as absolute alignment and fertility become important again. Because you don't have memory within your model. So in the original "Attention is all you need" paper, there is already the thought of "positional encoding" which is to model absolute alignment.

So the new Salesforce paper actually introduces another layer which brought back fertility. Instead of just feeding the output of encoder directly into the decoder. It will feed to a fertility layer to decide if a certain word should have higher fertility first. e.g. a fertility of 2 means that it should be copied twice. 0 means the word shouldn't be copy.

I think the cute thing about the paper is two-fold. One is that it is an obvious expansion of the whole idea of attention-based NNMT . Then there is the Socher's group is reintroducing classical SMT idea back to NNMT.

The result though is not working as well as the standard NNMT. As you can see in Table 1. There is still some degradation using the attention-based approach. That's perhaps why when the Google Research Blog mention the Salesforce results : it said "*towards* non-autoregressive translation". It implies that the results is not yet satisfying.

[einstein.ai](https://einstein.ai/research/non-autoregressive-neural-machine-translation)

---

### [Medical Image Segmentation Based on Multi-Modal Convolutional Neural Network: Study on Image Fusion Schemes](https://www.facebook.com/groups/aidl.ld/permalink/899349283563072/)

This is a well-written summary by one of our members. We decide to feature it here without further comments. So check it out! Only in our [Literature Discussion](https://www.facebook.com/groups/aidl.ld/?ref=bookmarks) group. 

[facebook.com](https://www.facebook.com/groups/aidl.ld/permalink/899349283563072/)

## Contemporary Classic

### [Deep Learning Architecture Diagrams](http://fastml.com/deep-learning-architecture-diagrams/)

This is a now classic article on architecture diagrams of deep learning. The section which criticizes Azimov Institute's infographics of deep learning should be a must-read for everyone. 

[fastml.com](http://fastml.com/deep-learning-architecture-diagrams/)
