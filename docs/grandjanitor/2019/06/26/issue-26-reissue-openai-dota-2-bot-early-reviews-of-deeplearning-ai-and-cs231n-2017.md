---
title: "Issue #26 - Reissue: OpenAI DotA-2 Bot, Early Reviews of deeplearning.ai and cs231n 2017"
date: 2019-06-26
---

# Issue #26 - Reissue: OpenAI DotA-2 Bot, Early Reviews of deeplearning.ai and cs231n 2017

# [Issue 26 *August 19th 2017* ](http://aidl.io/issues/26/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Woohoo! As deeplearning.ai launched last week, we started to see more reviews of the class. We will look at one by Arvind Naragaj. We will also zero in on one of the optional series within the class, called "Heroes of Deep Learning". This week, we will look at the Prof. Hinton interview by Prof Ng.

Oh, how about the OpenAI DotA-2 bot? Has it conquered the world of DotA-2 yet? From what we gather so far it doesn't seem to be the case..... So let's take a look in our Fact-checking section.

Other than deeplearning.ai and DotA-2, Stanford also just released the latest videos from cs231n 2017. So check out our Open Source Section!

---

As always, if you like our newsletter, please subscribe/forward to your colleagues!

Artificial Intelligence and Deep Learning Weekly

---

### Reissuing of Issue 25

Due to a technical problem we encountered yesterday, we decide to reissue Issue 25 today. We apologize for any inconvenience.

Artificial Intelligence and Deep Learning Weekly

## News

### [Prof. Andrew Ng is Also Raising 150m AI Fund](https://techcrunch.com/2017/08/15/andrew-ng-is-raising-a-150m-ai-fund/amp/)

It doesn't come as a surprise to us as financing is a core component of building the AI ecosystem. We don't have much detail yet. Other have questioned how the fund will differentiate itself from other funds such as Element.AI or Gradient as the proliferation of AI-focused funds continues.

We are of a different opinion - Prof. Andrew Ng is the secret sauce here. Having Prof. Ng as an investor is in itself a very positive signal that the AI is deep and real (as opposed to many startups that call themselves AI startups), and that would attract talent and follow-on investors.

