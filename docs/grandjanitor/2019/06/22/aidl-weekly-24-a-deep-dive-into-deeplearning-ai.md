---
title: "AIDL Weekly #24 - A Deep Dive Into deeplearning.ai"
date: 2019-06-22
---

# AIDL Weekly #24 - A Deep Dive Into deeplearning.ai

# [Issue 24 *August 11th 2017* ](http://aidl.io/issues/24/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Happy Summer (for those in the Northern Hemi anyway)! We were off last week and the past few weeks have proved very eventful. So we have lots of material for you in this issue.

The biggest headline is we finally know what deeplearning.ai is. We took a quick look at the curriculum. For example, what does the course covers, is it worthwhile to take? How does it compare to other similar on-line classes? Such as Hinton NNML, cs231n and cs224n? We wrote a long and detail piece for you this issue.

Then perhaps now an old (fake) news, you might have heard the claim "Facebook kills AI agents which create its own language." We looked into this in Issue 18 and 23. Since then, Gizmodo has debunked it, Snope has debunked it, and even Facebook researchers came out to clarify what it was all about. So it became a much bigger deal than your normal fake news. Since The Weekly is one of the earliest one to debunk the claim, we present our own take on the matter below.

Other than deeplearning.ai and our fact-checking, we have 9 more items including some cool topics like audio super-resolution, DeepMind/Blizzard Starcraft API+Database. Shallow network can work as well as a deep one, so we link to a paper on that too!

