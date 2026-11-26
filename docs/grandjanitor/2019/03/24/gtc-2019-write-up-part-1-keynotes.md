---
title: "GTC 2019 Write-Up Part 1: Keynotes"
date: 2019-03-24
categories: ["review"]
---

# GTC 2019 Write-Up Part 1: Keynotes

# Introduction

Inside every serious deep learning house, there is a cluster of machines. And inside each machine, there is one GPU card. Since Voci is a serious deep learning house, we end-up owning many GPU cards. 

\* \* \*

By now, no one would disagree deep learning has reinvigorated the ASR industry. Back in 2013, Voci was one of the earliest startups which adopt deep learning. It was the time when the [Hinton's seminal paper](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/38131.pdf) [1] was still fresh. Some brave souls in Voci, including Haozheng Li, Edward Lin and John Kominek decided to just jump to this then-radically new approach. My hybrid role, as part researcher, and part software maintainer also started then. We did several other things in Voci, but none of them is as powerful as deep learning.

\* \* \*

But I digress. Where were we?

Yep, Voci has a lot of GPU cards. At first you might have the impression that GPU is more like a "parallellizable-CPU". But then the reality is because GPU is specifically made for high-performance computing applications such as graphics rending. A GPU has a very different design from CPU. If you are a C-programmer, you can pick up ideas of [Compute Unified Device Architecture](https://en.wikipedia.org/wiki/CUDA) (or CUDA as Nvidia love acronyms). But then your intuition which was developed from years of programming CPU (Intel or Intel-like) would be completely wrong.

So we realized all these at Voci, that's why part of our focus is to understand how GPU works, and that's why both me and my boss , John Kominek, decided to travel to Silicon Valley and attend GTC 2019, which is the short for GPU Technology Conference.

This article is Part I of my impression for both on the Keynotes by Jensen Huang, I will also take a look of the Poster session as well as the various booths. But I will leave more technical ideas in the next post. 

*[image not recovered: Jen-Hsun_Huang_Headshot_15313247387.jpg]*

# Huang's Keynotes

We love Jensen Huang! He is walking around the stage, enthusiastically explain to the ten thousand audience what's new with Nvidia. But let's round up the top-5 announcements?

https://www.youtube.com/watch?v=Z2XlNfCtxwI

1. [CUDA-X](https://www.nvidia.com/en-us/technologies/cuda-x/): More like a convergence among different technologies within Nvidia. CUDA, as we know now, is more like a programming language. Whereas CUDA-X is more an architecture term within Nvidia, which encompass various technologie, such as RTX, HPC, AI etc.
2. [Mellanox Acquisition](https://nvidianews.nvidia.com/news/nvidia-to-acquire-mellanox-for-6-9-billion): Once you look at it, strength of Nvidia against its competitors is not just about the GPU cards. Nvidia also put an infrastructure that enables customers to build system among GPU cards. So of course, the first you want to think about is how do you use multiple machines, each with separate cards? Now, that explains the Mellanox deals ([Infiniband?](https://en.wikipedia.org/wiki/InfiniBand)). That also explains Huang spent a lion share of his time to talk about data center. How different containers are talking with each other and how that generate traffics. In a way, it is not just about the card, it is about the card and all peripherals. In fact, it is about the machines and their ecosystem.
3. [The T4 GPU](https://venturebeat.com/2019/03/18/aws-adopts-nvidias-tesla-t4-chip-for-ai-inference/): The way Nvidia market it, T4 is suitable for data-centers which focus on AI. Currently benchmarking says, a [T4 has lower speed than V100, but has a higher energy efficiency](https://www.servethehome.com/nvidia-supercomputing-2018-announcements/nvidia-sc18-tesla-t4-v-tesla-v100/). So this year big news on the server side is [AWS has now adopted T4 in their GPU instances](https://blogs.nvidia.com/blog/2019/03/18/t4-gpus-amazon-web-services/).
4. [Automatic Mixed Precision](https://developer.nvidia.com/automatic-mixed-precision) (AMP) : What about news for us techies? Well, the most interesting part is perhaps AMP is now available in [Tensorcores](https://www.nvidia.com/en-us/data-center/tensorcore/). So why precision is so important then? Well, once you create a production system on either training or inference. The first thing you will realize is that it takes a lot of GPU memory. How to reduce it? Reducing precision is one way to go. But when you reduce precision, it's possible that quality of your tasks (training or inference) would degrade. So it's a tricky problem. Couple of years ago, [researchers](https://arxiv.org/abs/1710.03740) have figured out couple of methods. Now you can implement it yourself, but then Nvidia decided to put it in Tensorcore directly.

Oh, FYI, keynotes feel like a party. 

*[image not recovered: IMG-1456.jpg]*

# 

# Booths

In a large conference like GTC, you can learn many interesting aspects of your technology. Unlike a pure academic conference, GTC also has the aspect of being a trade-show. So how does if feels like? Here are some impressions: 
1. **All GPU peripherals**: Once you get a GPU card, perhaps the bigger problem is how to install them and make them usable. Do you think it's easy to do so? It should be plug and play right? Nope, in reality, working with hardware GPU ca

    *[image not recovered: 55514065_2374231572610739_1345558712047108096_n.jpg]*

    rds is a difficult technical problem. Part of the issues is heat dissipation. If you don't trust me, try to get a few consumer grades GPU card into a same box, you can use it to be a heater in Boston! That's perhaps why there are so many vendors other than Nvidia try to get into the game of building GPU-based servers. They are probably one third of the booths in the show.
2. **Self Driving Car/LiDAR** I don't envy my colleagues in the SDC industry. Actually when will see Level 4 self-driving? Anyway, people do want to see SDC in thenear f

    *[image not recovered: IMG-1614.jpg]*

    uture. So that's why you see all SDC vendors show up in the conference.
3. **The Ecosystem:** Finally, you also see demonstrations of various clouds which use GPU.

Finally, here is a picture of donuts:There are more than 100 vendors showcasing their AI products. If you go t

o look at all the booths, you are going to get very hungry.

*[image not recovered: 55533177_2283697271909162_6961504789762932736_n-1.jpg]*

Wait for Part II!!!

Arthur Chan

Footnote: [1] The paper was actually jointly written by researchers from Google, IBM and Microsoft back then. Notice that these researchers were from separate (rival) groups and they seldom wrote joint paper, not to say about ground-breaking results.
