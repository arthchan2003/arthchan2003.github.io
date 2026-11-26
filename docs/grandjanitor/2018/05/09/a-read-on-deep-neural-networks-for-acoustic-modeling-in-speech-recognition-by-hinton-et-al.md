---
title: "A Read on \"Deep Neural Networks for Acoustic Modeling in Speech Recognition\" by Hinton et al."
date: 2018-05-09
categories: ["Summary"]
tags: ["deep learning"]
---

# A Read on "Deep Neural Networks for Acoustic Modeling in Speech Recognition" by Hinton et al.

A read on "Deep Neural Networks for Acoustic Modeling in Speech Recognition" by Hinton et al.

\* This is the now-classic paper in deep learning, which is for the first time people confirmed that deep learning can improve ASR significantly. It is important in the fields of both deep learning and ASR. It's also one of the first papers I read on deep learning back in 2012-3.

\* Many people know the origin of deep learning from image recognition, e.g. many kids would tell you stories about Imagenet, Alexnet and history from now on. But then the first important application of deep learning is perhaps speech recognition.

\* So what's going on with ASR before deep learning then? For the most part, if you can come up with a technique that cut a state-of-the-art system's WER by 10%, your PhD thesis is good. If your technique can consistently beat previous techniques in multiple systems, you usually get a fairly good job in a research institute in Big 4.

\* The only technique which I recall to be better than 10% relative improvement are discriminative training. It got ~15% in many domains. That happens back in 2003-2004. In ASR, the term "discriminative training" has very complicated connotation. So I am not going to explain much. This just gives you the context of how powerful deep learning is.

\* You might be curious what "relative improvement" is. e.g. suppose your original WER is 18%, but you improve from 17%, then your relatively improvement is 1%/18% = 5.56%. So 10% improvement really means you go down to 16.2%. (Yes, ASR is that tough.)

\* So here comes replacing GMM with DNN. In these days, it sounds like a no-brainer. But back then, it was a huge deal. Many people in the past tried to stuff various ML technique to replace GMM. But no one can successfully beat HMM. So this is innovative.

\* Now then it is how GMM is setup - the ancestor of this work has to trace back to Bourlard and Morgan's "Connectionist Speech Recognition" in which the authors tried to come up with a Context-independent HMM system by replacing VQ scores with a shallow neural network. At that time, the unit are chosen to be CI-states.

\* Hinton's and perhaps Deng's thinking are interesting: The unit was chose to be context-dependent states. Now that's an new change, and reflect how modern HMM system is trained.

\* Then there is how the network is really trained. Now you can see the early DLer's stress on using pre-training because training is very expensive at that point. (I suspect it wasn't using GPUs).

\* Then there is the use of entropy to train a model. Later on, in other systems, many people just use a sentence-based entropy to do training. So in this sentence, the paper is olden.

\* None of these are trivial work. But the result is stellar: we are talking about 18%-33% relative gain (p.14). To ASR people, that's unreal.

\* The paper also foresee some future use of DNN, such as bottleneck feature and articulatory feature. You probably know the former already. The latter is more exoteric in ASR, so I am not going to talk about much.

Anyway, that's what I have. Enjoy the reading!
