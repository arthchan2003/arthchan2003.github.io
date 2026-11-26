---
title: "Issue 59 - Google I/O 2018, in particular, Duplex"
date: 2019-07-18
---

# Issue 59 - Google I/O 2018, in particular, Duplex

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 59 *May 12th 2018* ](http://aidl.io/issues/59/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we cover Google I/O. In particular, Google Duplex has some surprising backlashes. Check out our fact-checking section. 

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues!

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 140,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## News

### [CMU launches AI Undergraduate degree](https://www.cs.cmu.edu/news/carnegie-mellon-launches-undergraduate-degree-artificial-intelligence)

CMU has always been one of the top schools in computer science, artificial intelligence and machine learning. They were early to start specialized graduate programs on machine learning/AI, such as programs from the Machine Learning institute, or [Robotic Institute](https://www.ri.cmu.edu/). They are now starting an entire undergraduate program just on AI. 

[cmu.edu](https://www.cs.cmu.edu/news/carnegie-mellon-launches-undergraduate-degree-artificial-intelligence)

---

### [Google Research is now Google AI](https://www.forbes.com/sites/samshead/2018/05/09/google-goes-all-in-on-artificial-intelligence-as-google-research-becomes-google-ai/#1de6374d4be3)

Google Research changed its name to Google AI. Google and other Alphabet subsidiaries are deeply involved in AI, and currently many Google products are actually deep-learning based. If Google wasn't all in before, it certain is now. 

[forbes.com](https://www.forbes.com/sites/samshead/2018/05/09/google-goes-all-in-on-artificial-intelligence-as-google-research-becomes-google-ai/#1de6374d4be3)

---

### Deals

- [Tailor Brands raises $15.5M](https://venturebeat.com/2018/05/09/tailor-brands-raises-15-5-million-to-grow-its-ai-powered-branding-platform-for-non-creatives/)
- [Gamalon raises $20M](https://venturebeat.com/2018/05/08/intel-leads-20-million-investment-in-gamalon-to-help-companies-interpret-customer-messages-through-natural-language-processing/) - Sounds like Gamalon has moved away from [Bayesian program synthesis](https://techcrunch.com/2017/02/14/gamalon-leverages-the-work-of-an-18th-century-reverend-to-organize-unstructured-enterprise-data/).
- [Nokia bought SpaceTime Insight](https://techcrunch.com/2018/05/07/nokia-acquires-spacetime-insight-adding-ai-to-its-internet-of-things-business/)

Artificial Intelligence and Deep Learning Weekly 

---

### AI Summary of Google I/O 2018

Google I/O, just like last year, kept churning out interesting products: 
- [Duplex](https://www.youtube.com/watch?v=bd1mEm2Fy08), a dialogue system which sounds very close to humans with natural understanding capability,
- [Smart Compose](https://www.blog.google/products/gmail/subject-write-emails-faster-smart-compose-gmail/) - automatic suggestions based on machine learning,
- [TPU 3.0](https://techcrunch.com/2018/05/08/google-announces-a-new-generation-for-its-tpu-machine-learning-hardware/) - TPU 3.0, yet another upgrade of Google's revolutionary ASIC-based neural network chip,
- [Google ML Kit](https://techcrunch.com/2018/05/08/googles-ml-kit-makes-it-easy-to-add-ai-smart-to-ios-and-android-apps/) - Google ML Kit, more a new interface to add Google AI product to apps.

Duplex has some surprising [backlashes](https://www.theverge.com/2018/5/11/17340894/google-duplex-all-party-consent-state-eavesdropping) after Google I/O. Some of these, in our view, could be misunderstanding in technicalities. See our fact-checking section on our analysis. In particular, as impressive as it is, Duplex is not AGI. 

Artificial Intelligence and Deep Learning Weekly

## Factchecking

### [Fact-checking: Google Duplex/AI](https://ai.googleblog.com/2018/05/duplex-ai-system-for-natural-conversation.html)

Google Duplex has been making waves last few days. WaPo has an [article](https://www.washingtonpost.com/news/the-switch/wp/2018/05/08/a-google-program-can-pass-as-a-human-on-the-phone-should-it-be-required-to-tell-people-its-a-machine/?noredirect=on) on whether such intelligent assistant technology would be too close to human. And of course, you will see ten thousands of posts in the next few months saying "AGI is coming!" So here's some pre-emptive fact-checking. 

So first-thing-first, Google Duplex is not an AGI. Here is an excerpt from the blog:

"One of the key research insights was to constrain Duplex to closed domains, which are narrow enough to explore extensively. Duplex can only carry out natural conversations after being deeply trained in such domains. *It cannot carry out general conversations.*" (Emphasis is mine.)

Google is Google, and their researchers are the honest bunch. I guess after learning from how the public perceive AI in the past (e.g. Facebook [was said to "kill" its own AI](https://qz.com/1043365/facebook-didnt-kill-its-language-building-ai-because-it-was-too-smart-it-was-actually-too-dumb/)), they are always very careful when they write.

But you might ask, is Duplex still a good technical achievement? Unequivocal yes. In some sense, Google researchers are understating. Unlike commercial dialogue systems in the past, their method is trainable. More interestingly, they are using end-to-end neural network to come up with the best response. So this approach goes beyond the two usual methods we know: first is the hand-crafted dialogue response, which is costly to build. The second is the seq2seq approach.

More on the second approach: Many of you might have learned it from deeplearning.ai (Course 5) already. An NNMT systems can be used as a dialogue system as well. But that is making a big assumption: i.e. dialogue system can be modeled as a machine translator. Google is not taking such an approach. From the diagram in the Google's blog post, you also see that the network has context as input. This is an old idea in dialogue systems, but it's interesting to see it is applied in neural networks.

This is what we have, so far the Google hadn't released any technical papers about the Duplex. So if we see it, we will look into the issue deeper.

[googleblog.com](https://ai.googleblog.com/2018/05/duplex-ai-system-for-natural-conversation.html)

## Blog Posts

### [How Ian Goodfellow Failed](http://www.veronikach.com/how-i-fail/how-i-fail-ian-goodfellow-phd14-computer-science/)

Ian Goodfellow gave an honest and heartfelt interview about he failed before he was famous. The part we like the most? Here: 

"12. What is the best piece of advice you could give to your past self?

I wish I’d used some of those GPUs I bought for deep learning to mine some bitcoin."

[veronikach.com](http://www.veronikach.com/how-i-fail/how-i-fail-ian-goodfellow-phd14-computer-science/)

## Video

### [Emojify by Dibakar Saha](https://github.com/evilport2/emojify)

One of our members at AIDL, Dibakar Saha, always churn out interesting projects in computer vision. This time is emojify, which can turn analysis human expression and dup it with emoji. See his thread [on AIDL](https://www.facebook.com/dibakar.saha.750/posts/2151590888405342) too? 

[github.com](https://github.com/evilport2/emojify)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 140,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760 

Artificial Intelligence and Deep Learning Weekly
