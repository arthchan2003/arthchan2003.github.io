---
title: "AIDL Weekly Issue 35 -"
date: 2019-07-05
---

# AIDL Weekly Issue 35 -

# [Issue 35 *October 21st 2017* ](http://aidl.io/issues/35/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

**Big announcement** - last week, we launched our own topic-based messaging app called Expertify, to help you connect with other AI and DL professionals in our 45,000-member community. More details below on why we rolled our own and specific AI / DL features we want to add to it over time... 

[Download Expertify iOS app](https://itunes.apple.com/app/id969850760)

We'd love for you you to try it and give us some feedback, if you are on iOS. We're working on a web app and a bit down the road, Android.

In other news, we heard of stunning news that AlphaGo beats itself again and created the first Go player which has Elo-rating over 5000.

In technical news, Google created a new activation function which works better than even ReLU. And we wrote a full review of Coursera deeplearning.ai Course 1, which was quite well-received in different networks.

---

As always, if you like our newsletter, feel free to subscribe/forward the letter to your colleagues.

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Attack of the AI Startups ](https://aiworld.com/sessions/mlai/)

We will be hosting an AIDL Meetup at the AI World Conference in Boston on Dec 12 at 6:15pm where some cutting-edge AI companies will present. We got FREE tickets for you all! Come join us in person if you can!! 

Attack of the AI Startups - https://aiworld.com/sessions/mlai/ at AI World - aiworld.com

All attendees need to register to attend. To register, please go to: https://aiworld.com/live-registration/ To receive your FREE expo pass (thru September 30), use priority code: AIWMLAIX

To receive a $200 discount off of your 1, 2 or 3 day VIP conference pass, use priority code: AIWMLAI200

AI World is the industry's largest independent event focused on the state of the practice of enterprise AI and machine learning. AI World is designed to help business and technology executives cut through the hype, and learn how advanced intelligent technologies are being successfully deployed to build competitive advantage, drive new business opportunities, reduce costs and accelerate innovation efforts.

The 3–day conference and expo brings together the entire applied AI ecosystem, including innovative enterprises, industry thought leaders, startups, investors, developers, independent researchers and leading solution providers. Join 100+ speakers and 75+ sponsors and exhibitors and thousands of attendees. Other than that, we also include some of our analyses on two paper as well as multiple interesting links for blogs and open source resources. So check it out!

As always, if you like our newsletter, subscribe/forward it to your colleagues!

[aiworld.com](https://aiworld.com/sessions/mlai/)

---

## News

### [We launched a messaging app to help AI / DL practitioners connect with one another. Here's why we rolled our own](https://itunes.apple.com/app/id969850760)

Many in our 45,000-person AIDL community have asked us if there's a way for them to interact with one another (advice, recruiting, where to get training data, keeping up with new research, etc.) in a more real-time fashion. Messaging apps are a dime a dozen (we looked at Slack, Telegram, etc.) but we haven't found one that is topic-based (that's not Reddit) and makes it easy for professionals to have high-quality group or 1-on-1 discussions in a simple format. 

The other big reason we rolled our own is that we want it to serve as a laboratory for practitioners to test various DL ideas and get feedback. There are many ways to customize the app to enable some DL-specific features that no other platforms have. For example, we may want to enable users to build or connect their chatbots, classifiers, anything else you can think of to our platform, test it and receive feedback from other DL practitioners. We are also exploring ways to use it as a way to crowdsource training data. The possibilities are endless.

We'd love for you to use it and help us define our roadmap, so we can build features that are useful to you and other folks in DL.

[Download Expertify iOS app](https://itunes.apple.com/app/id969850760)

[apple.com](https://itunes.apple.com/app/id969850760)

---

### [Facebook/Intel Collaboration](http://www.alphr.com/intel/1007400/facebook-has-worked-with-intel-on-a-deep-learning-ai-chip)

We heard last week Facebook is collaborating with Intel on their latest Nervanna chip. We saw the quote 

> We are thrilled to have Facebook in close collaboration sharing their technical insights as we bring this new generation of AI hardware to market,

from Intel CEO Brian Krzanich. We don't know much details yet. Will report more as we hear more. 

[alphr.com](http://www.alphr.com/intel/1007400/facebook-has-worked-with-intel-on-a-deep-learning-ai-chip)

---

### [Apple's SDC spotting. ](https://www.theverge.com/2017/10/18/16496182/apple-self-driving-car-project-titan-sensor-lidar)

Verge is running a piece Apple's SDC. There are certainly some big guns here : such as 6 Velodyne-made LIDARs. 

[theverge.com](https://www.theverge.com/2017/10/18/16496182/apple-self-driving-car-project-titan-sensor-lidar)

## Blog Posts

### [AlphaGo Zero Now Learn Go From Scratch](https://deepmind.com/blog/alphago-zero-learning-scratch/)

We heard from DeepMind again on a new development of AlphaGo. Once again, the team created an even stronger Go player. From an Elo rating standpoint, Master, the one we saw that beats Ke Jie, has rating ~4900. But Zero's rating is above ~5100. And it beats Alpha Go Lee in a record of 100 to 0. 

What's even more amazing is that Zero learns all by self-play - previous versions of AlphaGo has at least some human added feature. One more technical detail we like: instead of doing rollout to predict who would win, this time a neural network is used instead. So it is a rather drastic change from the system perspective.

[deepmind.com](https://deepmind.com/blog/alphago-zero-learning-scratch/)

---

### [Review of deeplearning.ai Course 1: Neural Networks and Deep Learning](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/)

This is written by Arthur, and it will address issues such as what Course 1 is about. Is it a difficult class? And should you take the class if you already have some experience? We will address those issues on the article. 

[thegrandjanitor.com](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/)

---

### [Mixed Precision Training](https://www.reddit.com/r/MachineLearning/comments/75phd2/r_mixed_precision_training/?st=j8ntr6wo&sh=e59130db)

Nice discussion on mixed precision training. It's a good complement if you'd like to read [the paper from Baidu recently](https://arxiv.org/abs/1710.03740). 

[reddit.com](https://www.reddit.com/r/MachineLearning/comments/75phd2/r_mixed_precision_training/?st=j8ntr6wo&sh=e59130db)

---

### [A Rare Glimpse of How "Hey Siri" Works. ](https://machinelearning.apple.com/2017/10/01/hey-siri.html)

This is a bit old but Apple's engineers wrote a new piece on how "Hey Siri" works. Or as we call it in the industry, keyword wakeup. The post has fairly detail explanation on what models are used on acoustic modeling as well as experimental details. It's interesting to note that Apple engineers decides not to use the best model (LSTM) but using a simpler model (DNN) in order to run everything on a device. 

[apple.com](https://machinelearning.apple.com/2017/10/01/hey-siri.html)

## Member's Question

### [Should I be a Software Engineer or an ML Engineer?](https://www.facebook.com/groups/DeepNetGroup/permalink/515513918841495/)

Answer from Arthur: 

The most important factor is where your passion is. Do you like to be an ML guy? Do you want to be a software engineer? Notice that there is a wide spectrum of jobs in the world which is in between ML engineer and software engineer. There're researchers/scientists who are purely about ML. There are software engineers who purely play with code. Then there are architect which you need to know a bit of everything. But it is what do you like to do decide your future.

The second most important factor I would say is reality. If you are starving, you can't fulfill your passion. So there's also no shame to just come up with a practical career and work hard on it.

[facebook.com](https://www.facebook.com/groups/DeepNetGroup/permalink/515513918841495/)

## Paper/Thesis Review

### [Swish: a Self-Gated Activation Function](https://arxiv.org/abs/1710.05941)

Perhaps the most interesting paper last week is the Swish function. Here are some notes: 
- Swish is extraordinarily simple. It's just swish(x) = x \* sigmoid(x).
- Derivative? swish'(x) = swish(x) + sigmoid(x) (1 - swish (x)) Simple calculus.
- Can you tune it? Yes, there is a tunable version which the parameter is trainable. It's call Swish-Beta which is x \* sigmoid( Beta \* x)
- So here's an interesting part of why it is a "self-gating function". So.... if you understand LSTM, essentially it introduced a multiplication sign. e.g. input gate and forget gate, give you are weight of "how much you want to consider the input" and "how much much you want to forget". (http://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- So swish is not too different - there is the activation function but it is weighted by the input itself. Thus the term self-gating. In a nutshell, in plain English, "because we multiply".
- It's all good, but does it work? The experimental results look promising. It works on Cifar-10, Cifar-100. On Imagenet, it beats Inception-v2 and v3 when swish replace ReLU.
- It's worthwhile to point out the latest Inception is in v4. So the imagenet number is not beating stoa even within Google, not to say the best number in Imagenet 2016. But that shouldn't matter, if something consistently improve on some models of Imagenet, it is a very good sign it is working.
- Of course, looking at the activation function. It introduces a multiplication. So it does increase computation when compare with a simple ReLU. And that seems to be the complaint I heard. That's what I have. Enjoy!

[arxiv.org](https://arxiv.org/abs/1710.05941)
