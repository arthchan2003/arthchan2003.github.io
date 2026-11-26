---
title: "A read on \"ImageNet Training in Minutes\""
date: 2018-05-09
---

# A read on "ImageNet Training in Minutes"

Yes, you read it right, Imagenet training in 24 mins. In particular, an Alexnet structure in 24 mins and Resnet-50 in 60 mins. In terms of Alexnet, in fact, You's work break the previous Facebook's record: 1 hour for Alexnet training. Last time I check, my slightly-optimized training with one single GPU will take ~7 days. Of course, I'm curious how these ideas work. So this post is a summary.

\* For the most part, this is not GPU works. This is mostly more a CPU platform but accelerated by Intel Knight Landing (KNL) accelerator. Such accelerator is very suitable in HPC platforms. And there are couple of supercomputers in the world which were built up to 2000 to 10000 such CPUS. 

\* The gist of why KNL is good: it can divide processors on chip with the memory well. So unlike many clusters you might encounter with 8 to 16 processors, memory bandwidth is much wider. That's usually is a huge bottleneck in training speed.

\* Another important line of thought here is "Can you load in more data per batch?" because that allows calculation to be parallelized much easier. The first author, You's previous work already allow the Imagenet batch goes from the standard, 256-512 to something like 8192. This thought has been there for a while, perhaps since Alex Krishevzky. His previous idea is based on adaptive calculation of learning rate per layers. Or Layer-wise Adaptive Rate Scaling (LARS).

\* You then combined LARS with another insight from FB researchers: a slow warmup in learning rate. That results in his current work. And it is literally 60% faster than the previous work.

Given what we know, it's thinkable that the training can be even faster in the future. What has been blocking people seem to be 1) No. of CPUs within a system 2) How large a batch size can be loaded in. And I bet after FB read You's paper, there will be another batch of improvement as well. How about that? Don't you love competition in deep learning?
