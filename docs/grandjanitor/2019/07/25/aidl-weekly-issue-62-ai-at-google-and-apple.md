---
title: "AIDL Weekly Issue #62 - AI at Google and Apple"
date: 2019-07-25
---

# AIDL Weekly Issue #62 - AI at Google and Apple

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 62 *June 9th 2018* ](http://aidl.io/issues/62/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we look at AI development of two industry giants: Google and Apple. Google recently stopped working on [project Maven](https://www.theverge.com/2018/6/1/17418406/google-maven-drone-imagery-ai-contract-expire), a high-profile government drone project, and this week we see CEO publish "AI at Google: our principles" to create values on how Google should use AI. See our coverage of the piece.

On the other hand, Apple, another powerhouse in the commercial AI, is now trying to establish her presence. Would she succeed? We have two pieces this week for you to think and ponder.

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues.

---

Also check out our sponsor this week: [CVPR Daily](https://www.rsipvision.com/feel-at-cvpr-without-being-at-cvpr/), published by RSIP Vision?

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 147,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## Sponsor

[*[image not recovered: original_ratio_extra_large_340dfa2f-7c45-48a7-998a-9c641c0b99fc.jpg]*](https://www.rsipvision.com/feel-at-cvpr-without-being-at-cvpr/) 

### [Feel at CVPR without being at CVPR!](https://www.rsipvision.com/feel-at-cvpr-without-being-at-cvpr/)

CVPR Daily is the official magazine published by RSIP Vision during CVPR, the main yearly conference on Computer Vision and Pattern Recognition. 

The CVPR Daily includes news, highlights, lectures, interviews and presentations from the conference and it is sent every day to all the attendees of CVPR, which this year is held June 18-22 in Salt Lake City, Utah.

You also can receive the CVPR Daily news in your mailbox, every day for free.

Fill the form [here](https://www.rsipvision.com/feel-at-cvpr-without-being-at-cvpr/) and subscribe for free to this year's three CVPR Daily magazines.

It's a free service from RSIP Vision, global leader in deep learning and computer vision, to the algorithm community worldwide.

Enjoy!

[rsipvision.com](https://www.rsipvision.com/feel-at-cvpr-without-being-at-cvpr/)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Core ML 2](https://venturebeat.com/2018/06/04/apples-core-ml-2-is-30-faster-cuts-ai-model-sizes-by-up-to-75/)

At WWDC, Apple stresses that new Core ML2 improve model speed by 30%, and reduce the size of model by 75%. Impressive enough, is Apple's strategy viable? See our next piece.

[venturebeat.com](https://venturebeat.com/2018/06/04/apples-core-ml-2-is-30-faster-cuts-ai-model-sizes-by-up-to-75/)

---

### [Pivots to Automation? Or have an AI bakeoff?](https://www.zdnet.com/article/wwdc-2018-apple-enables-siri-to-handle-shortcuts-pivots-to-automation-over-ai-bakeoff/)

The rumor before WWDC 2018 was that Apple is going to do something on AI, in particular Siri. But what we see now, on the other hand, is Apple seems to rather pivot to Siri automation, than have direct competition with MS, Google and Amazon.

Is Apple's strategy viable? Here are couple of thoughts: 
- Apple's AI development is more developer-centric. For example, releasing Core ML 2 which we just saw this week are more catered to practical applications, rather than research.
- We can say something similar about the decision of pivoting the Siri shortcuts. To be honest, shortcuts sounds less interesting than intelligent assistant which was released at Google I/O. But then Siri is still a product of AI, which is based on years of research in automatic speech recognition (ASR) and dialogue systems. So again, pivoting to Siri shortcuts is more along the line of Apples' developer-centric strategy.
- Just to comment from the perspective of ASR: While allowing developers adding Siri shortcuts sounds easy, it's actually a tough task technically - usually ASR development are benchmarked and measured through a fixed vocabulary and grammar. Allowing developers to customize shortcut would mean that you are confident that certain sets of word and its arbitrary combination would attain good ASR performance.

All-in-all, we believe Apple is taking a different route from other big companies such as Google which has a strong focus on AI research. Apple's approach is more to preserve her developer base. And when you look at it deeply, it is not less of a feat from other what other companies do.

[zdnet.com](https://www.zdnet.com/article/wwdc-2018-apple-enables-siri-to-handle-shortcuts-pivots-to-automation-over-ai-bakeoff/)

---

### Deals

- [Forward X $10 Million](https://venturebeat.com/2018/05/29/forwardx-raises-10-million-for-ai-powered-luggage-that-follows-you/)
- [Hailo $12.5 Million Series A](https://techcrunch.com/2018/06/05/hailo-raises-a-12-5m-series-a-round-for-its-deep-learning-chips/)
- [Zebra $30 Million Series C](https://techcrunch.com/2018/06/07/zebra-medical-vision-gets-30m-series-c-to-create-ai-based-tools-for-radiologists/)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [AI at Google : The 7 Principles](https://www.blog.google/topics/ai/ai-principles/)

"AI at Google, the principe" was published 2 days ago. It reads like a sudden change of mind. Given the mantra of Google : don't be evil. (It was [dropped](https://en.wikipedia.org/wiki/Don%27t_be_evil) lately.), you would hope that Google published these principles *before* working on a defense project. Yet it only comes two days ago when Google already establish a sales department for selling AI research to agencies. And of course, pulling out from project Maven doesn't mean that Google would stop acting like a defense contractor in the future.

What we know: the conflict between Google the web search company and Google the defense contractor will continue. So stay tune?

[blog.google](https://www.blog.google/topics/ai/ai-principles/)

---

### [Keras 2.2.0 is here](https://github.com/keras-team/keras/releases/tag/2.2.0)

Keras 2.2.0 was just released. Perhaps the most important change is allow user to write a new model through Model subclassing.

[github.com](https://github.com/keras-team/keras/releases/tag/2.2.0)

---

### [Real Time t-SNE](https://ai.googleblog.com/2018/06/realtime-tsne-visualizations-with.html?m=1)

Google presents yet another interesting results which can speed up t-SNE, the very versatile visualization algorithm. So what did Google researchers do?

In essence, there are two parts. First through a sampling method, they figure out a way to make the nlog(n) calculation in t-SNE to be linear. Then they also figure out how to draw the point faster by using WebGL texture function. The two combined was why the approach is much faster and can be real-time.

The source code can be found at [here](https://nicola17.github.io/tfjs-tsne-demo/). You may also read the paper at [here](https://arxiv.org/abs/1805.10817).

[googleblog.com](https://ai.googleblog.com/2018/06/realtime-tsne-visualizations-with.html?m=1)

---

### [A Good Advice of Debugging Python Script](https://twitter.com/dennybritz/status/1003959960206761984)

Denny Britz on Twitter wrote about the Zen of Debugging Python Programs, while by itself is not just about AI. I think it's very suitable for our group.

"How to debug Python, for beginners: 
1. Carefully read the exception message. Repeat it to yourself 3 times, slowly.
2. Step away from the computer. Ideally, lie down somewhere.
3. Close your eyes, take 10 deep breaths.
4. You will have found your mistake."

[twitter.com](https://twitter.com/dennybritz/status/1003959960206761984)

---

### [Using AI to turn People into Anime Art](https://kotaku.com/using-a-i-to-turn-real-people-into-anime-art-1826598115)

Based on the paper published last year, ["Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks"](https://arxiv.org/abs/1703.10593) ,from Fudan University.

[kotaku.com](https://kotaku.com/using-a-i-to-turn-real-people-into-anime-art-1826598115)

## About Us

### Announcement: About AIDL Posting

From Jun 10, 2018, all posts at the [AIDL group](https://www.facebook.com/groups/DeepNetGroup/) would be first approved by admins/mods before they can appear in the main forum, or we call it the "pre-approval" system. This changes our long-time policy of "post-approval", i.e. we allowed anyone to post but only remove the post afterward. Read below for further discussion.

Details: Since AIDL's inception 2 years ago, we have adopted a posting system which allows members to post anything, but only close/remove posts afterward. Unfortunately, our surprisingly rapid growth made this system unscalable. It's getting harder for admins/mods to manually remove all spammy commercial or irrelevant posts from the forum. Furthermore, since posts would pop up on members feed, these irrelevant posts has been hurting our group's reputation as an informative news source.

Perhaps more importantly, we want to listen to our members: Many members voice their concerns of repetitive beginner posts and spams, there are also more told us that they decide to leave the group because posts have low quality.

Our change will make all posts go through admin first before appearing in the main forum. We will still keep general discussion, but they will only appear in several designated threads from the forum.

If you left AIDL because of spam, note that we are taking steps to improve post quality. We hope you like our new policy. If you have any questions, feel free to talk with admins/mods.

Artificial Intelligence and Deep Learning Weekly

---

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 147,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