[techcrunch.com](https://techcrunch.com/2017/08/15/andrew-ng-is-raising-a-150m-ai-fund/amp/)

## Factchecking

### OpenAI's Dota 2 Bot In Perspective

One of the biggest news last week is perhaps an OpenAI bot was able to beat pro [Dota 2](http://www.dota2.com/play/) player [Dendi](https://en.wikipedia.org/wiki/Dendi_%28Dota_player)) (See Footnote 1). Public outlets rush to report the news and many of them reminded us how dangerous AI can become. And as you might also know, Elon Musk who launch OpenAI, [says](https://twitter.com/elonmusk/status/896163163581825025?ref_src=twsrc%5Etfw&ref_url=https%3A%2F%2Fwww.theverge.com%2F2017%2F8%2F14%2F16141938%2Fdota-2-openai-bots-elon-musk-artificial-intelligence), 

> OpenAI first ever to defeat world's best players in competitive eSports. Vastly more complex than traditional board games like chess & Go.

And remember in [Issue 24](http://aidl.io/issues/24#start), we looked at DeepMind/Blizaard Starcraft II environment, and we said [on using reinforcement learning on SCII], 

> So far, DeepMind researchers are still perplexed by the problem - and all RL algorithms so far cannot beat the built in AI agents.

So had we perceived the status of technology incorrectly? We are certainly not the only group who felt surprised. AI researcher, [Danny Britz](http://www.wildml.com/about/) also feels the same. So is SalesForce researcher, [Stephen Merity](https://twitter.com/Smerity/)

Since this issue is already discussed quite well by Britz' [blog post](http://www.wildml.com/2017/08/hype-or-not-some-perspective-on-openais-dota-2-bot/) and Merity's tweets' [discussion](https://twitter.com/Smerity/status/897959187480625153). The Verge [piece](https://www.theverge.com/2017/8/14/16143392/dota-ai-openai-bot-win-elon-musk) is pretty good if you want a less technical piece. OpenAI researchers also wrote two messages on the task. ([Part I](https://blog.openai.com/dota-2/) and [Part II](https://blog.openai.com/more-on-dota-2/))

So we will just extract several important take-aways here: 
1. A multiplayer online battle arena (MOBA) is not an real-time strategy (RTS) Game. e.g. League of Legends or Dota 2 are MOBA, whereas Starcraft I,II are RTS. They look the same, but computationally they can be very different. A MOBA has significantly fewer actions to choose from because you only control one single character. Whereas RTS require you to control not only the Heroes, and it requires you to control all the buildings.
2. OpenAI bot is a 1v1 bot. And A MOBA 1v1 game is very different from a MOBA 5v5. Most tournament game in DotA-2 is actually 5v5, So the machine has to deal with a team of 5 coordinated players. So even OpenAI researchers opine in their [post](https://blog.openai.com/more-on-dota-2/): "1v1 is complicated, but 5v5 is an ocean of complexity." Also playing a MOBA 1v1 game usually mean you and your opponent will use the same lane, so reflex of the player will be the key. Of course, in this case machines have an huge edge.
3. Then you should observe that DotA-2 API actually provide a lot of vital information which give advantage to the bot. For example, as the Verge piece points out - distance information can be easily access and give advantages to [machines](https://developer.valvesoftware.com/wiki/Dota_Bot_Scripting), which human doesn't have such advantage.
4. Consider all these, many also observe that Open-AI engine has many human element involved. The e.g. Heroes was chosen manually out of the 110+ choices. [Shadow Fiend](https://dota2.gamepedia.com/Shadow_Fiend) was chosen. So the character picking is not done by machine. Then there is a key technique of creep blocking, which allows creep to reinforce a defense. Turns out it is trained separately.

So all of these 4 points should make you convince that we seem to be quite far away from beating general RTS games, not to say making Skynet in general.

So how do we see it? Our opinion is very similar to Britz - while that we believe popular outlets and Musk's comment are over the top. By its own, OpenAI DotA-2Bot is still an impressive engineering project. Their status is currently comparable to say DeepBlue before it met Kasparov. There are some known issues, such as many players rumored that they can beat the bot by a technique called [creep-control](https://dota2.gamepedia.com/Creep_control_techniques). But it may be a bug in the engine, and expect OpenAI researchers would fix it one day.

On the other hand, you should still notice that beating DotA-2 in 5v5 and a general RTS game are still faraway from us. Hopefully saying so would stop your nightmares (and frankly, curb your enthusiasm) of an AI-powered doomsday machine.

Footnote 
1. If this is the first time you heard of DotA-2, check out this [video](https://www.youtube.com/watch?v=HXayKdseygg) for the gameplay?

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [AI Heroes of Deep Learning - Geoffrey Hinton](/grandjanitor/2017/08/13/quick-impression-on-deeplearning-ai-heroes-of-deep-learning-geoffrey-hinton/?fref=gc)

This piece is Arthur's impression of the first video (long, 40 mins) of AI Heroes of Deep Learning which interviews of Geoffrey Hinton. Unlike other parts of deeplearning.ai class, "AI Heroes of Deep Learning" series has more research discussion, which is more suitable for working practitioners of deep learning.

[thegrandjanitor.com](/grandjanitor/2017/08/13/quick-impression-on-deeplearning-ai-heroes-of-deep-learning-geoffrey-hinton/?fref=gc)

---

### [Early Review of Deeplearning.ai Specialization](https://medium.com/towards-data-science/thoughts-after-taking-the-deeplearning-ai-courses-8568f132153)

This is an early review of deeplearing.ai from Arvind Nagaraj. It's also the first review of the class. The part we like is his comparison between fast.ai and the deeplearning.ai. In a nutshell, fast.ai is more top-down approach of teaching - it teaches you how to run the script first before describing the internals. Whereas Prof. Ng's deeplearning.ai is more a bottom-up approach - it first teaches you the internals, then build up from there.

The specialization is still very new. So expect more reviews will come soon. Another good one we haven't cover is Gautam Karmarker's [post](https://medium.com/@gautam.karmakar/my-experience-with-new-deep-learning-course-from-deeplearning-ai-coursera-585c6997401f), but check it out!

[medium.com](https://medium.com/towards-data-science/thoughts-after-taking-the-deeplearning-ai-courses-8568f132153)

## Open Source

### [Stanford cs231n 2017 videos](https://www.youtube.com/playlist?list=PL3FW7Lu3i5JvHM8ljYj-zLfQRF3EO8sYv&app=desktop)

cs231n 2017 is finally released to the public. Compare to the class at 2016, there are three new lectures sets: Lecture 13 on generative models, Lecture 14 on Deep Reinforcement learning and Lecture 16 on adversarial training. That makes it a must-watch sets of videos even if you have seen it once.

[youtube.com](https://www.youtube.com/playlist?list=PL3FW7Lu3i5JvHM8ljYj-zLfQRF3EO8sYv&app=desktop)

---

### [Tensorflow v1.3 Released](https://github.com/tensorflow/tensorflow/releases/tag/v1.3.0)

In our view, this is more a release with upgrades such as adding new estimators, and perhaps the last pre-build with cuDNN 6.0. (v1.4 will pre-build by cuDNN 7.0.) [Dustin Tran on twitter](https://twitter.com/dustinvtran) also mentioned that this is the first time tf.distribution. According to Tran, so far it doesn't break his very interesting toolkit, [Edward](http://edwardlib.org/).

[github.com](https://github.com/tensorflow/tensorflow/releases/tag/v1.3.0)

---

### [All About NLP](http://tangra.cs.yale.edu/newaan/)

[Prof. Dragomir Radev](http://cpsc.yale.edu/people/dragomir-radev) shared us a search engine by Yale [LILY group](https://yale-lily.github.io/) which has all useful information you need to learn NLP. You can also upvote/downvote a resource. Sounds quite nifty, so check it out!

[yale.edu](http://tangra.cs.yale.edu/newaan/)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing)

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## Paper/Thesis Review

### [Recent trend in NLP](https://arxiv.org/abs/1708.02709v2)

In this survey paper from University of Singapore, the authors gave great explanation on several well-used techniques in current NLP application of deep learning. It also include several STOA results in several tasks such as POS tagging, translation etc.

[arxiv.org](https://arxiv.org/abs/1708.02709v2)

---

### [Paper Version of Tensorflow Playground](https://arxiv.org/pdf/1708.03788v1.pdf)

This is the paper version of the well-known [Tensorflow Playground](http://playground.tensorflow.org/#activation=tanh&batchSize=10&dataset=circle®Dataset=reg-plane&learningRate=0.03®ularizationRate=0&noise=0&networkShape=4,2&seed=0.67194&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false) which provides great visualization on neural network training.

[arxiv.org](https://arxiv.org/pdf/1708.03788v1.pdf)
