---
title: "AIDL Weekly Issue 31 - Get Rid of Backprop and Start Over"
date: 2019-07-02
---

# AIDL Weekly Issue 31 - Get Rid of Backprop and Start Over

# [Issue 31 *September 23rd 2017* ](http://aidl.io/issues/31/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Prof. Hinton said we should just get rid of backpropagation and start over. What does he mean? Let's find out in this issue. We also include the link of all videos from deeplearning.ai here as well. Of course, also check out our blog and paper sections. 

---

We will be hosting an AIDL Meetup at the *AI World Conference* in Boston on Dec 12 at 6:15pm where some cutting-edge AI companies will present. We got FREE tickets for you all! Come join us in person if you can!!

*Attack of the AI Startups* - https://aiworld.com/sessions/mlai/ at AI World - aiworld.com

All attendees need to register to attend. To register, please go to: https://aiworld.com/live-registration/ To receive your FREE expo pass (thru September 30), use priority code: **AIWMLAIX**

To receive a $200 discount off of your 1, 2 or 3 day VIP conference pass, use priority code: **AIWMLAI200**

AI World is the industry's largest independent event focused on the state of the practice of enterprise AI and machine learning. AI World is designed to help business and technology executives cut through the hype, and learn how advanced intelligent technologies are being successfully deployed to build competitive advantage, drive new business opportunities, reduce costs and accelerate innovation efforts.

The 3–day conference and expo brings together the entire applied AI ecosystem, including innovative enterprises, industry thought leaders, startups, investors, developers, independent researchers and leading solution providers. Join 100+ speakers and 75+ sponsors and exhibitors and thousands of attendees. Other than that, we also include some of our analyses on two paper as well as multiple interesting links for blogs and open source resources. So check it out!

---

As always, if you like our newsletter, subscribe/forward it to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Hinton's Suspicion of Back Propagation](https://www.axios.com/ai-pioneer-advocates-starting-over-2485537027.html)

When the father of deep learning is suspicious of something, you listen. Prof. Hinton believes we need to get rid of backpropagation. To quote Axios: 

> But Hinton suggested that, to get to where neural networks are able to become intelligent on their own, what is known as "unsupervised learning," "I suspect that means getting rid of back-propagation."

The first thing we should ask is : Is the quote real? When we search the quote online, it all links back to the Axios article. That means Axios is our only source. Notice this view is quite different from researchers such as Yoshua Bengio. It's also surprising because he is one of the inventors of the [algorithm](https://www.iro.umontreal.ca/~vincentp/ift3395/lectures/backprop_old.pdf) (together with David Rumelhart and Ronald Williams). 

