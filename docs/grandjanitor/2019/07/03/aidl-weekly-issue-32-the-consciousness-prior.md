---
title: "AIDL WEEKLY ISSUE 32 - The Consciousness Prior"
date: 2019-07-03
---

# AIDL WEEKLY ISSUE 32 - The Consciousness Prior

# [Issue 32 *September 30th 2017* ](http://aidl.io/issues/32/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Many interesting news last week including, 
- MS released new tools on Azure and Visual Studio to support deep learning,
- Intel released Lolhi, a new neuromorphic chip,
- Nvidia released its own deep learning accelerator chip design,
- And we also read a Wire profile on the controversial figure - Anthony Lewandoski.

All of these pieces would normally be the highlights of the week. But then, Prof. Bengio come up with an intriguing note called "The Consciousness Prior". Upon closer read, it gives an interesting take on a potential mechanism to mimic human consciousness, or a kind of access of attention as neuroscientists like Stanislas Dahaene would call. So his paper is this week's theme.

---

As always, if you like our newsletter, feel free to subscribe and forward our letter to your colleagues!

Artificial Intelligence and Deep Learning Weekly

---

### [If you live in Boston area....](https://www.meetup.com/Boston-AIDL-Meetup/members/?sort=join_date&desc=true)

As Waikit and Arthur are preparing our own "Attack of the A.I. Startups" in December, we also start a new AIDL meetup group in the Boston area. Feel free to join us if you live in the New England or New York area!

