---
title: "Learning Deep Learning: The \"Basic Five\" - Five Beginner Classes on Deep Learning"
date: 2017-05-13
categories: ["deep learning", "Machine Learning"]
tags: ["Andrew Ng", "computer vision", "David Silver", "deep learning", "Fei-fei Li", "Geoffrey Hinton", "Machine Learning", "NLP", "reinforcement learning", "Richard Socher", "unsupervised learning"]
---

# Learning Deep Learning: The "Basic Five" - Five Beginner Classes on Deep Learning

*[image not recovered: clem-onojeghuo-110878.jpg]*

By onojeghuo from Unsplash, CC0

I have been self-learning deep learning for a while, informally from 2013 when I first read Hinton's "[Deep Neural Networks for Acoustic Modeling in Speech Recognition](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/38131.pdf)" and through [Theano](http://deeplearning.net/software/theano/), more "formally" from various classes since the 2015 Summer when I got freshly promoted to [Principal Speech Architect](https://www.linkedin.com/notifications/) [5]. It's not an exaggeration that deep learning changed my life and career. I have been more active than my previous life. e.g. If you are reading this, you are probably directed from the very popular Facebook group, [AIDL](https://www.facebook.com/groups/DeepNetGroup/), which I admin.

So this article was written at the time I finished watching an older version on Richard Socher's cs224d on-line [1]. That, together with Ng's, Hinton's, Li and Karpathy's and Silvers's, are the 5 classes I recommended in my now widely-circulated "[Learning Deep Learning - My Top-Five List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)". I think it's fair to give these sets of classes a name - *Basic Five.* Because IMO, they are the first fives classes you should go through when you start learning deep learning.

In this post I will say a few words on why I chose these five classes as the *Five.* Compared to more established bloggers such as [Kapathy](http://karpathy.github.io/), [Olah](http://colah.github.io/) or [Denny Britz](https://github.com/dennybritz), I am more a learner in the space [2], experienced perhaps, yet still a learner. So this article and my others usually stress on *learning.* What you can learn from these classes? Less talk-about, but as important: what is the limitation of learning on-line? As a learner, I think these are interesting discussion, so here you go. 

# What are the* Five*?

Just to be clear, here is the classes I'd recommend: 
1. [Andrew Ng's Coursera Machine Learning](https://www.coursera.org/learn/machine-learning) - my [review](/grandjanitor/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/),
2. [Fei-Fei Li and Andrew Karpathy's Convolutional Neural Networks for Visual Recognition](http://cs231n.stanford.edu/) or Stanford cs231n 2015/2016,
3. [Richard Socher's Deep Learning and Natural Language Processing](http://cs224d.stanford.edu/) or Stanford cs224d,
4. [David Silver's Reinforcement Learning](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html),
5. [Hinton's Neural Network and Machine Learning](https://www.coursera.org/learn/neural-networks) - my [review](/grandjanitor/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/).

And the ranking is the same as I wrote in [Top-Five List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/). Out of the five, four has official video playlist published on-line for free[6]. With a small fee, you can finish the Ng's and Hinton's class with certification. 

# How much I actually Went Through the *Basic Five*

Many beginner articles usually come with gigantic set of links. The authors usually expect you to click through all of them (and learn through them?) When you scrutinize the list, it could amount to more than 100 hours of video watching, and perhaps up to 200 hours of work. I don't know about you, but I would suspect if the author really go through the list themselves.

So it's fair for me to first tell you what I've actually done with the *Basic Five* as of the first writing (May 13, 2017)

[table id=1 /]

This table is likely to update as I go deep into a certain class, but it should tell you the limitation of my reviews. For example, while I have watched through all the class videos, only on Ng's and Hinton's class I have finished the homework. That means my understanding on two of the three "[Stanford Trinities](http://aiplaybook.a16z.com/docs/reference/links)"[3] is weaker, nor my understanding of reinforcement learning is solid. Together with my work at Voci, the Hinton's class gives me stronger insight than average commenters on topics such as unsupervised learning. 

# Why The *Basic Five*? And Three Millennial Machine Learning Problems

Taking classes is for learning of course. The five classes certainly give you the basics, and if you love to learn the *fundamentals of deep learning.* And take a look of footnote [7]. The five are not the only classes I sit through last 1.5 years so their choice is not arbitrary. So oh yeah. Those are the stuffs you want to learn. Got it? That's my criterion. :)

But that's what other one thousand bloggers would tell you as well. I want to give you a more interesting reason. Here you go:

If you go back in time to the Year 2000. That was the time Google just launched their search engine, and there was no series of Google products and surely there was no Imagenet. What was the most difficult problems for machine learning? I think you would see three of them: 
1. Object classification,
2. Statistical machine learning,
3. Speech recognition.

So what's so special about these three problems then? If you think about that, back in 2000, all three were known to be hard problems. They represent three seemingly different data structures - 
1. Object classification - 2-dimensional, dense array of data
2. Statistical machine learning (SMT) - discrete symbols, seemingly related by loose rules human called grammars and translation rules
3. Automatic speech recognition (ASR)- 1-dimensional time series, has similarity to both object classification (through spectrogram), and loosely bound by rules such as dictionary and word grammar.

And you would recall all three problems have interest from the government, big institutions such as Big Four, and startup companies. If you master one of them, you can make a living. Moreover, once you learn them well, you can transfer the knowledge into other problems. For example, handwritten character recognition (HWR) resembles with ASR, and conversational agents work similarly as SMT. That just has to do with the three problems are great metaphor of many other machine learning problems.

Now, okay, let me tell one more thing: even now, there are people still (or trying to) make a living by solving these three problems. Because I never say they *are* *solved.* e.g. What about we increase the number of classes from 1000 to 5000? What about instead of Switchboard, we work on conference speech or speech from Youtube? What if I ask you to translate so well that even human cannot distinguish it? That should convince you, "Ah, if there is one method that could solve all these three problems, learning that method would be a *great idea!"*

And as you can guess, *deep learning* *is that one method* revolutionize all these three fields[4]. Now that's *why* you want to take the *Basic Five*. *Basic Five* is not meant to make you the top researchers in the field of deep learning, rather it teaches you just the basic. And at this point of your learning, knowing powerful template of solving problems is important. You would also find going through *Basic Five* makes you able to read majority of the deep learning problems these days.

So here's why I chose the *Five*, Ng's and NNML are the essential basics of deep learning. Li and Kaparthy's teaches you object classification to the state of the art. Whereas, Socher would teach you where deep learning is on NLP, it forays into SMT and ASR a little bit, but you have enough to start.

My explanation excludes Silver's reinforcement learning. That admittedly is the goat from the herd. I add Silver's class because increasingly RL is used in even traditionally supervised learning task. And of course, to know the place of RL, you need a solid understanding. Silver's class is perfect for the purpose. 

# What You Actually Learn

In a way, it also reflect what's really important when learning deep learning. So I will list out 8 points here, because they are repeated them among different courses. 
1. Basics of machine learning: this is mostly from Ng's class. But theme such bias-variance would be repeated in NNML and Silver's class.
2. Gradient descent: its variants (e.g. ADAM), its alternatives (e.g. second-order method), it's a never-ending study.
3. Backpropagation: how to view it? As optimizing function, as a computational graph, as flowing of gradient. Different classes give you different points of view. And don't skip them even if you learn it once.
4. Architecture: The big three family is DNN, CNN and RNN. Why some of them emerge and re-emerge in history. The detail of how they are trained and structured. None of the courses would teach you everything, but going through the five will teach you enough to survive
5. Image-specific technique: not just classification, but localization/detection/segmentation (as in cs231n 2016 L8, L13). Not just convolution, but "deconvolution" and why we don't like it is called "deconvolution". :)
6. NLP-specific techniques: word2vec, Glovec, how they were applied in NLP-problem such as sentiment classification
7. (Advanced) Basics of unsupervised learning; mainly from Hinton's, and mainly about techniques 5 years ago such as RBM, DBN, DBM and autoencoders, but they are the basics if you want to learn more advanced ideas such as GAN.
8. (Advanced) Basics of reinforcement learning: mainly from Silver's class, from the DP-based model to Monte-Carlo and TD.

# The Limitation of Autodidacts

By the time you finish the *Basic Five,* and if you genuinely learn something out of them. Recruiters would start to knock your door. What you think and write about deep learning would appeal to many people. Perhaps you start to answer questions on forums? Or you might even write LinkedIn articles which has many Likes.

All good, but be cautious! During my year of administering AIDL, I've seen many people who purportedly took many deep learning class, but upon few minutes of discussion, I can point out holes in their understanding. Some, after some probing, turned out only take 1 class in entirety. So they don't really grok deeper concept such as back propagation. In other words, they could still improve, but they just refuse to. No wonder, with the hype of deep learning, many smart fellows just choose to start a company or code without really taking time to grok the concepts well.

That's a pity. And all of us should be aware is that self-learning is limited. If you decide to take a formal education path, like going to grad schools, most of the time you will sit with people who are as smart as you and willing to point out your issues daily. So any of your weaknesses will be revealed sooner.

You should also be aware that as deep learning is hyping, your holes of misunderstanding is unlikely to be uncovered. That has nothing to do with whether you work in a job. Many companies just want to hire someone to work on a task, and expect you learn while working.

So what should you do then? I guess my first advice is *be humble*, be aware of *[Dunning-Kruger Effect](https://en.wikipedia.org/wiki/Dunning%E2%80%93Kruger_effect).* Self-learning usually give people an intoxicating feeling that they learn a lot. But learning a lot doesn't mean you know everything. There are always higher mountains, you are doing your own disservice to stop learning.

The second thought is you should try out your skill. e.g. It's one thing to know about CNN, it's another to run a training with Imagenet data. If you are smart, the former took a day. For the latter, it took much planning, a powerful machine, and some training to get even Alexnet trained.

My final advice is to talk with people and understand your own limitation. e.g. After reading many posts on AIDL, I notice that while many people understand object classification well enough, they don't really grasp the basics of object localization/detection. In fact, I didn't too even after the first parse of the videos. So what did I do? I just go through the videos on localization/detection again and again until I understand[8]. 

# After the *Basic Five.......*

So some of you would ask "What's next?" Yes, you finished all these classes, as if you can't learn any more! Shake that feeling off! There are tons of things you still want to learn. So I list out several directions you can go: 
- *Completionist:* As of the first writing, I still haven't really done all the homework on all five classes, notice that doing homework can really help your understand, so if you are like me, I would suggest you to go back to these homework and test your understanding.
- *Intermediate Five:*  You just learn the basics so it's time to learn the next level. I don't have a concrete ideas of the next 5 classes yet, but for now I would go with [Koller's Bayesian Network](https://www.coursera.org/learn/probabilistic-graphical-models), [Columbia's EdX CSMM 102x](https://www.edx.org/course/machine-learning-columbiax-csmm-102x-0), [Berkeley's Deep Reinforcement Learning](http://rll.berkeley.edu/deeprlcourse/#lecture-videos), [Udacity's Reinforcement Learning ](https://www.udacity.com/course/reinforcement-learning--ud600) and finally [Oxford Deep NLP 2017](https://github.com/oxford-cs-deepnlp-2017/lectures).
- *Drilling the Basics of Machine Learning:* So this goes another direction - let's work on your fundamentals. For that, you can any Math topics forever. I would say the more important and non-trivial parts perhaps Linear Algebra, Matrix Differentiation and Topology. Also check out this very good link on [how to learn college-level of Math](https://www.quantstart.com/articles/How-to-Learn-Advanced-Mathematics-Without-Heading-to-University-Part-1#year1-geometry).
- *Specialize on one field*: If you want to master just one single field out of the Three Millennial Machine Learning Problems I mentioned, it's important for you to just keep on looking at specialized classes on computer vision or NLP. Since I don't want to clutter this point, let's say I will discuss the relevant classes/material in future articles.
- *Writing:*  That's what many of you have been doing, and I think it helps further your understanding. One thing I would suggest is to always write something new and something you want to read yourself. For example, there are *too many* blog posts on *Computer Vision Using Tensorflow* in the world. So why not write one which is all about what people don't know? For example, practical transfer learning for *object detection*. Or what is deconvolution? Or literature review on some non-trivial architectures such as Mask-RCNN? And compare it with existing decoding-encoding structures. Writing this kind of articles takes more time, but remember quality trumps quantity.
- *Coding/Githubbing*: There is a lot of room for re-implementing ideas from papers and open source them. It is also a very useful skill as many companies need it to repeat many trendy deep learning techniques.
- *Research:*  If you genuinely understand deep learning, you might see many techniques need refinement. Indeed, currently there is plenty of opportunities to come up with better techniques. Of course, writing papers in the level of a professional researchers is tough and it's out of my scope. But only when you can publish, people would give you respect as part of the community.
- *Framework:* Hacking in C/C++ level of a framework is not for faint of hearts. But if you are my type who loves low-level coding, try to come up with a framework yourself could be a great idea to learn more. e.g. Check out [Darknet](https://pjreddie.com/darknet/), which is surprisingly C!

# Conclusion

So here you go. The complete *Basic Five,* what they are, why they were basic, and how you go from here. In a way, it's also a summary of what I learned so far from various classes since Jun 2015. As in my other posts, if I learn more in the future, I would keep this post updated. Hope this post keep you learning deep learning.

Arthur Chan

Footnote: [1] Before 2017, there was no coherent set of Socher's class available on-line. Sadly there was also no legitimate version. So the version I refer to is a mixture of 2015 and 2016 classes. Of course, you may find a legitimate [2017 version of cs224n](https://www.youtube.com/playlist?list=PL3FW7Lu3i5Jsnh1rnUwq_TcylNr7EkRe6) on Youtube.

[2] My genuine expertise is speech recognition, unfortunately that's not a topic I can share much due to IP issue.

[3] "Stanford Trinity" is a term I learned from the AI Playbook List from [Andreseen Howoritz's list](http://aiplaybook.a16z.com/docs/reference/links).

[4] Some of you (e.g. from AIDL) would jump up and say "No way! I thought that NLP wasn't solved by deep learning yet!" That's because you are one lost soul and misinformed by misinformed blog post. ASR is the first field being tackled by deep learning, and it dated back to 2010. And most systems you see in SMT are seq2seq based.

[5] I was in the business of speech recognition from 1998 when I worked on voice-activated project for my undergraduate degree back in HKUST. It was a mess, but that's how I started.

[6] And the last one, you may always search it through youtube. Of course, it is not legit for me to share it here.

[7] I also audit, 
- [MIT Self Driving 6.S094](http://selfdrivingcars.mit.edu/)
- John Schulman's 4 Lectures of Reinforcement Learning

I also took, 
- [Radev's Natural Language Processing](https://www.coursera.org/learn/natural-language-processing), which leans on ML as well. ([my review](/grandjanitor/2015/12/22/radevs-coursera-introduction-to-natural-language-processing-a-review/))
- 3 out of 10 [Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science).
- The first class of UW's [Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning).

[8] It's still a subject that \*I\* could explore. For example, just the logistic seems to be hard enough to setup.

\* \* \* If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).

\* \* \*

History:

20170513: First version finished

20170514: Fixed many typos. Rewrite/add some paragraphs. Ready to publish.

\-------------

If you like this post, you might also like:

http://thegrandjanitor.com/2016/08/15/learning-deep-learning-my-top-five-resource/

http://thegrandjanitor.com/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/

http://thegrandjanitor.com/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/

http://thegrandjanitor.com/2016/05/21/learning-machine-learning-some-personal-experience/
