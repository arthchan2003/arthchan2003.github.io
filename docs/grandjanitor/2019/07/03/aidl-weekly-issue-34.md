---
title: "AIDL Weekly Issue 34 -"
date: 2019-07-03
---

# AIDL Weekly Issue 34 -

# [Issue 34 *October 14th 2017* ](http://aidl.io/issues/34/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Perhaps the biggest new to us last week is California will allow car companies to test their fully autonomous vehicles on the street as soon as 2018.

Deal of the week last week is the Amazon/MS joint release of Gluon.

Then there are interviews. You would be interested to hear Google CEO Sinchar Pinchai's view on what being AI-first means.

---

As always, if you like our newsletter, feel free to subscribe/forward it to your colleagues.

Artificial Intelligence and Deep Learning Weekly

## News

### [Interview with Fei-Fei Li](https://www.technologyreview.com/s/609060/put-humans-at-the-center-of-ai/)

This is an interview with Fei-Fei Li, on her view about AI is not human-centric enough. And indeed, all we are building are A(S)I, S for special. Everyone is looking for the next paradigm change that takes us beyond the restrictive pattern recognition approach today.

[technologyreview.com](https://www.technologyreview.com/s/609060/put-humans-at-the-center-of-ai/)

---

### [Sundar Pinchai and The AI-First Google](https://www.theguardian.com/technology/2017/oct/07/google-boss-sundar-pichai-tax-gender-equality-data-protection-jemima-kiss)

This is the story of Google's CEO Sundar Pinchai, a calm presence in Google and the Valley, talking about his view on AI-First Google. His point - more isn't always better.

[theguardian.com](https://www.theguardian.com/technology/2017/oct/07/google-boss-sundar-pichai-tax-gender-equality-data-protection-jemima-kiss)

---

### [SDC in Carlifornia in 2018](https://www.theverge.com/2017/10/11/16458850/self-driving-car-california-dmv-regulations)

California is going to let 42 companies test up to 285 autonomous vehicles. And it will happen as soon as 2018.

[theverge.com](https://www.theverge.com/2017/10/11/16458850/self-driving-car-california-dmv-regulations)

---

### [Amazon and Microsoft release Gluon](https://www.geekwire.com/2017/amazon-microsoft-announce-gluon-neural-network-technology-teaming-machine-learning/)

We covered Gluon at [Issue 23](http://aidl.io/issues/23#start). Technically, we found it an interesting hybrid between imperative (like PyTorch) and declarative (like Tensorflow) style of programming. We learn from the [announcement](https://www.facebook.com/groups/DeepNetGroup/permalink/512611712465049/) that it is now available in AWS and MS.

For us the most interesting part is perhaps the partnership between MS and Amazon. It is the second time we heard they work with each other this year. In fact, back in September, we learn that they partner in [integrating ther voice assistants](https://www.theverge.com/2017/8/30/16224876/microsoft-amazon-cortana-alexa-partnership).

[geekwire.com](https://www.geekwire.com/2017/amazon-microsoft-announce-gluon-neural-network-technology-teaming-machine-learning/)

## Blog Posts

### [LSTM by numpy](http://blog.varunajayasiri.com/numpy_lstm.html)

This is a rare from-scratch implementation (with derivation) of LSTM using pure numpy.

[varunajayasiri.com](http://blog.varunajayasiri.com/numpy_lstm.html)

## Open Source

### [ONNX AI Format Gains Traction](https://research.fb.com/onnx-ai-format-adds-partners/)

The ONNX format introduced by FB and MS starts get more partners. This sounds good. For the most part, having an open format would allow results to spread more quickly across different sites/frameworks.

[fb.com](https://research.fb.com/onnx-ai-format-adds-partners/)

---

### [Tensorflow Lattice](https://techcrunch.com/2017/10/11/tensorflow-lattice-ensures-your-machine-learning-models-follow-global-trends/?ncid=mobilenavtrend)

When we first look at this piece, we thought that Lattice is yet another cool brandname. As it turns out Lattice is a release of an interesting mathematical model call deep lattice model (DLM).

So what is DLM then? It's all about lattice analysis - normal regression analysis usually doesn't impose order relationship between your inputs and outputs. So what if you hope that your output and input monotonically increase? That's the point of [lattice](https://papers.nips.cc/paper/3694-lattice-regression.pdf).

Of course, things are more complicated when the output is more monotonically increased with multiple inputs. Then using multi-layers of lattice layer would make sense. That was what the Google's original [paper](https://arxiv.org/abs/1709.06680) is about. Perhaps more importantly, they showed great results in several ML tasks.

[techcrunch.com](https://techcrunch.com/2017/10/11/tensorflow-lattice-ensures-your-machine-learning-models-follow-global-trends/?ncid=mobilenavtrend)

## Video

### [But what \*is\* a Neural Network? | Deep learning, Part 1 by 3Blue1Brown](https://www.youtube.com/watch?v=aircAruvnKk&feature=youtu.be)

Here is a very good introduction of what neural network is by the beloved Math teacher, 3Blue1Brown.

[youtube.com](https://www.youtube.com/watch?v=aircAruvnKk&feature=youtu.be)

## Paper/Thesis Review

### [Tutorial on Variational Autoencoders](https://arxiv.org/pdf/1606.05908.pdf)

We were trying to read [DP Kingma's thesis](https://www.dropbox.com/s/v6ua3d9yt44vgb3/cover_and_thesis.pdf?dl=0) on VAE. As you might know, he wrote the paper on reparametization trick on VAE. But this is not my topic this time. We just want to talk about a simple tutorial paper by Carl Doersch, which we found it to be better for beginners. Here are some notes: 
- VAE is really quite different sparse AE or denoising AE except you can think of both of them like having an encoder structure.
- The Tutorial would guide you through the setup of VAE. e.g. You probably know that VAE is based on latent variable. But then the setup is special which the latent variable is randomly sampled from a Gaussian.
- Then there is a detail readable section on how the common optimization evidence lower bound (ELBO) is formulated. What it bugs me a bit is that it doesn't quite use the term ELBO.
- Lastly it's the reparametization trick. we don't fully grok it but that's why we still need to read Kingma

So far, this seems to be a great tutorial on VAE and it's a great first read on the topic.

[arxiv.org](https://arxiv.org/pdf/1606.05908.pdf)