[meetup.com](https://www.meetup.com/Boston-AIDL-Meetup/members/?sort=join_date&desc=true)

---

### [Interview of Waikit and Arthur](https://soundcloud.com/botsupply/episode-2-arthur-waikit-aidl)

Botsupply's Grasia B. Hald and Shridhar Kumar were kind enough to invite us to their podcast. We had a fun time talking about how we started our AIDL community, our experience in commercial and technical side of machine learning. So check it out!

[soundcloud.com](https://soundcloud.com/botsupply/episode-2-arthur-waikit-aidl)

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Yoshua Bengio Calls for Breaking Up Big Tech AI Research](https://www.axios.com/artificial-intelligence-pioneer-calls-for-the-breakup-of-big-tech-2487483705.html)

At an AI conference in Montreal, Prof. Yoshua Bengio said: 

> "Concentration of wealth leads to concentration of power. That's one reason why monopoly is dangerous. It's dangerous for democracy."

One consequence of deep learning becoming more mainstream is that the barriers of learning and practicing it are continually being lowered. In the past, working on state-of-the-art machine learning requires clusters of high-end machines. But now, it is possible to use a PC with a good GPU card, and do some experiments on your own.

At the same time, however, such democratization doesn't extend upstream to the cutting-edge research side. Deep learning research has increasingly been concentrated in hands of a few large companies. Such drain of talents from academia is becoming a problem, and perhaps why Bengio is sounding the alarm.

[axios.com](https://www.axios.com/artificial-intelligence-pioneer-calls-for-the-breakup-of-big-tech-2487483705.html)

---

### [A Profile on Anthony Levandowski](https://www.wired.com/story/god-is-a-bot-and-anthony-levandowski-is-his-messenger)

If you are interested in SDC, you would notice that the Waymo-Uber lawsuit is still going on. In fact, unlike the [seemingly more gentle stance](https://techcrunch.com/2017/07/07/waymo-drops-patent-claims/) earlier in Summer, Waymo in reinitiating [charges against Uber](https://www.nytimes.com/2017/09/20/business/waymo-uber-lawsuit.html?mcubz=0) after discovering new Uber technical documents.

The whole drama centers on one person, Mr. Anthony Levandowski. This Wired piece is a good profile on him.

While peripheral, it's an interesting study into a key person (up till recently at least) whose interesting worldview include robots taking over the world. As quote in the Wired article: 

> “We’re going to take over the world. One robot at a time,” wrote Levandowski another time [to Kalanick]"

[wired.com](https://www.wired.com/story/god-is-a-bot-and-anthony-levandowski-is-his-messenger)

---

### [The New Intel Neuromorphic Chip](https://newsroom.intel.com/editorials/intels-new-self-learning-chip-promises-accelerate-artificial-intelligence/)

Intel just released a chip but it is not a standard deep learning chip as Google's Tensor processing unit (TPU) or Nvidia's recently released NVLDA.

Intel's line of work seems to base on spiking neural network (SNN) which was always described as closer to human brain than the usual deep neural network. What's the difference? For starters, deep neural network doesn't quite consider spike train as human brain neurons do. And timing of the spikes usually convey a lot of information within our biological neural networks.

Neuromorphic design also uses less energy. In the case of Lolhi, the new chip, it could use down to 2000 times less energy consumption.

Perhaps one thing we are not sure is how *fast* the new chip could be. Currently we only heard about test case in MNIST.

[intel.com](https://newsroom.intel.com/editorials/intels-new-self-learning-chip-promises-accelerate-artificial-intelligence/)

## Blog Posts

### [Sebastian Ruder on Multi-Task Learning](http://ruder.io/multi-task-learning-nlp/)

Ruder is doing it again, this time he wrote a very accessible text on multi-task learning. He talked about strategies of choosing auxilliary cost functions as well as how different tasks can be shared.

[ruder.io](http://ruder.io/multi-task-learning-nlp/)

---

### [Review of EMNLP 2017 by Leon Derczynski](http://approximatelycorrect.com/2017/09/26/a-random-walk-through-emnlp-2017/)

A great review of EMNLP 2017. The ones I like is Derczynski's reviews on the workshops on both noisy text data as well as embedding evaluation.

[approximatelycorrect.com](http://approximatelycorrect.com/2017/09/26/a-random-walk-through-emnlp-2017/)

## Open Source

### [Microsoft Releases New Tools for Machine Learning](https://techcrunch.com/2017/09/25/microsoft-launches-new-machine-learning-tools/)

MS has always been a major player of machine learning. But then its recent move to release several tools such as Microsoft Azure Experimental Service, as well as allow MS Visual Studio to work with toolkits such Caffe and MS's own CNTK. That's a very important step forward - remember that installing/compiling any of the DL toolkits are very painful process.

[techcrunch.com](https://techcrunch.com/2017/09/25/microsoft-launches-new-machine-learning-tools/)

---

### [Theano at 1.0 and its final version.](https://groups.google.com/forum/#!topic/theano-users/7Poq8BZutbY)

Just yesterday, Yoshua Bengio announced that the grandfather of all deep learning toolkit, Theano, will be at 1.0, but it's also the last version MILA would release. I think we should take a moment to remember how much Theano has help jumpstarted deep learning.

(In fact, Arthur's first deep learning experiments are all ran in Theano on an old Dell Inspiron 530 - not using GPU Card btw.)

[google.com](https://groups.google.com/forum/#!topic/theano-users/7Poq8BZutbY)

---

### [Nvidia open source Deep Learning Accelerator Chip Design](http://nvdla.org/)

This is a rather big move from Nvidia, as it is seldom the case that chip company would open source their chip design to the public. Beside the fact that this could be a publicity stun, it's possible that they were too behind of Google's effort of Tensor processing unit (TPU) development, which as you know Google just release its [v2](https://www.hpcwire.com/2017/05/25/google-debuts-tpu-v2-will-add-google-cloud/)(!) in this April. It's reasonable to believe that Google may be 5 years ahead of the game.

Nvidia open sourcing their own accelerator make the community to work on the chip design together. In a way, it can attract contribution to the source code such that there is a chance to catch up.

Of course, the downside is that hardware development usually requires more investment. So unlike the software-counterpart, it's harder for anyone who could come up with a good design to rival TPU v2 soon.

Regardless, we think it is a good development for the DL community. Let's see what the community come up in the next few years.

[nvdla.org](http://nvdla.org/)

## Paper/Thesis Review

### [Reading Prof. Yoshua Bengio's "The Consciousness Prior"](https://arxiv.org/abs/1709.08568)

Prof. Yoshua Bengio released an intriguing note last week on an idea called "The Consciousness Prior". The framework is interesting and I would point out several interesting aspects of it. 
- The consciousness mentioned in the paper is much less of what would think as [qualia](https://en.wikipedia.org/wiki/Qualia) but more about access of the different representations.
- The terminology is not too difficult to understand, suppose there is a representation of the brain at a current time h_t, *a representation RNN* F is used to model such representation.
- Whereas the protagonist here is the *consciousness RNN*, C, which is to used to model a consciousness state. What is \*consciousness state& then? It is actually a low-dimension vector of the representation h_t.
- Now one thing to notice is that Bengio believe that *consciousness RNN, C* should by itself include some kind of attention mechanism. What that means is that attention being used in NNMT these days should be involved. In a nutshell, C should "pay attention" to only important details within this consciousness vector when it updates itself.
- I think so far the idea is already fairly interesting, in fact, just the idea one interesting thought : what if we just initialize the consciousness vector to be random instead, in that case, there will be a new representation of brain appears. As a result. this mechanism mimic human brains on exploring different scenario we conjured with imagination.
- Bengio's thought also encompass a training method which he called verifier network, V. The goal of the network to match the current representation h_t with previous consciousness state c\_{t-k} (states?). The training as he envisioned can be a Variational autoencoder (VAE) or GAN.
- So far the idea doesn't quite echo with human's way of thinking. Human seems to create high-level concepts, like symbols to simplify our thinking. So Bengio addresses these difficulty by suggesting we can just use another network to generate what we mean from the consciousness state, he called it U. Perhaps we can call it *generation network*. This network can well-be implemented by memory-augmented networks style of architecture which distinguish key/value pairs. In this case, we can map the consciousness to more concrete symbols which symbolic logic or knowledge representation framework can use. ... Or we humans can also understand this consciousness representation.
- This all sounds good, but as you may hear from many readers of the paper. There is no experimental results. So this is really a theoretical paper.
- To be fair though, the good professor has outlined how each of the above 4 networks can be actually implemented. He also mentioned how such idea can be experimented in practice. E.g. he believe one good arena is reinforcement learning tasks.

All-in-all, this is an interesting paper, it's a pity that the detail is scanty at this point. But it's still quite worthwhile for your time to read.

[arxiv.org](https://arxiv.org/abs/1709.08568)