---

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues/friends!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [deeplearning.ai - A Closer Look At Prof. Andrew Ng's Deep Learning Course](https://www.deeplearning.ai/)

By now, we all know that deeplearning.ai is a new series of courses, or specialization, developed by Prof. Andrew Ng. First off, we really appreciate Prof. Ng to create a new deep learning class right after he left the industry. One of us (Arthur) has quickly browsed through the curriculum of Course 1 to 3, here are some notes: 
- Only Course 1 to 3 are published now, they are short classes, more like 2-4 weeks. It feels like the [JHU Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science) and it feels good for beginners. Assume that Course 4 and 5 are long, say 4 weeks. So we are talking about 17 weeks of study.
- Unlike the standard Ng's ML class, python numpy is the default language. That's good in our view because close to 80-90% of practitioners are using python-based frameworks and knowledge of numpy is always very useful.
- Course 1-3 has around 3 weeks of curriculum overlapped with "Intro to Machine Learning" Lecture 2-3. But you should still check the course out even if you have some ML background. The course helps you to see other ML techniques from the eyes of a DL researcher. For example, Course 1 would guide you how to optimize a logistic regressor with back-prop like algorithm.
- Course 2 is about optimization, there we're introduced Tensorflow.
- Course 3 is more about how to setup a deep learning system pipeline. While it is only two weeks long, we find this Course the most exciting because we can hear what Prof. Ng thinks about DL after his years in industry.
- Course 4 and 5 are about CNN and RNN respectively, they are not yet published. From the outline so far, they are good preliminary classes before you take cs231n or cs224n.
- So our general impression here is that the specialization is more a comprehensive class, comparable with Hugo Larochelle's Lectures, as well as Hinton's NNML. Yet the latter two classes are known to be more difficult. Hinton's class in particular, are known to confuse even PhDs. So that shows one of the values of this new DL class: it is a great transition from "Intro to ML" to more difficult classes such as Hinton's.
- But how does it compared with other similar course such as Udacity's DL nanodegree then? We are not sure yet, but the price seems to be more reasonable if you go through the Coursera route. Assume we are talking about 5 months of study, you are paying $245. Compare to Udacity's price tag of $549. Ng's specialization looks like a bargain.
- Better than that: many of you Weekly readers are likely to take many other courses before considering Ng's class. In that case, you would find finishing the class faster than you thought. That also mean, you can spend *less than $245* on the class.
- We also found that many existing beginner classes advocate too much on running scripts, but avoid linking more fundamental concepts such as bias/variance with DL. Or go deep to describe models such as Convnet and RNN. cs231n did a good job on Convnet, and cs224n teach you RNN. But they seem to be more difficult than Ng or Udacity's class. So again, Ng's class sounds like a great transition class.
- Throughout the class, there are interviews with luminaries in DL community, including Prof. Hinton, Dr. Ian Goodfellow and Dr. Andrej Karpathy. Just listening to them may worth the $49 price tag.

Our current take: *We are going to take the class ourselves.* And we highly recommend this class to any aspiring students of deep learning.

[deeplearning.ai](https://www.deeplearning.ai/)

## Factchecking

### [A Closer Look at The Claim "Facebook kills Agents which Create its Own Language"](http://gizmodo.com/no-facebook-did-not-panic-and-shut-down-an-ai-program-1797414922)

As we fact-checked in Issue [18](http://aidl.io/issues/18#start) and [23](http://aidl.io/issues/23#start), we rated the claim 

> Facebook kills Agents which Create Its Own Language.

as **false**. And as you might know, the faked news has spread to 30+ outlets which stir the community.

Since the Weekly has been tracking this issue much earlier than other outlets (Gizmodo is the first popular outlet call the faked news out), we believe it's a good idea to give you our take on the issue, especially given all information we know. You can think of this piece as more a fact-checking from a technical perspective. You can use as a supplement of the [Snope's piece](http://www.snopes.com/facebook-ai-developed-own-language/).

Let's separate the issue into few aspects:

1, *Does Facebook kills an A.I. agent at all?*

Of course, this is the most ridiculous part of the claim. For starter, most of these "agents" are really just Linux processes. So..... you can just stop them by using the Linux command *kill*. The worst case.... *kill -9* or *kill -9 -r*? (See Footnote [1])

2, *What Language does AI Agents Generated and The Source*

All outlets, seem to point to couple of sources, or the original articles. As far as we know, none of these sources had quoted academic work which is directly the subject matter. For convenience, let's call these source articles to be "The Source" (Also see Footnote [2]). The Source apparently has conducted original research and interview with Facebook researchers. Perhaps the more stunning part is there are printouts of how the machine dialogue look like. For example. Some of the machine dialogue looks like 

> Bob: "i can i i everything else"
>
>
>
> Alice: "balls have zero to me to me to me to me ....."

That does explain why many outlets sensationalized this piece, because while the dialogue is still English (as we explained in Issue #18), it does look like codeword, rather than English.

Where does the printout comes from? It's not difficult to guess - it comes from the open source code of ["End-to-End Negotiator"](https://github.com/facebookresearch/end-to-end-negotiator) But then the example from github we can find there looks much more benign: 

> Human : hi i want the hats and the balls
>
>
>
> Alice : i will take the balls and book &lt;eos&gt;
>
>
>
> Human : no i need the balls
>
>
>
> Alice : i will take the balls and book &lt;eos&gt;

So one plausible explanation here is that someone has played with the open source code, and they happened to create a scary looking dialogue. Th question, of course, are these dialogue generated by FB researchers? or does FB researchers just provide The Source the dialogue? Here is the part we are not sure. Because the Source does quote words from Facebook's researcher (see Footnote [3]), so it's possible.

3, *What is Facebook's take?*

Since the event, Prof. Dhruv Batras has post a [status at July 31](https://www.facebook.com/dhruv.batra.dbatra/posts/1943791229195215) in which he simply ask everyone to read the piece ["Deal or No Deal"](https://code.facebook.com/posts/1686672014972296/deal-or-no-deal-training-ai-bots-to-negotiate/) as the official reference of the research. He also called the faked news "clickbaity and irresponsible". Prof. Yann Lecun also came out and [slam at the faked newsmaker](https://www.facebook.com/yann.lecun/posts/10154653925097143).

Both of them decline to comment on individual pieces, including The Source. We also tried to contact both Prof. Dhruv Batra and Dr. Mike Lewis on the validity of the Source. Unfortunately, they are both unavailable for comments.

4, *Our Take*

Since it's an unknown for us whether any of The Source is real, we can only speculate what happened here. What we can do is make as technically plausible as possible.

The key question here: is it possible that FB researchers have really created some codeword-like dialogue and passed it off to the source? It's certainly possible but *unlikely*. Popular outlets have general bad reputation of misinforming the public on A.I., it is hard to imagine that P.R. department of FB don't stop this kind of potential bad press in the first place.

Rather, it's more likely that FB researchers only publish paper, but somebody else is misusing the code the researchers open sourced (as we mentioned in Pt. 2). In fact, if you reexamine the dialogue released by The Source: 

> Bob: "i can i i everything else"
>
>
>
> Alice: "balls have zero to me to me to me to me ....."

It looks like the dialogue was generated by models which are not *well-trained*, this is true especially if you compare the print out with the one published by Facebook's github.

If our hypothesis is true, we side with FB researchers, and believe that someone just write a over-sensational post in the first place causing a stirs of the public. Generally, everyone who spreads the news should take responsibility to check the sources and ensure integrity of their piece. We certainly don't see such responsible behavior in the 30+ outlets who report the faked news. It also doesn't look likely that The Source is written in a way which is faithful of the original FB research. Kudos to Gizmodo and Snope's authors who did the right thing. [4]

Given the agent is more likely to behave like what we found on Facebook's github, we maintain our verdict as in Issue 18 and 23, it is still very unlikely that FB agents are creating any new language. But we add qualifier "very unlikely" because as you can see in Point 3, we still couldn't get Facebook researchers' verification as of this writing.

So let us reiterate our verdict: We rate the "Facebook killing agents" *false*. We rate "Agents that create its own language" *very likely false*.

AIDL Editorial Team

Footnote:

[1] So, immediately after the event, couple of members was [joking](https://www.facebook.com/groups/DeepNetGroup/permalink/480006772392210/) about the public was being ignorant about what so-called AI agents are.

[2] We avoiding naming what The Source is. There seems to be multiple of them and we are not sure which one is the true origin.

[3] The author of The Source seems to have communication with Facebook researcher [Prof. Dhruv Batra](https://www.cc.gatech.edu/~dbatra/index.html) and quote the Professor's word, e.g. 

> There was no reward to sticking to English language,

as well as talking with researcher Mike Lewis, 

> Agents will drift off understandable language and invent codewords for themselves,

[4] *What if we are wrong? Suppose the Source is real, and the Agents does Generated Codeword-Like Dialogue, Are they new Language?*

That's more a debatable issue. Again, just like we said in Issue 18, suppose you start from training a model like from an English database, the language you got will still be English. But can you characterize a English-like language as a new language? That's a harder question. e.g. a creole is usually seen as another language, but a pidgin is usually seen as just a grammatical simplification of a language. So how should we see the codeword generated by purported "rogue" agent? Only professional linguist should judge.

It is worthwhile to bring up one thing: while you can see the codeword language just like any machine protocol such as TCP/IP, the Source implies that Facebook researcher have consciously making sure the language adhere to English. Again, this involves if the Source is real, and whether the author has mixed in his/her own researches into the article.

[gizmodo.com](http://gizmodo.com/no-facebook-did-not-panic-and-shut-down-an-ai-program-1797414922)

## Blog Posts

### [Google at ICML 2017](https://research.googleblog.com/2017/08/google-at-icml-2017.html)

This is a set of papers written by Google researchers at ICML 2017.

[googleblog.com](https://research.googleblog.com/2017/08/google-at-icml-2017.html)

---

### [DeepMind's paper at ICML 2017](https://deepmind.com/blog/deepmind-papers-icml-2017-part-one/)

You can also find [Part Two](https://deepmind.com/bl%E2%80%A6/deepmind-papers-icml-2017-part-two/) and [Part Three](https://deepmind.com/blog/icml-round-papers-part-three/).

[deepmind.com](https://deepmind.com/blog/deepmind-papers-icml-2017-part-one/)

---

### [Fitting to Noise or Nothing At All: Machine Learning in Markets by Zachary David](http://zacharydavid.com/2017/08/fitting-to-noise-or-nothing-at-all-machine-learning-in-markets/)

While mostly criticizing one single paper, David's article should also alarm you how easy it is to do it wrong in DL+fintech world, and how easy to read a wrong paper.

[zacharydavid.com](http://zacharydavid.com/2017/08/fitting-to-noise-or-nothing-at-all-machine-learning-in-markets/)

---

### [DeepMind and Blizzard Release Starcraft II Research Environment ](https://deepmind.com/blog/deepmind-and-blizzard-open-starcraft-ii-ai-research-environment/)

In this very entertaining post from DeepMind, we learn about the new Starcraft II AI research environment. So that includes API, dataset and a sets of mini-games that agents can play.

Those are all good, but I guess the most interesting question we should ask when would computers can beat Starcraft at human level? That should make us all curious. In fact, DeepMind's post give us clues - currently, the problem seems to be very daunting - there are close to 300 basic actions at one moment you can use. According to DeepMind's estimation: even for a small screen size 84 x 84, we are talking about, there are around 1 million possible actions. That compare to Atari's 10 actions or in Go which has around few hundreds, we are talking about another breed of problems.

That's perhaps why DeepMind first encourage researcher to work on mini-games first - That makes a lot of sense - it's like before you play Go on a full board, you first learn how to play on a 9x9 board.

So far, DeepMind researchers are still perplexed by the problem - and all RL algorithms so far cannot beat the built in AI agents. And their next step is to imitation learning, which would be enabled by Blizaard's database on how the winners won on the game.

[deepmind.com](https://deepmind.com/blog/deepmind-and-blizzard-open-starcraft-ii-ai-research-environment/)

## Open Source

### [PyTorch 0.2 is out](https://github.com/pytorch/pytorch/releases/tag/v0.2.0?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=The%20Wild%20Week%20in%20AI)

The new toolkit in town, PyTorch, is releasing the second version of its toolkit. It does look cool, the two coolest feature in our view is higher order gradient calculation and distributed training. The former saves you time if you love to analyze NN by looking at Hessians. The latter is cool, of course, because it allows PyTorch to be used in more industrial scenarios which can speed up training if resources allowed.

[github.com](https://github.com/pytorch/pytorch/releases/tag/v0.2.0?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=The%20Wild%20Week%20in%20AI)

---

### [Distributome](http://distributome.org/)

Have you ever feel confused by probability distributions? We know we do. So that's why Distributome is such a cool project. Not only it comes up with the description of different distribution and their relationship. It also allow you to sample them. So in a sense, this is a cool mathematical and computational tool for researchers.

[distributome.org](http://distributome.org/)

## Paper/Thesis Review

### [Audio Super-Resolution with Neural Network](https://arxiv.org/pdf/1708.00853v1.pdf)

If you are into audio processing and super-resolution, this rare gem is for you. This paper brought the idea of image superresolution such as [C Dong's method](http://ieeexplore.ieee.org/document/7115171/) to audio.

[arxiv.org](https://arxiv.org/pdf/1708.00853v1.pdf)

---

### [Natural Language Processing with Small Feed-Forward Networks](https://arxiv.org/abs/1708.00214v1)

When the abstract says: 

> We show that small and shallow feed-forward neural networks can achieve near state-of-the-art results on a range of unstructured and structured language processing tasks while being considerably cheaper in memory and computational requirements than deep recurrent models.

This should make your pay attention, especially in our world where everyone is talking about using deep models. This article is a great rebuttal that in NLP you don't have to do that all the time. Shallower models can work as well.

[arxiv.org](https://arxiv.org/abs/1708.00214v1)
