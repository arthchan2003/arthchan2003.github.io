---
title: "AIDL Weekly Issue #63 - Predicting Winner of World Cup 2018"
date: 2019-07-25
---

# AIDL Weekly Issue #63 - Predicting Winner of World Cup 2018

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 63 *June 16th 2018* ](http://aidl.io/issues/63/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Our issue this week is mostly technical: 
- How to predict the winner of World Cup 2018?
- How to use a pretrained model in text classification?
- How to build a custom face recognition dataset?

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 149,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Yitu $200 M Series C](https://www.chinamoneynetwork.com/2018/06/12/icbc-international-spdb-international-invest-200m-series-c-round-in-chinese-ai-firm-yitu-technology)
- [Memrise $15.5M](https://techcrunch.com/2018/06/11/memrise-raises-15-5m-as-its-ai-based-language-learning-app-passes-35m-users/)
- [Ride OS (formed by Uber alums), raise $9.5 Million](https://www.bloomberg.com/news/articles/2018-06-15/ford-unit-teams-with-startup-developing-waze-for-self-driving-cars)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [Predicting World Cup Using ML](https://www.technologyreview.com/s/611397/machine-learning-predicts-world-cup-winner/)

If you are US-based, probably you don't care about soccer as much as the rest of the world do. In some parts of the planet though, soccer is like a religion. So it's no surprise people are making serious effort on predicting the winner of FIFA 2018.

The paper which is making rounds is "Prediction of the FIFA World Cup 2018 - A random forest approach with an emphasis on estimated team ability parameters" by Groll et al, which use random forest for modeling. Looking deeper into the paper, the author used 16 factors including FIFA ranking and economic metrics of the country as the input variables.

Who is most likely to win? According to the authors: Spain which has 17.8% chance to win. What about German and Brazil? 17.1% and 12.8% respectively. Well well, we will see if these predictions are correct, and whether Spain would be in top-3.

[technologyreview.com](https://www.technologyreview.com/s/611397/machine-learning-predicts-world-cup-winner/)

---

### [Kaggle Data Note: Predict the World Cup 2018 Winner](http://blog.kaggle.com/2018/06/14/data-notes-6-14-2018/)

From Kaggle, isn't this the most important dataset now?

[kaggle.com](http://blog.kaggle.com/2018/06/14/data-notes-6-14-2018/)

---

### [Improving Language Understanding through Unsupervised Learning. ](https://blog.openai.com/language-unsupervised/)

This work, by OpenAI, addresses the low resource problem in NLP, specifically in text classification. The authors asked if we get better performance by fine-tuning a pre-trained unsupervised model. And they found, in several tasks, the fine-tuned models give better results than SOTA. This works is based on previous OpenAI's work on [unsupervised sentiment neuron](https://blog.openai.com/unsupervised-sentiment-neuron/).

OpenAI's approach is not without issues: e.g. while pre-trained model is effective, we need to assume we have a pre-trained model in the first place. But then training one would require large amount of computation. The authors also found that there are still issues of generalizability.

[openai.com](https://blog.openai.com/language-unsupervised/)

---

### [The AI Bubbles and AI Researchers ](http://hunch.net/?p=9604328)

When there is such irrational exuberance in AI, how should you see yourself as a researcher or perhaps even a developer?

Generally we believe that the so called "AI hype" itself is more fluffy talk. Though recently there are indeed more indications that companies are irrationally exuberant on the prospect of AI. e.g. There are so many self-styled experts. And you see AI influencers are treated as celebrities. I think these are unhealthy phenomena as well.

Many articles only try to pour cold water on AI, and some of their analyses are just plain silly. The authors of the OP though as researchers, are just setting themselves in the right footing, hoping that they can continue to research or do whatever they like to do. So I don't see anything wrong.

[hunch.net](http://hunch.net/?p=9604328)

---

### [How to build a custom face recognition data set?](https://www.pyimagesearch.com/2018/06/11/how-to-build-a-custom-face-recognition-dataset/)

Yet another great article by Adrian Rosebrock. This time on how to build a custom face recognition data set.

[pyimagesearch.com](https://www.pyimagesearch.com/2018/06/11/how-to-build-a-custom-face-recognition-dataset/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 149,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
