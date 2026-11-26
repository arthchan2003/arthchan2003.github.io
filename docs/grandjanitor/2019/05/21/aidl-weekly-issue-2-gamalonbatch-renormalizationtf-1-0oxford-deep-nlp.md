---
title: "AIDL Weekly Issue 2 - Gamalon/Batch Renormalization/TF 1.0/Oxford Deep NLP"
date: 2019-05-21
---

# AIDL Weekly Issue 2 - Gamalon/Batch Renormalization/TF 1.0/Oxford Deep NLP

# Issue 2 *February 24th 2017*

## Editorial

### Thoughts From Your Humble Curators

How to create a good A.I. newsletter? What first comes to everybody's mind is to simply aggregate a lot of links. This is very common in deep learning resource lists, say "Cool List of XX in Deep Learning". Our experience is that you usually have to sift through 100-200 links and decide which are useful.

We believe there is a better way: In AIDL Weekly, we only choose important news and always provide detailed analysis on each of them. For example, here we take a look at newsworthy [Gamalon](https://gamalon.com/), it is known to use a ground-breaking method to outperform deep learning and win a defense contract recently. What is the basis of its technology? We cover this in a deep dive in the "News" section.

Or you can take a look of the exciting development of batch renormalization that tackles its current shortcomings. Anyone who does normalization in training will likely benefit from the paper.

Last week, we also saw the official release of Tensorflow 1.0 as well as the 2017 Official Tensorflow Summit. We prepared two good links so that you can follow. If you love deep learning with NLP, you might also want to check out the new course from Oxford.

As always, check out [our FB group](https://www.facebook.com/groups/DeepNetGroup/), our [YouTube channel](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg), of course [subscribe this newsletter](https://aidlweekly.curated.co/).

Artificial Intelligence and Deep Learning Weekly

## News

### [Gamalon](https://www.technologyreview.com/s/603542/ai-software-juggles-probabilities-to-learn-from-less-data/)

[Gamalon](https://gamalon.com/) stunned all of us last week by claiming the use of "Bayesian program synthesis" (BPS) is superior than Deep Learning. That's a bold claim, but how real is it? The Wired piece only gives us a glimpse. So let's take a closer look.

While Gamalon's demo on recognizing drawing is impressive, we think the more telling example is Gamalon's [abbreviation modeling](https://gamalon.com/technology/). It clearly shows that BPS has better performance than LSTM-based seq2seq, especially when there is not enough training sample. Because despite the prowess of deep learning, it requires substantial amount of training data, and often, large amount of data is just unavailable. In a way, this is where Bayesian methods shine - data is just used an evidence to update a prior distribution. (For an intro, take a look of PRML Chapter 1.)

Since Bayesian method was around for a while, what's the big deal with Gamalon then? We think it has a lot to do with [probabilistic programming](https://en.wikipedia.org/wiki/Probabilistic_programming_language) which has been a buzzword lately. Probabilistic programming (PPL) ([simple tutorial from Cornell](https://www.cs.cornell.edu/courses/cs4110/2016fa/lectures/lecture33.html)) promises to make statistical modeling much easier with pre-defined programming structures, and reduce the very complex programming task to much fewer lines (e.g. [this link](https://phys.org/news/2015-04-probabilistic-lines-code-thousands.html)).

PPL was conventionally related to Bayesian network and graphical models. We speculate that Gamalon is using PPL to code up some type of Bayesian method. [Ben Vigoda](https://www.linkedin.com/in/ben-vigoda-b4b0a61), Founder & CEO of Gamalon, worked on probabilistic programming in his thesis.

We hope that there will be more details published by either Vigoda or researchers from Gamalon. All-in-all, Gamalon is using an easier-for-developer paradigm (PPL) and a less data-hungry method (Bayesian method). If this approach works well generically across most/all use cases, then it could really push the envelope where training data is sparse which is almost always true in niche-er or less AI-mature fields where A.I. is just being applied.

We believe this is a big pain point and part of an important and larger innovation theme in deep learning in the foreseeable future - how to solve the data sparseness problem. There are a few approaches - from the framework/algo side (Gamelon's) to training data acquisition and labelling as a service ([Mighty AI](https://mty.ai/)) to just plain mechanical turk-ing. Unlike other disruptions that tend to favor upstarts, machine learning requires so much training data that today, the advantage is with the behemoths, given their troves of training data with full usage rights (Google, MSFT, etc.). We'll maybe dive a little deeper into these competitive dynamics in a different issue...

[technologyreview.com](https://www.technologyreview.com/s/603542/ai-software-juggles-probabilities-to-learn-from-less-data/)

---

### [Batch Renormalization: Classic Batch Normalization Paper Got an Update](https://arxiv.org/pdf/1702.03275v1.pdf)

A more DL-geeky news: Wow! Batch normalization is getting an update!

As you might recall, [BatchNorm](https://arxiv.org/abs/1502.03167) is a powerful method which normalize activations of a neural network. Such normalization stabilize the network and significantly improve training speed and performance. Of course, the cute part is the normalization can be used with backprop so it becomes a staple in convnet training.

In Batch ReNormalization (batchrenorm), Sergey Ioffe tries to resolve the problem of batchnorm which is sensitive to small size batch. So why small size batch would be an issue then? A small mini-batch would cause a mis-estimation of the batch means and variance, which are crucial in the batchnorm's calculation.

Can you simply use a running average of mean to reduce the misestimation? Turns out you cannot, loffe in the previous [BatchNorm paper](https://arxiv.org/abs/1502.03167), already observed that a trivial use of running average counteract normalization. It would lead to no update to the parameters. So you will have to use the means/variances from batchnorm.

Ok, enough of a teaser - Ioffe does come up with a good idea in batchrenorm which trade off the running average of mean and the batch means. And again, it can run as part of backprop. That's a very exciting development.

So I highly recommend you to read this new paper. Btw, the method is also useful to deal with non-i.i.d. mini-batch which is useful in [metric learning](http://cseweb.ucsd.edu/~naverma/talks/metric_learning_tutorial_verma.pdf). So check it out.

[arxiv.org](https://arxiv.org/pdf/1702.03275v1.pdf)

## Blog Posts

### [Julia Evans explains CNN](https://jvns.ca/blog/2017/02/12/neural-style/)

[Julia Evans](https://twitter.com/b0rk) has been one of my favorite bloggers last couple of years. In her blog, she explore wide range of topics including system programming and machine learning. In this [post](https://jvns.ca/blog/2017/02/12/neural-style/), she explains the basic principle of [neural-style transfer](https://arxiv.org/abs/1508.06576) (not to be confused with ["transfer learning"](http://cs231n.github.io/transfer-learning/). She picked up [the original paper by Leon Gatsys](https://arxiv.org/abs/1508.06576).

I appreciate her writing - the part I like most is that she emphasize that she does not quite understand why "style" in Gatys' paper was so-defined. If you read Gatys' paper, the most innovative part of the work is the definition of Gram's matrix, which is roughly an inner product of feature maps. Why does that constitute a "style"? For example, why wouldn't one element of the Gram's matrix be more important than the others to define an image? No one seems to have a clear answer. She is not alone, not even Karparthay was able to explain the concept in cs231n 2016.

Perhaps that's why neural-style transfer is still a research topic, it gives us all these weird pictures, yet no one understand why.

[jvns.ca](https://jvns.ca/blog/2017/02/12/neural-style/)

---

### [AWS AI Blog](https://aws.amazon.com/blogs/ai/welcome-to-the-new-aws-ai-blog/)

New A.I. blog from Amazon, another power house of A.I. and deep learning. Recently Amazon starts a [deep learning AWS instance](https://aws.amazon.com/marketplace/pp/B06VSPXKDX). Of course Amazon is also great supporter of [MXNet](https://aws.amazon.com/mxnet/). Would this new A.I. blog become like [Google Research Blog](https://research.googleblog.com/)? Which gives us the latest research papers of Amazon?

[amazon.com](https://aws.amazon.com/blogs/ai/welcome-to-the-new-aws-ai-blog/)

## Open Source

### [Official Release of Tensorflow 1.0](https://developers.googleblog.com/2017/02/announcing-tensorflow-10.html)

More and more, [Tensorflow](https://www.tensorflow.org/) becomes more a gcc for deep learning. It is the most popular deep learning toolkit, perhaps only [Pytorch](http://pytorch.org/) is close to its popularity.

What should we expect from an official release of 1.0 then? To developers, hopefully it means a consolidation of API. As many TF developers would tell you, TF breaks backward compatibility from time to time, and it could be painful to forward-port your existing code. We can also expect 1.0's python API will keep ["API stability promises"](https://www.tensorflow.org/programmers_guide/version_semantics)

I do find TF's development is healthy and they have systematically integrate quality packages. One example is to integrate [Keras](https://keras.io/) as [one of the official meta-layers](https://github.com/fchollet/keras/issues/5050). I can't wait to see what new exciting development from TF this year.

[googleblog.com](https://developers.googleblog.com/2017/02/announcing-tensorflow-10.html)

---

### [PyTorch Example](https://github.com/jcjohnson/pytorch-examples)

[Justin Johnson](http://cs.stanford.edu/people/jcjohns/) delivers again. If you follow the software space of Torch, Johnson had upgraded [Andrej Karparthy's code on char-rnn](https://github.com/karpathy/char-rnn) to [torch-rnn](https://github.com/jcjohnson/torch-rnn). He also came up with a [fast implementation of neural-style transfer](https://github.com/jcjohnson/neural-style). Of course, we welcome his new package on how to use [pytorch](http://pytorch.org/) as well.

[github.com](https://github.com/jcjohnson/pytorch-examples)

## Video

### [TensorFlow Developer Summit 2017](https://www.youtube.com/watch?v=LqLyrl-agOw)

Other than releasing 1.0, Tensorflow also holds its developer summit at Feb 15, here is the full video shared at YouTube with many power developers on the latest of TF.

Contents (Timemarks originally from [YouTube user BigBadWolf](https://www.youtube.com/user/sect00rify)) 
- [11:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=660s) Intro
- [12:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=720s) Jeff Dean on general info
- [20:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=1200s) Rajat Monga on TensorFlow 1.0, XLA
- [28:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=1680s) Megan Kacholia TensorFlow in Depth
- [34:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=2040s) Jeff Dean What people have been doing
- [38:20](https://www.youtube.com/watch?v=LqLyrl-agOw&t=2300s) commercial video
- [42:20](https://www.youtube.com/watch?v=LqLyrl-agOw&t=2540s) Intro to the next part
- [43:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=2580s) Chris on XLA and other tensorflow compilers
- [1:31:30](https://www.youtube.com/watch?v=LqLyrl-agOw&t=5490s) Dendelion on Tensorboard (good part)
- [1:55:30](https://www.youtube.com/watch?v=LqLyrl-agOw&t=6930s) Martin on TensorFlow High-Level API
- [2:13:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=7980s) Francois on Keras integration
- [3:01:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=10860s) Daniel from Deepmind Applied Why they choose TensorFlow and how they use it
- [3:31:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=12660s) Using Tensorflow on mobile and embedded devices (lunch)
- [5:11:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=18660s) Derek on Distributed TensorFlow
- [5:41:10](https://www.youtube.com/watch?v=LqLyrl-agOw&t=20470s) Jonathan on the TensorFlow EcoSystem
- [5:59:30](https://www.youtube.com/watch?v=LqLyrl-agOw&t=21570s) Noah on TensorFlow Serving
- [6:18:50](https://www.youtube.com/watch?v=LqLyrl-agOw&t=22730s)Ashish on ML Toolkit (scikit inspired)
- [6:58:20](https://www.youtube.com/watch?v=LqLyrl-agOw&t=25100s) Eugene on the RNN API in TensorFlow and dynamic calculations
- [7:30:50](https://www.youtube.com/watch?v=LqLyrl-agOw&t=27050s) Wide and Deep Learning
- [7:48:40](https://www.youtube.com/watch?v=LqLyrl-agOw&t=28120s) Magenta
- [8:01:00](https://www.youtube.com/watch?v=LqLyrl-agOw&t=28860s) TensorFlow in Medicine

[youtube.com](https://www.youtube.com/watch?v=LqLyrl-agOw)

---

### [Deep Learning for Natural Language Processing: 2016-2017](https://www.cs.ox.ac.uk/teaching/courses/2016-2017/dl/)

For a long time, the only choice intro-class for "deep learning with NLP" would be Socher's [Stanford cs224d](http://cs224d.stanford.edu/). Now there is another choice. [Phil Blunsom](https://www.cs.ox.ac.uk/people/phil.blunsom/) starts a new Oxford class on [Deep NLP](https://github.com/oxford-cs-deepnlp-2017/lectures) and all lectures are available on-line.

The material looks promising. For example, the material about conditional language model (by [Chris Dyer](http://www.cs.cmu.edu/~cdyer/)) is new for an intro class.

[ox.ac.uk](https://www.cs.ox.ac.uk/teaching/courses/2016-2017/dl/)

## Member's Question

### Question from a AIDL Member

** Q: (Rephrase) I am trying to learn the following languages, (...) to intermediate level, and the following languages, (...) to professional level. Would this be helpful for my career on Data Science/Machine Learning? I have a mind to work on deep learning."** 

This is a variation of a frequently asked question. In a nutshell, "how much programming should I learn if I want to work on deep learning?". The question itself shows misconceptions about programming and machine learning. So we include it in this issue. This is my (Arthur's) take: 
1. First thing first, usually you first decide which package to work on, if the package use language X, then you go to learn-up language X. e.g. if I want to hack Linux kernel, I would need to know C and learn Linux system calls, and perhaps some assembly language. Learning programming is more like a means to achieve a goal. Echoing J.T. Bowlin's point, programming language is more like a language, you can always learn more, but there's a point it seems to be unnecessary.
2. Then you ask what language should be used to work on deep learning. I will say *mathematics*, because once you understand the greek symbols, you can translate all these symbols to code (approximately). So if you ask me what you need to learn to hack tensorflow, "Mathematics" would be the first answer, yes, the package is written by Python/C++/C, but they won't be even close in my top-5 answers. Because if you don't know what Backprop is, knowing how C++ destructor works can't make you an expert of TF.
3. The final thing is you mentioned the term "level". What does this "level" mean? So is it like chess-rating or go-rating that someone has higher rating, they will have a better career in deep learning? It might work for competitive programming...... but real-life programming doesn't work that way. Real-life programming means you can read/write a complex programs. e.g. in C++, you use a class instead of repeating a function implementation many times to reduce programming. Same as templates. That's why class and templates are important concept and people debate their usages a lot. How can you give "levels" to such skills?

Lastly I would say if you seriously want to focus on one language, consider python, but always learn a new programming language yearly. Also pick up some side-projects, both your job and side-projects would usually give you ideas which language you should learn more.

Artificial Intelligence and Deep Learning Weekly

©2017-2019 Artificial Intelligence and Deep Learning Weekly | [Sponsorship](http://aidl.io/sponsorship/index.html)
