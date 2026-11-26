---
title: "AIDL Weekly Issue #6 - Ng's Departure, Mask-RCNN and Intel's AIPG"
date: 2019-05-23
---

# AIDL Weekly Issue #6 - Ng's Departure, Mask-RCNN and Intel's AIPG

### Thoughts From Your Humble Curators

The biggest AI/DL news last week is definitely Andrew Ng's departure from Baidu so naturally it is the top news this issue. 

Other than Ng's departure, last week was filled with news on interesting researches and source code: 
- OpenAI's research on multiple agents led to emergence of a simple language,
- FAIR's Kaiming He proposed Mask-RCNN, which shatters previous records,
- Distill, a new on-line journal for deep learning,
- Google's Syntaxnet upgrade,
- Google's new skip-thought model.

Enjoy!

Artificial Intelligence and Deep Learning Weekly

## News

### [Andrew Ng Leaving Baidu](https://medium.com/@andrewng/opening-a-new-chapter-of-my-work-in-ai-c6a4d1595d7b#.x9b4oswqq)

Perhaps the biggest news this week: Andrew Ng is leaving Baidu. As all of you know, Ng started Coursera, taught the perhaps most well-known MOOC, [Machine Learning](https://www.coursera.org/learn/machine-learning), found Google Brain, and later lead important researches in Baidu such as speech recognition. No one will doubt he is one of the giants in today's world of deep learning. So it comes to be a surprise for his departure and leave many speculations on his next move. He said in his Medium post, he would "explore new ways to support all of you in the global AI community". That makes you wonder, what can be bigger than Google or Baidu? 

Our speculation is that Ng might join an initiative such as OpenAI which is a joint effort from multiple companies, or he starts a new research initiative, similar to his own Coursera, or Fei-Fei Li's Imagenet project, both create tremendous values to the community.

Regardless of his choice, we wish the good Professor well in his new journey. There are still many unsolved problems in machine learning. We are waiting for a world-class talent like Andrew to help solving them.

[medium.com](https://medium.com/@andrewng/opening-a-new-chapter-of-my-work-in-ai-c6a4d1595d7b#.x9b4oswqq)

---

### [Intel's Artificial Intelligence Product Groups ](https://www.forbes.com/sites/patrickmoorhead/2017/03/23/intel-forms-new-ai-group-reporting-directly-to-ceo-brian-krzanich/#4c88e1ea462b)

As many of you know, Intel has been acquiring different deep learning startups such as [Nervanna](https://www.nervanasys.com/) and [Mobileye](http://www.mobileye.com/en-us/). Now Intel is aligning all these efforts under one single group, Artificial Intelligence Product Groups (AIPG), which will be reporting directly to the CEO's Brian Krzanich. 

While Intel is behind from its competitors such as Nvidia in the deep-learning market. Their recent effort of rounding up helps through acquisition is impressive. Perhaps the more difficult technical problem here is how Intel would assimilate different diverse pieces of technology together. For example, it's thinkable that with technology of both Nervanna and Mobileye, we could have a very fast system on collision avoidance system. This will, in turn, gives room to further machine learning performance improvement, as slower methods are usually more accurate. All these interesting potential can only happen when multiple existing systems can work together. It would take Intel time and proper management to move things forward.

It will also be interesting to see how Intel can wrest some marketshare away in the low-power embedded space from ARM which is rumored to be furiously building/buying their own AI stack. The AI future will likely be hybridized - with AI training and inference happening on both server and client side. There may be some network effects in ability to own both sides.

[forbes.com](https://www.forbes.com/sites/patrickmoorhead/2017/03/23/intel-forms-new-ai-group-reporting-directly-to-ceo-brian-krzanich/#4c88e1ea462b)

---

### [Uber's Leaked Disengagement Report](https://www.recode.net/2017/3/16/14938116/uber-travis-kalanick-self-driving-internal-metrics-slow-progress)

Recode obtained Uber's disengagement number last week, and we should feel alarmed by one statistics: miles per intervention. That is how often drivers need to disengage the self-driving system and intervene driving themselves. Uber has an alarmingly low number: 0.8miles. That is for less than 1 mile, the safety driver has to take over the driving. 

Compare this number from what we know about [Waymo](http://www.theverge.com/2017/2/1/14474790/google-waymo-self-driving-car-disengagement-dmv-california), it shows that Uber still has quite a catch up to do: Waymo's vehicles are now in the disengagement rate of 0.2 disengagement per 1000 miles. That means the safety driver only has take over every *5000 miles*.

Btw, disengagement rate is in [public record](https://www.dmv.ca.gov/portal/dmv/detail/vr/autonomous/disengagement_report_2016) in the State of California. I couldn't find similar reports at Pennsylvania yet, apparently some consumer groups has urged Uber to release such reports around [a year ago](http://www.consumerwatchdog.org/newsrelease/consumer-watchdog-tells-uber-make-robot-car-test-details-public-poses-10-key-questions).

[recode.net](https://www.recode.net/2017/3/16/14938116/uber-travis-kalanick-self-driving-internal-metrics-slow-progress)

## Blog Posts

### [Distill](https://research.googleblog.com/2017/03/distill-supporting-clarity-in-machine.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed:+blogspot/gJZg+%28Official+Google+Research+Blog%29&utm_content=Netvibes)

Distill is a new on-line journal on deep learning. There are many superstar authors such as Andrej Kapathy and Chris Olah, both are known to explain with clarify and can produce great visualization of deep learning techniques. The effort is jointly supported by OpenAI and DeepMind so you can expect the best deep learning talent would publish on the site. 

[googleblog.com](https://research.googleblog.com/2017/03/distill-supporting-clarity-in-machine.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed:+blogspot/gJZg+%28Official+Google+Research+Blog%29&utm_content=Netvibes)

---

### [OpenAI : Learning to Communicate for Agents](https://openai.com/blog/learning-to-communicate/)

Similar to DeepMind, OpenAI has established itself to be a power house of deep learning research. My impression is that OpenAI is nurturing an environment of reinforcement learning, and this research is one example. 

What the authors try to do is see if a simple language can emerged through interactions of agents. It is one of these stories, if picked up by popular outlets, which can get sensationalized easily. So it deserves to take a closer look. For example, you would hope that if you feed in English words, then the agents would just automatically come up with an English sentence. That's not the case. OpenAI's researchers found that sometimes agent will use one single word to represent entire sentence. While this is very nice in term of efficiency, it is very difficult for human to interpret the meaning of the agent's language.

Other than this technicality though, I(Arthur Chan) do find the work fascinating, it was inspired by the Nature's paper, ["the evolution of syntactic communication"](http://www.nature.com/nature/journal/v404/n6777/full/404495a0.html). Just from the sound-byte, if one go ahead to tweak the optimization criterion, it's possible to resolve the interpretability issue. Also check out the [arxiv paper](https://arxiv.org/pdf/1703.04908.pdf), it provides more detail on how the implementation is done, including using [Grumbel-Softmax](https://arxiv.org/abs/1611.01144) trick in "soften" a categorical distribution.

[openai.com](https://openai.com/blog/learning-to-communicate/)

---

[*[image not recovered: twenty_by_nine_extra_large_c9aa4803-8dce-4aa6-b80d-bf156ef43630.png]*](https://arxiv.org/abs/1703.06870) 

### [FAIR's Mask RCNN by Kaiming He](https://arxiv.org/abs/1703.06870)

Kaiming He, with the Resnet fame, surprised us again last week, by proposing yet another simple, but innovative Convnet architecture to the field. This time the game is instance segmentation. As we discussed in [Issue #4](http://aidl.io/issues/4#start), instance segmentation tries to come up with individual instances and mask for a particular object. That's different from semantic segmentation, in which a pixel-by-pixel decision is make on the regions of the image. 

If you have taken [cs231n 2016](http://kaiminghe.com/) (Lecture 13), you would learn that most instance segmentation system have a very similar processing pipeline as object detection: conceptually the image first went through object proposals, and then classification layers would run upon the different regions of interest (RoI)s which come up with both the classification score and bounding box. That, as many of you know is the basic structure of [RCNN](https://arxiv.org/abs/1311.2524). Of course, the original authors later on come up with an end-to-end version of RCNN, [Faster RCNN](https://arxiv.org/abs/1506.01497), in which the object proposals were done by region proposal network (RPN).

So most instance segmentation use very similar pipeline as Faster-RCNN, but the glitch is there is usually a further stage called "region refinement", e.g. as in ["Simultaneous Detection and Segmentation"](https://biomedicalcomputervision.uniandes.edu.co/images/webpage/publications/hagm_eccv2014.pdf) by Bharath Hariharan. The purpose is to further refine the mask to fit the RoI. You can imagine doing so would slow down the speed of the system.

Saying this much, the first thing you should appreciate He's architecture is that he has practically done away the region refinement stage, and make the mask to be trainable with the Faster-RCNN framework. This is surprisingly simple. So the next question is why such simple architecture never emerged until now?

My guess is two, first is perhaps instance segmentation is still a relatively new task. Just like other tasks, people are still searching for a good end-to-end framework.

The second one is perhaps more technical: Normal faster-RCNN inherit a hard quantized RoIpool layer from [fast-RCNN](https://arxiv.org/pdf/1504.08083.pdf) which was found to be suitable for extracting a feature for each RoI. It was suitable in detection task, but it is perhaps too coarse for pixel-based decision. Th technical improvement from the authors is that they come up with a better layer RoIalign, this significantly improves the network performance for creating mask, yet only make the system slightly slower than Faster RCNN (now at 5 fps).

Perhaps the most impressive part is its segmentation performance, it crushes all existing benchmarks on Coco. Let's wait for its github code release, and we will wait and see how such architecture would be used in the future.

[arxiv.org](https://arxiv.org/abs/1703.06870)

## Open Source

### [Google releases new skip thought model](https://github.com/tensorflow/models/tree/master/skip_thoughts)

Here is an interesting piece of code shared by Google, on the [skip thoughts model](https://papers.nips.cc/paper/5950-skip-thought-vectors.pdf) first suggested by Kiros et al. The idea is similar to [skip-gram](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf), but in the sentence level. Given a sentence, a skip-thought model would predict a sentence which has the closest semantic and syntactical property. It's a powerful technique because a similar sentence can be used as an input to upper layer such as classification. More importantly, the resource can be unlabelled and much lower the cost. 

The Google's recipe contain a Tensorflow-based recipe which can train, evaluate your own skip-thought models.

[github.com](https://github.com/tensorflow/models/tree/master/skip_thoughts)

---

### [Google upgrade SyntaxNet](https://research.googleblog.com/2017/03/an-upgrade-to-syntaxnet-new-models-and.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+blogspot%2FgJZg+%28Official+Google+Research+Blog%29&utm_content=Netvibes)

Syntaxnet is interesting piece of technology, it is a [dependency parser](https://en.wikipedia.org/wiki/Dependency_grammar) and if you know a bit about NLP parsing technology, it gives great speed-accuracy trade-off in parsing. When I first learned it in [Dragomir Radev's Coursera class](https://www.coursera.org/learn/natural-language-processing), I found it fairly interesting because it allows using machine learning method to solve parsing. 

When Syntaxnet was first released, it was billed as "most accurate in the world". So there were many articles to put in context. The one I like most is from [Matthew Honnibal](https://www.linkedin.com/in/honnibal/) of [explosion.ai](https://explosion.ai/) who wrote the spaCY NLP library. One thing Honnibal pointed out is that [Syntaxnet only inch forward](https://explosion.ai/blog/syntaxnet-in-context) from academic research. So what Google did was more the legwork to make such parser available to general public.

So how should we see this upgrade of syntaxnet? I think my view is similar to Honnibal's one year ago. It looks like Google has done a good job to expand syntaxnet to train character-based model easier. This is crucial for morphologically rich languages such as Russian. Google dubbed models with such capability as [ParseySaurus](https://github.com/tensorflow/models/blob/master/syntaxnet/g3doc/conll2017/README.md). Google's result was tested at this year [CoNLL](http://www.conll.org/) for 45 languages. Such capability is interesting, but probably not too far away from academic researchers. (I wonder what will Honniabal say now.)

Regardless, I appreciate Google's continuous effort of open-sourcing their technology. So check it out and see how well you can parse Russian now. :)

[googleblog.com](https://research.googleblog.com/2017/03/an-upgrade-to-syntaxnet-new-models-and.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+blogspot%2FgJZg+%28Official+Google+Research+Blog%29&utm_content=Netvibes)

## Video

### [AIDL Office Hour session with Dashbot and Fireflies.ai founders.](https://www.youtube.com/watch?v=-8OaZI9sM9A)

This week we talked with [Fireflies](https://bots.directory/slack/fireflies_ai) founder, [Sam Udotong](https://www.linkedin.com/in/sudotong/) and [Dashbot](https://www.dashbot.io/)'s founder [Arte Meritt](https://www.linkedin.com/in/artemerritt/). Waikit and I(Arthur Chan) came up with a lot of questions for Sam and Arte, and they proved to be very interesting panel. 

Some highlights: 
- Fireflies uses deep NLP to classify if a certain message is task related or not.
- Dashbot works with multiple platforms, and Arte gave many interesting insights on the difference between different platforms.
- Waikit asked how both founders feel about the future of chatbots in the next 5 years.
- Many of us working on chatbot because we want to achieve some kind of artificial general intelligence (AGI), but as we work on the problem for a while, we know it is infeasible in our time. So I asked towards the end of the video: "Anything other than AGI, what are the tasks you want to automate the most?" And I think both founders gave me good and practical answers.

[youtube.com](https://www.youtube.com/watch?v=-8OaZI9sM9A)

## Book Review

### "Deep Learning" by Ian GoodFellow et al

I (Arthur) have some leisure lately to browse ["Deep Learning"](https://mitpress.mit.edu/books/deep-learning) by Goodfellow for the first time. Since it is known as the bible of deep learning, I decide to write a short afterthought post, they are in point form and not too structured. 
- If you want to learn the zen of deep learning, "Deep Learning" is the book. In a nutshell, "Deep Learning" is an introductory style text book on nearly every contemporary fields in deep learning. It has a thorough chapter covered Backprop, perhaps best introductory material on SGD, computational graph and Convnet. So the book is very suitable for those who want to further their knowledge after going through 4-5 introductory DL classes.
- Chapter 2 is supposed to go through the basic Math, but it's unlikely to cover everything the book requires. PRML Chapter 6 seems to be a good preliminary before you start reading the book. If you don't feel comfortable about matrix calculus, perhaps you want to read "Matrix Algebra" by Abadir as well.
- There are three parts of the book, Part 1 is all about the basics: math, basic ML, backprop, SGD and such. Part 2 is about how DL is used in real-life applications, Part 3 is about research topics such as E.M. and graphical model in deep learning, or generative models. All three parts deserve your time. The Math and general ML in Part 1 may be better replaced by more technical text such as PRML. But then the rest of the materials are deeper than the popular DL classes. You will also find relevant citations easily.
- I enjoyed Part 1 and 2 a lot, mostly because they are deeper and fill me with interesting details. What about Part 3? While I don't quite grok all the Math, Part 3 is strangely inspiring. For example, I notice a comparison of graphical models and NN. There is also how E.M. is used in latent model. Of course, there is an extensive survey on generative models. It covers difficult models such as deep Boltmann machine, spike-and-slab RBM and many variations. Reading Part 3 makes me want to learn classical machinelearning techniques, such as mixture models and graphical models better.
- So I will say you will enjoy Part 3 if you are 1) a DL researcher in unsupervised learning and generative model or 2) someone wants to squeeze out the last bit of performance through pre-training, 3) someone who want to compare other deep methods such as mixture models or graphical model and NN.

Anyway, that's what I have now. May be I will summarize in a blog post later on, but enjoy these random thoughts for now. 

Original version from my (Arthur's) [blog post](/grandjanitor/2017/03/10/some-quick-impression-of-browsing-deep-learning/).

Artificial Intelligence and Deep Learning Weekly
