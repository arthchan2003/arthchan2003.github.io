---
title: "Two Views of Time-Signal : Global vs Local"
date: 2013-01-08
categories: ["Berkeley license", "cmn", "cmu sphinx", "global", "GNU license.", "HCopy", "HTK", "HVite", "local", "sphinxbase", "sphinx_fe", "Thought", "wave2feat"]
---

# Two Views of Time-Signal : Global vs Local

As I have been working on Sphinx at work and start to chat with Nicholay more, one thing I realize is that several frequently used components of Sphinx need to rethink. Here is one example related to my work recently.

Speech signal or ...... in general time signal can be processed in two ways: you either process as a whole, or you process in blocks. The former, you can call it a global view, the latter, you can call it a local view. Of course, there are many other names: block/utterance, block/whole but essentially the terminology means the same thing.

For most of the time, global and local processing are the same. So you can simply say: the two types of the processing are equivalent. 

Of course, not when you start to an operation which use information available. For a very simple example, look at cepstral mean normalization (CMN). Implementing CMN in block mode is certainly an interesting problem. For example, how do you estimate the *mean* if you have a running window? When you think about it a little bit, you will realize it is not a trivial problem. That's probably why there are still papers on cepstral mean normalization.

Translate to sphinx, if you look at sphinxbase's sphinx_fe, you will realize that the implementation is based on the local mode, i.e. every once in a while, samples are consumed, processed and write onto the disc. There is no easy way to implement CMN on sphinx_fe because it is assumed that the consumer (such as decode, bw) will do these stuffs their own.

It's all good though there are interesting consequence: what the SF's guys said about "feature" is really all the processing that can be done in the local sense. Rather than the "feature" you see in either the decoders or bw. 

This special point of view is ingrained within sphinxbase/sphinxX/sphinxtrain (Sphinx4? not sure yet.) . This is quite different from what you will find in HTK which see feature vector as the vector used in Viterbi decoding.

That bring me to another point. If you look deeper, HTK such as HVite/HCopy are highly abstract. So each tool was designed to take care of its own problem well. HCopy really means to provide just the feature, whereas HVite is just doing Viterbi algorithm on a bunch of features. It's nothing complicated. On the other hand, Sphinx are more speech-oriented. In that world, life is more intertwined. That's perhaps why you seldom hear people use Sphinx to do research other than speech recognition. You can, on the other hand, do other machine learning tasks in HTK.

Which view is better? If you ask me, I hope that both HTK and Sphinx are released in Berkeley license. Tons of real-life work can be saved because each cover some useful functionalities. 

Given that only one of them are released in a liberal license (Sphinx), then may be what we need is to absorb some design paradigm from HTK. For example, HTK has a sense of organizing data as pipes. That something SphinxTrain can use. This will enhance work of Unix users, who are usually contribute the most in the community. 

I also hope that eventually there are good clones of HTK tools but made available in Berkeley/GNU license. Not that I don't like the status quo: I am happy to read the code of HTK (unlike the time before 2.2......). But as you work in the industry for a while, many are actually using both Sphinx and HTK to solve their speech research-related problems. Of course, many of these guys (, if they are honest,) need to come up with extra development time to port some HTK functions into their own production systems. Not tough, but you will wonder whether time can be better spent ......

Arthur

---

## Comments

**Arthur Chan** (2013-11-17):

Hint: Write one yourself.

The algorithm is in the literature and if you look at the tools, it is quite unlikely you want to replicate what HTK or sphinx already do.

Arthur

