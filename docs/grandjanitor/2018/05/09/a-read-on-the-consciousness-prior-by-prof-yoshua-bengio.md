---
title: "A Read on \"The Consciousness Prior\" By Prof. Yoshua Bengio"
date: 2018-05-09
---

# A Read on "The Consciousness Prior" By Prof. Yoshua Bengio

Here are some notes after reading Prof. Yoshua Bengio's "The Consciousness Prior". I know many of you, like [Stuart Gray](https://www.facebook.com/StuartGray?fref=gs&dti=849857175178950&hc_location=group) was quite unhappy that there is no experimental results. Yet, this is an interesting paper and good food for thought for all of us. Here are some notes:

\* The consciousness mentioned in the paper is much less of what would think as qualia but more about access of the different representations.

\* The terminology is not too difficult to understand, suppose there is a representation of the brain at a current time h_t, a representation RNN F is used to model such representation.

\* Whereas the protagonist here is the consciousness RNN, C, which is to used to model a consciousness state. What is \*consciousness state& then? It is actually a low-dimension vector of the representation h_t.

\* Now one thing to notice is that Bengio believe that consciousness RNN, C should by itself include some kind of attention mechanism. What that means is that attention being used in NNMT these days should be involved. In a nutshell, C should "pay attention" to only important details within this consciousness vector when it updates itself

\* I think so far the idea is already fairly interesting, in fact, just the idea one interesting thought : what if we just initialize the consciousness vector to be random instead, in that case, there will be a new representation of brain appears. As a result. this mechanism mimic human brains on exploring different scenario we conjured with imagination.

\* Bengio's thought also encompass a training method which he called verifier network, V. The goal of the network to match the current representation h_t with previous consciousness state c\_{t-k} (states?). The training as he envisioned can be a Variational autoencoder (VAE) or GAN.

\* So far the idea doesn't quite echo with human's way of thinking. Human seems to create high-level concepts, like symbols to simplify our thinking. So Bengio addresses these difficulty by suggesting we can just use another network to generate what we mean from the consciousness state, he called it U. Perhaps we can call it generation network. This network can well-be implemented by memory-augmented networks style of architecture which distinguish key/value pairs. In this case, we can map the consciousness to more concrete symbols which symbolic logic or knowledge representation framework can use. ... Or we humans can also understand this consciousness representation.

\* This all sounds good, but as you may hear from many readers of the paper. There is no experimental results. So this is really a theoretical paper.

\* To be fair though, the good professor has outlined how each of the above 4 networks can be actually implemented. He also mentioned how such idea can be experimented in practice. E.g. he believe one good arena is reinforcement learning tasks.

All-in-all, this is an interesting paper, it's a pity that the detail is scanty at this point. But it's still quite worthwhile for your time to read.
