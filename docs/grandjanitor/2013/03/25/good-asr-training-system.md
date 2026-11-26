---
title: "Good ASR Training System"
date: 2013-03-25
categories: ["sphinxtrain", "Thought", "training", "training scripts"]
---

# Good ASR Training System

The term "speech recognition" is a misnomer. 

Why do I say that? I have explained this point in an old article "[Do We Have True Open Source Dictation?](http://arthur-chan.blogspot.com/2009/04/do-we-have-true-open-source-dictation.html), which I wrote back in 2005: To recap, a speech recognition system consists of a Viterbi decoder, an acoustic model and a language model. You could have a great recognizer but bad accuracy performance if the models are bad. 

So how does that related to you, a developer/researcher of ASR? The answer is ASR training tools and process usually become a core asset of your inventories. In fact, I can tell you when I need to work on acoustic model training, I need to spend full time to work on it and it's one of the absorbing things I have done. 

Why is that? When you look at development cycles of all tasks in making an ASR systems. Training is the longest. With the wrong tool, it is also the most error prone. As an example, just take a look of Sphinx forum, you will find that majority of non-Sphinx4 questions are related to training. Like, "I can't find the path of a certain file", "the whole thing just stuck at the middle". 

Many first time users complain with frustration (and occasionally disgust) on why it is so difficult to train a model. The frustration probably stems from the perception that "Shouldn't it be well-defined?" The answer is again no. In fact how a model should be built (or even which model should be built) is always subjects to change. It's also one of the two subfields in ASR, at least IMO, which is still creative and exciting in research. (Another one: noisy speech recognition.) What an open source software suite like Sphinx provide is a standard recipe for everyone. 

Saying so, is there something we can do better for an ASR training system? There is a lot I would say, here are some suggestions:  

1. A training experiment should be created, moved and copied with ease,
2. A training experiment should be exactly repeatable given the input is exactly the same,
3. The experimenter should be able to verify the correctness of an experiment before an experiment starts.

Ease of Creation of an Experiment

You can think of a training experiment as a recipe ...... not exactly. When we read a recipe and implement it again, we human would make mistakes. 

But hey! We are working with computers. Why do we need to fix small things in the recipe at all? So in a computer experiment, what we are shooting for is an experiment which can be easily created and moved around. 

What does that mean? It basically means there should be no executables which are hardwired to one particular environment. There should also be no hardware/architecture assumption in the training implementations. If there is, they should be hidden. 

Repeatability of an Experiment

Similar to the previous point, should we allow difference when running a training experiment? The answer should be no. So one trick you heard from experienced experimenters is that you should keep the seed of random generators. This will avoid minute difference happens in different runs of experiments. 

Here someone would ask. Shouldn't us allow a small difference between experiments? We are essentially running a physical experiment. 

I think that's a valid approach. But to be conscientious, you might want to run a certain experiment many times to calculate an average. In a way, I think this is my problem with this thinking. It is *slower* to repeat an experiment. e.g. What if you see your experiment has 1% absolute drop? Do you let it go? Or do you just chalk it up as noise? Once you allow yourself to not repeat an experiment *exactly,* there will be tons of questions you should ask.

Verifiability of an Experiment

Running an experiment sometimes takes day, how do you make sure running it is correct? I would say you should first make sure trivial issues such as missing paths, missing models, or incorrect settings was first screened out and corrected.

One of my bosses used to make a strong point and asked me to verify input paths every single time. This is a good habit and it pays dividend. Can we do similar things in our training systems?

## Apply it on Open Source

What I mentioned above is highly influenced by my experience in the field. I personally found that sites, which have great infrastructure to transfer experiments between developers, are the strongest and faster growing. 

To put all these ideas into open source would mean very different development paradigm. For example, do we want to have a centralized experiment database which everyone shares? Do we want to put common resource such as existing paramatized inputs (such as MFCC) somewhere in common for everyone? Should we integrate the retrieval of these inputs into part of our experiment recipe? 

Those are important questions. In a way, I think it is the most type of questions we should ask in open source. Because regardless of much volunteer's effort. Performance of open source models is still lagging behind the commercial models. I believe it is an issue of methodology. 

Arthur

---

## Comments

**三十三博** (2013-03-26):

Hey Pranav,

Thanks for your comments. I have noticed your earlier comments wasn't shown so I decided to revert to an earlier templates. Sorry for the missing comments.

Arthur

**Pranav Jawale** (2013-03-26):

\+1 for 'verify the correctness of an experiment before an experiment starts'.

Another imp thing is to pay attention to the warnings (wrt SphinxTrain). At times there could be warnings like "senone never found" in context independent stage. Although training doesn't halt, it is better to modify the phoneset (by merging two or more phones into one) if one finds such warnings.