What does the Professor really means by "unsupervised technique" then? No one knows. Our guess would be some types of unsupervised models such as [Boltzmann machine](https://en.wikipedia.org/wiki/Boltzmann_machine) which can automatically learn the distribution of the data.

[axios.com](https://www.axios.com/ai-pioneer-advocates-starting-over-2485537027.html)

## Blog Posts

### [Udacity added a New "Introduction to Self Driving Cars" Nanodegree](https://techcrunch.com/2017/09/19/udacity-adds-a-new-intro-to-self-driving-cars-nanodegree/)

For us, any opportunity to learn is important. This new Udactiy class seems to be a preliminary class of its standard SDC nanodegree. There are also 400 scholarships provided by Lyft. 

[techcrunch.com](https://techcrunch.com/2017/09/19/udacity-adds-a-new-intro-to-self-driving-cars-nanodegree/)

---

### [Sebastian Ruder's review of EMNLP 2017](http://blog.aylien.com/highlights-emnlp-2017-exciting-datasets-return-clusters/?utm_content=60468229&utm_medium=social&utm_source=twitter)

This is summary written by Sebastian Ruder which summarize trends and news of EMNLP 2017. 

[aylien.com](http://blog.aylien.com/highlights-emnlp-2017-exciting-datasets-return-clusters/?utm_content=60468229&utm_medium=social&utm_source=twitter)

## Open Source

### [Unity RL framework](https://blogs.unity3d.com/2017/09/19/introducing-unity-machine-learning-agents/)

This post from Arthur Juliani, on the Unity RL framework. It looks fairly impressive as it support multiple agent types as well as more advanced features such as curriculum learning. Can it be a replacement of an OpenAI gym? So far we know, OpenAI maintenance seems to be inconsistent. Perhaps another framework/toolkit is needed. 

[unity3d.com](https://blogs.unity3d.com/2017/09/19/introducing-unity-machine-learning-agents/)

## Video

### [CMU Deep Learning on NLP Class](https://www.youtube.com/user/neubig/playlists)

This is a still on-going but very promising sets of videos from CMU on deep learning on NLP. Graham Neubig has written some great tutorials on NNMT, so I think his teaching should be very valuable for learners. 

[youtube.com](https://www.youtube.com/user/neubig/playlists)

---

### [deeplearning.ai official Youtube Channel](https://www.youtube.com/channel/UCcIXc5mJsHVYTZR1maL5l9w)

It sounds like a new release from the course staffs and you can find all course videos there. 

---

Btw, we are often asked in one of our satellite groups, [Coursera deeplearning.ai](https://www.facebook.com/groups/DeepLearningAISpecialization/) on when would Course 4 and 5 will be released. As far as we know, the staff has sent out a [mail](https://www.facebook.com/photo.php?fbid=10159373724060319&set=gm.1975109682733881&type=3&theater) to the students, stating the Course 4 would start in early October, and Course 5 would start soon afterward.

[youtube.com](https://www.youtube.com/channel/UCcIXc5mJsHVYTZR1maL5l9w)

## Paper/Thesis Review

### [StarSpace: Embed All The Things!](https://arxiv.org/abs/1709.03856)

This is StarSpace, a new embedding method from FB's Weston's group. So what's so special about the technique? In our view, the generality of the technique is the first thing to note - it was able to unified supervised and unsupervised embedding, as well as collaborative filtering which is commonly used in recommendation system. 

Here are some details of how the method works: First of all, the optimization is implemented as ranking loss, which one usual choice is just a max margin loss or hinge loss. The authors also tried out softmax, but they found that ranking loss is giving better results across the board. What we don't know is perhaps whether more advanced losses such as weight ranking loss or WARP was being used.

Just a digression: Is supervised embedding a thing? Indeed it is, it was also one of the Weston's research as well. [Here](http://emnlp2014.org/tutorials/8_notes.pdf) is a fairly good review.

By comparing with many existing STOA results such as FastText in unsupervised embedding, and WSABE in supervised embedding, the authors show that the techniques show across the board improvement. Perhaps why the author name the techniques as "\*-Space".

[arxiv.org](https://arxiv.org/abs/1709.03856)

---

### [Imagenet Training in 24 mins - A New Record from Berkeley. ](https://arxiv.org/abs/1709.05011)

Yes, you read it right, Imagenet training in 24 mins. In particular, an Alexnet structure in 24 mins and Resnet-50 in 60 mins. In terms of Alexnet, in fact, You's work break the previous Facebook's record: 1 hour for Alexnet training. Last time we checked, our slightly-optimized training with one single GPU will take ~7 days. Of course, we're curious how these ideas work. So this post is a summary: 
- This is not based on GPUs. This is mostly a CPU platform but accelerated by Intel Knight Landing (KNL) accelerator. Such accelerator is suitable in HPC platforms. And there are couple of supercomputers in the world which were built up to 2000 to 10000 such CPUS.
- The gist of why KNL is good: it can divide processors on chip with the memory well. So unlike many clusters you might encounter with 8 to 16 processors, memory bandwidth is much wider. That's usually is a huge bottleneck in training speed.
- Another important line of thought here is "Can you load in more data per batch?" because that allows calculation to be parallelized much easier. The first author, You's previous work already allow the Imagenet batch goes from the standard, 256-512 to something like 8192. This thought has been there for a while, perhaps since Alex Krishevzky. His previous idea is based on adaptive calculation of learning rate per layers. Or Layer-wise Adaptive Rate Scaling (LARS).
- You then combined LARS with another insight from FB researchers: a slow warmup in learning rate. That results in his current work. And it is literally 60% faster than the previous work.

Given what we know, it's possible that the training can be even faster in the future. What has been blocking people seem to be 1) No. of CPUs within a system 2) How large a batch size can be loaded in. And I bet after FB read You's paper, there will be another batch of improvement as well. How about that? Don't you love competition in deep learning? 

You's previous work: [*Large Batch Training of Convolutional Networks*](https://arxiv.org/pdf/1708.03888.pdf)

FB 1 hour work: [*Accurate, Large Minibatch SGD: Training ImageNet in 1 Hour*](https://arxiv.org/pdf/1706.02677.pdf)

[arxiv.org](https://arxiv.org/abs/1709.05011)
