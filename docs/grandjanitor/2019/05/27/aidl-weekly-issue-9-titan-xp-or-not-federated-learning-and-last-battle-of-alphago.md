---
title: "AIDL Weekly Issue 9 - Titan Xp or Not? Federated Learning and Last Battle of AlphaGo(?)"
date: 2019-05-27
---

# AIDL Weekly Issue 9 - Titan Xp or Not? Federated Learning and Last Battle of AlphaGo(?)

# [Issue 9 *April 14th 2017* ](http://aidl.io/issues/9/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we focus on several note-worthy developments of the week: 
- Federated Learning from Google, what is its impact?
- Titan Xp, should you buy it or not?
- AlphaGo vs Ke Jie, is it AlphaGo final battle against humans?
- Hinton's NNML class, is it still relevant or not? Should you take it?

As always, if you like our newsletter, subscribe and forward it to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Video Conferencing That Just Works, So You Can Get Back To Work](https://www.cyclops.io/?utm_source=AIDL-newsletter)

Easy, free video conferencing that works in your browser. No Download. No login. Get up and running in seconds. Comes with productivity apps on top. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Titan-XP](https://www.nvidia.com/en-us/geforce/products/10series/titan-xp/)

The new Titan is here! With a price tag of $1200, Titan Xp isn't too impressive doesn't other than speed improvement (3x). On-board memory is still 12G, slightly ahead of the late 1080 Ti.

Should you buy a Titan Xp? Tim Dettmer would recommend a generally no. Also check out another link from his "Which GPU(s) to Get for Deep Learning?".

[nvidia.com](https://www.nvidia.com/en-us/geforce/products/10series/titan-xp/)

---

### [AlphaGo vs Ke Jie](https://deepmind.com/blog/exploring-mysteries-alphago/)

Go, unlike Chess, has no Elo rating. The closest equivalent is [Rémi Coulom](https://en.wikipedia.org/wiki/R%C3%A9mi_Coulom)'s [unofficial rating](https://www.goratings.org/). Currently Ke Jie is the number 1 on the list. (The Korean Champion, Lee Sedol? No.5.) You can think of Ke Jie as a Gary Kasparov-equivalent of Go. Ke Jie was known for his confidence, balanced style and his several wins versus the Korean Champion. And before his unofficial match with the ["Master"](https://qz.com/877721/the-ai-master-bested-the-worlds-top-go-players-and-then-revealed-itself-as-googles-alphago-in-disguise/) in January, he was also confident that AlphaGo can be beaten. So far, AlphaGo racked up [60 wins, 0 loses](https://qz.com/877721/the-ai-master-bested-the-worlds-top-go-players-and-then-revealed-itself-as-googles-alphago-in-disguise/). That sadly includes 3 wins on Ke Jie.

Ke Jie still claims he has [one last move](https://qz.com/878503/ke-jie-the-worlds-best-go-player-says-he-still-has-one-last-move-to-defeat-google-goog-deepminds-alphago-ai/). Would he be able to stall AlphaGo's advance? Would AlphaGo improve even more after the 60 wins? We will find out in May, "Future of Go Summit".

[deepmind.com](https://deepmind.com/blog/exploring-mysteries-alphago/)

---

### [Canada: The New Hub of A.I.?](https://www.nytimes.com/2017/04/09/technology/canada-artificial-intelligence.html?_r=0)

NYT report on Canada's attempt to reverse her AI brain drain. Modern deep learning has its origin from three famous professors: [Geoff Hinton](http://www.cs.toronto.edu/~hinton/), [Yoshua Bengio](http://www.iro.umontreal.ca/~bengioy/yoshua_en/) and [Yann Lecun](https://en.wikipedia.org/wiki/Yann_LeCun). All of them have Canadian connections. This shows how much Canada has been an influence of deep learning, one of the most impactful technologies today.

Even though it's been a hotbed of academic A.I. activity, Canada has been losing A.I. talent to Silicon Valley, and to a lesser extent, New York or Boston. However, this may be changing in the future.

The NYT article details the [Creative Destruction Lab](https://www.creativedestructionlab.com/) and two of its participants, [Atomwise](http://www.atomwise.com/) and [Deep Genomics](https://www.deepgenomics.com/). With the newly found [Vector Institute](https://www.utoronto.ca/news/toronto-s-vector-institute-officially-launched) and new influx of fundings, we'll see if it stems the outflow.

[nytimes.com](https://www.nytimes.com/2017/04/09/technology/canada-artificial-intelligence.html?_r=0)

## Blog Posts

### [Update on "Which GPU(s) to Get for Deep Learning" by Tim Dettmers](http://timdettmers.com/2017/04/09/which-gpu-for-deep-learning/)

For years, if you want to DIY a deep learning machine, you read Dettmers' post "Which GPU(s) to Get for Deep Learning" which gives the final verdict of which card should buy.

So with 1080Ti and Pascal Tx just released last month, should you toss in $600 more to buy a Pascal Tx? Let's look at few categories from Dettmer's "tl;dr" recommendation: 
- Best GPU overall (by a small margin): Titan Xp
- I have little money: GTX 1060 (6GB)
- I have almost no money: GTX 1050 Ti (4GB)
- I am a competitive computer vision researcher: NVIDIA Titan Xp; do not upgrade from existing Titan X (Pascal or Maxwell)
- I am a researcher: GTX 1080 Ti

We like Dettmer's suggestion. GTX 1080Ti is a fairly unusual card - it is the first GTX card which has more than 8G of RAM. So in a way, GTX 1080Ti makes it hard for customers to buy the Titan series. But then if you do want to do the best computer vision experiment, a Titan X (Pascal) upper is necessary.

Another note here is the new Titan Xp isn't as impressive as one hopes. Dettmer's guide is quite clear: don't replace your Titan X (Pascal) yet with Xp. We also think that's solid advice from a cost-efficiency point of view.

In any case, Dettmer's guide should teach you how to DIY your dream DL machines, check out his post regardless of your goal.

[timdettmers.com](http://timdettmers.com/2017/04/09/which-gpu-for-deep-learning/)

---

### [Federated Learning](https://research.googleblog.com/2017/04/federated-learning-collaborative.html)

What is federated learning? Basically it is a kind of distributed method for model training. First you train models from different devices, then the devices upload updates and the server averages them to become a single model.

From a deep learning point of view, such training requires parallelizing SGD into multiple parts, which is quite hard. So the merit of [Google Research paper](https://arxiv.org/abs/1602.05629) is that they figure you can just use a large batch size on each device. In that case, you can avoid using small-step SGD and use lower bandwidth, which is precious in a federated learning scenario. (There are also techniques to deal with the non-IID-ness of the scenario. But a key insight the researchers found is that averaging behaves surprisingly well.)

Perhaps the more important issue is *privacy*. For example, a new user input could be learned from the model, and it's plausible this new user input could be used to derive info of the user. That is protected by the "Secure Aggregation Protocol" (http://eprint.iacr.org/2017/281).

All-in-all, this is interesting work from Google. Check out the original blog post for more detail.

[googleblog.com](https://research.googleblog.com/2017/04/federated-learning-collaborative.html)

---

### [Unsupervised Sentiment Neuron](https://blog.openai.com/unsupervised-sentiment-neuron/#methodology)

From time to time, simple ideas trump complicated and over-engineered ones. OpenAI's unsupervised sentiment neuron is one of those cases. The idea is very simple, you first train a character language model on a large corpora. In OpenAI's case, it is a [multiplicative LSTM](https://arxiv.org/abs/1609.07959) with x-units. But no matter how complicated the model is, you are essentially just modeling the underlying distribution. Notice that, at this point, all the data is still unlabeled

Now this is the interesting part, with labeled data, you can take the x-units (now dubbed as "unsupervised sentiment neurons" ) and train a linear model out of them. When OpenAI did it, this turns out to be surprisingly effective and beat the best technique on the Stanford Sentiment Treebank task. More importantly, even if they are using 30-100x less label data, they can still match results of other methods. It took a month to train such models, but the result is very impressive.

This result is reminiscent of pre-training of DNN. It also makes you wonder, can we use method other than linear model to train on the unsupervised neurons and get better results? In any case, this piece is thought-provoking. Yet another great piece of work from OpenAI.

[openai.com](https://blog.openai.com/unsupervised-sentiment-neuron/#methodology)

---

### [Review of Hinton's Coursera "Neural Network and Machine Learning"](/grandjanitor/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/)

Prof. Hinton's "Neural Networks and Machine Learning" (NNML) is perhaps the first MOOC on deep learning. In this review, Arthur will discuss whether you should take this course, when you should take it. And more relevant to our audience: given the many courses/classes/tutorials you could find, is NNML still relevant? He will offer some answers in my post.

[thegrandjanitor.com](/grandjanitor/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/)

---

### [Trends in Machine Learning by Andrej Kapathy](https://medium.com/@karpathy/a-peek-at-trends-in-machine-learning-ab8a1085a106)

This is post by Andrej Kapathy, and he looks at various trends of machine learning, including frameworks, models, optimization algorithms etc. Sounds like "Fully Convolutional Encoder Decoder BatchNorm ResNet GAN applied to Style Transfer, optimized with Adam." is not that far off. :)

[medium.com](https://medium.com/@karpathy/a-peek-at-trends-in-machine-learning-ab8a1085a106)

## Open Source

### [DeepMind Sonnet](https://deepmind.com/blog/open-sourcing-sonnet/)

Sonnet is a library written for research purpose within DeepMind. According to the README, part of the reasons why DeepMind released yet another library is to allow more effective weight sharing within the network. That's a fairly interesting technical reason.

Another strength is the use of submodules. As the blog post suggest, promoting submodules would probably mean easier design for large neural networks such as [Differentiable Neural Computer](https://deepmind.com/blog/differentiable-neural-computers/). Indeed, specifying a large network can be tedious task using raw TF.

Perhaps the last important feature of Sonnet is that there will be more future releases. With Deepmind's deep involvement in projects such as AlphaGo, we expect there are more interesting code open in the next year.

[deepmind.com](https://deepmind.com/blog/open-sourcing-sonnet/)

---

[*[image not recovered: twenty_by_nine_extra_large_aed61168-5b9c-4b37-a2c9-14d2ad6b4bd2.jpg]*](http://www.kdnuggets.com/2017/04/10-free-must-read-books-machine-learning-data-science.html) 

### [10 Free and Legal Books for Machine Learning and Data Science](http://www.kdnuggets.com/2017/04/10-free-must-read-books-machine-learning-data-science.html)

We seldom post book-link ass many of them are filled with paid content. This one from KDNuggets is different and all the books are free, meaning it is legal for you to download. We even add this link into our forum's FAQ. 

[kdnuggets.com](http://www.kdnuggets.com/2017/04/10-free-must-read-books-machine-learning-data-science.html)

## Video

[*[image not recovered: twenty_by_nine_extra_large_dd6e78f8-30b8-4357-9b38-b0cceb1e305b.png]*](https://www.youtube.com/watch?v=9reHvktowLY&feature=youtu.be) 

### [Power of CycleGAN](https://www.youtube.com/watch?v=9reHvktowLY&feature=youtu.be)

Wow, check out this image generated by [CycleGAN](https://github.com/junyanz/CycleGAN)! It's certainly impressive for the flawless transfer of all strips. 

Many in the forum pointed out that the horse's eyes is still blurry, and some had tried the package with mixed results, e.g. the processing isn't too smooth at the edge of an object. We are not too surprised - while cycleGAN propose a new loss term, cycle loss, it doesn't quite use any segmentation information. In that way, pixels around the object could easy altered and reduced in spurious change.

We still found the technology fairly impressive - after all, you just need to throw in a bunch of training images, then the algorithm would generate the right texture.

[youtube.com](https://www.youtube.com/watch?v=9reHvktowLY&feature=youtu.be)

---

### [Artificial Intelligence & Deep Learning Office Hour Episode #6](https://www.youtube.com/watch?v=b-mUlfOR6oQ)

We had an awesome office hour session with Slack's [Amir Shevat](https://www.linkedin.com/in/amirshevat)! We discussed where AI fits in the conversational interface and the enterprise, among other things. Appreciate the time!

For those interested in building on Slack, below are the relevant links: [api.slack.com](http://api.slack.com). Check out his article "[Build an interactive Slack app with message menus](https://medium.com/slack-developer-blog/build-an-interactive-slack-app-with-message-menus-1fb2c6298308)" and [his book](http://shop.oreilly.com/product/0636920057741.do).

Also, Amir is going on an EU tour to talk more about Slack developer platform.

Here are the dates:

**London, England**

Daytime Workshops April 24

Daytime Workshops April 25

Messaging Bots London April 25

**Berlin, Germany**

Daytime Workshops April 26

Daytime Workshops April 27

\#BotsBerlin Meetup April 26

**Vienna, Austria**

BotBarCamp April 29–30

**Copenhagen, Denmark**

Meetup at Founders HQ May 1

**Paris, France**

Daytime Workshops May 2

Chatbots Paris Meetup May 2

**Stockholm, Sweden**

StartupGrind with Bear Douglas May 3

**Tel Aviv, Israel**

Basebots Meetup May 3

Rooftop Chat with Aleph May 3

To AI or not to AI: Chat with Amir Shevat May 4

[youtube.com](https://www.youtube.com/watch?v=b-mUlfOR6oQ)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 16,000+ members and host a weekly ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube.
