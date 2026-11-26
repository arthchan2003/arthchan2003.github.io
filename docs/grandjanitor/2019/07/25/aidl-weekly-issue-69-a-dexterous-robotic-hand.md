---
title: "AIDL Weekly Issue 69 - A Dexterous Robotic Hand"
date: 2019-07-25
---

# AIDL Weekly Issue 69 - A Dexterous Robotic Hand

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 69 *August 6th 2018* ](http://aidl.io/issues/69/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we look deep into latest OpenAI's work on dexterous robotic hand, and ask if feed-forward networks are just as good as the recurrent ones.

As always, if you like our newsletter, feel free to share it with your friends and colleages.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 165,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Skyline $18M](https://techcrunch.com/2018/07/31/skyline-ai-raises-18m-series-a-for-its-machine-learning-based-real-estate-investment-tech/)
- [RideOS Series B](https://techcrunch.com/2018/08/02/rideos-series-b-self-driving-cars/)

Artificial Intelligence and Deep Learning Weekly

---

### [US AI Patent Filings](https://www.wired.com/story/despite-pledging-openness-companies-rush-to-patent-ai-tech)

As you can imagine, it grows explosively in the last 5 years. So ask: what if Tensorflow has patented ideas in it? And how would software patents affect AI production systems?

[wired.com](https://www.wired.com/story/despite-pledging-openness-companies-rush-to-patent-ai-tech)

## Blog Posts

### [OpenAI's Robotic Hand can Spin a Cube!](https://blog.openai.com/learning-dexterity/)

After stunning results such as AlphaGo, you would think it's hard for AI to surprise again. But then OpenAI is still churning out interesting results day by day, and the latest result is to make a dexterous robotic hand.

There are many nuance in their results, and you may read their blog post (as linked), and [their paper](https://arxiv.org/abs/1808.00177). But we want to highlight several things: 
- As in many AI work, the authors were using simulated data in training. But surprisingly enough, using real-data doesn't help much. Perhaps it has to do with scalability, you can generate several order of magnitude of data than capturing real-data.
- When researchers observed how robots manipulate the cube, they found that gripping happens in between index and middle finger, which is different from human, which use index finger and thumb. OpenAI's researchers believe it has to do with the robotic hand has a flexible index finger.

Anyway, this sounds like an interesting and breakthrough research to us. Of course the natural dexterity shows in [their video](https://www.youtube.com/watch?v=DKe8FumoD4E&feature=youtu.be) is impressive. But also robotic hand manipulation is just one of the examples where there are high-dimensional outputs to learn and require reinforcement learning to learn well. Other example perhaps is walking or climbing stairs. Solving this one problem well may lead to solving many difficult problems in the future.

[openai.com](https://blog.openai.com/learning-dexterity/)

---

### [OpenCV Object Tracking by Adrian Rosebrock](https://www.pyimagesearch.com/2018/07/30/opencv-object-tracking/)

Here is another tutorial written by Joey Rosebrock. This time is a hand-on implementation on object detection using 8 algorithms provided by OpenCV. As always you can always learn something from Rosebrock's writing.

[pyimagesearch.com](https://www.pyimagesearch.com/2018/07/30/opencv-object-tracking/)

---

### [When Feed-forward model is as good](http://www.offconvex.org/2018/07/27/approximating-recurrent/)

As you know, RNN or BLSTM is now taught in all standard deep learning courses. Conventional wisdom tells us that RNN usually outperforms the corresponding feed-forward networks (FFN) with limited context. Yet FFNs are still more prevalent than RNNs. Or practitioners just chose to use FFN because it parallelizes better.

So that begs a question - is FFN actually better than RNN in some problems? This is what this post, written by John Miller, is driving at. In fact, Miller summarizes several well-known systems in last few years which find convnets to give better performance. Another intriguing result is from Google's technical report: "N-gram Language Modeling using Recurrent Neural Network Estimation" which shows that a 13-gram may performs as well as an well-trained RNN.

[offconvex.org](http://www.offconvex.org/2018/07/27/approximating-recurrent/)

## Member's Question

### AIDL Admin's Feedback on the New Pre-approval System.

*An answer from Arthur*: Zubair Ahmed posted a thread on getting everyone's feedback about our now 2-month-old pre-approval system. So far, most feedbacks we got are positive. I just want to give you my take on the new system.

First off, our system (or think of it as post-approval) was meant to give members freedom to post what they like.

Unfortunately, self-inspection from all members couldn't filter out all malicious postings such as porns, religious and political messages which have nothing to do with AI, etc. Plus there are too many complaints about basic questions such as "How do I learn AI?" was asked repetitively.

So here comes our new pre-approval system. How does it really work in practice? Let me just give you a sample of my day, and how we processed different posts and decide if they should appear in the feed. I am not the only approver, but we have fairly consistent standard across admins/mods. So you will have a good feel of our work.

Daily, we receive 50-70 posts required to be approved. In my timezone, I will process around 40-50 of them. Here is a rough breakdown of them: 
- 10%: selling irrelevant products such as rolexes, web hosting. What I do: delete the post.
- 20%: technology-related but has nothing to do with AI. What I do: delete the post.
- 30%: AI-related news which comes from unreliable sources, or from a Page which just reposts a piece. Or sensational opinion about AI-related technology. What I do: I usually delete the post unless it reflect a certain zeitegeist in AI development.
- 10%: Members questions which are unclear. Usually these posts are poorly formatted and not proofread. These posts usually solicit angry responses from impatient AIDL members. What I do: sometimes I let them in, but comment on the quality of the questions. If they are "How do I learn AI?" I would just delete them.

Members questions which I have no idea the meanings are. Usually they are the results from poor formatting and poor or no proof-reading from the posters. They are usually gone because the post will only solicit angry response from the slightly more knowledgeable but impatient AIDL members. What I do: sometimes I let them in, but comment on the quality of the questions. But I don't mind to delete them. If they are "How do I learn AI?" Sorry, I would just delete them.

So the rest is what you see in the feed. That accounts for ~10-15 posts. If they are posts, they are original form the authors, if they are code, they share from the programmers. If they are questions, they are usually non-trivial. And their answers are good for everybody knows.

One questions members often asked is how does the pre-approval affect our workload as admin? I'll say : at the moment, it lighten up our load. The reason is we pretty much just used similar curation criteria before the pre-approval system. But now we see fewer group-wide outrages of poor quality posts. Spams such as porn, while infrequent, they are disruptive to our members', and thus our life.

There are some members just completely disagree with any pre-approval system. I'll say this: If you just look at the post breakdown, you should quickly notice that 60% of pending posts are inappropriate for the group. So we have always been removing them even before the system. We really tried to get the old system working, but it's too hard.

I'll also say we admins realize that we are just humans and can be biased and make mistakes. So let's say we keep an open-minded and feel free to give us feedbacks.

On a lighter note: me and Zubair Ahmed found that there are always someone suggest that ML should be used to replace us admins/mods. Of course, we also repeatedly pointed out that this is a cliche idea. But let's see how often they appear? :)

Artificial Intelligence and Deep Learning Weekly

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 165,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
