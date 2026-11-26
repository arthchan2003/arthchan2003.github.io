---
title: "AIDL Weekly #64 - The Medical Brain"
date: 2019-07-25
---

# AIDL Weekly #64 - The Medical Brain

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 64 *June 24th 2018* ](http://aidl.io/issues/64/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We take a closer look of Google Medical Brain this week. In particular, we look at their recent paper on predicting in-hospital mortality (and more) based on EHR.

As always, if you like our newsletter, feel free to subscribe and forward it to your colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 150,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. Join our community for real-time discussions with this iOS app here: https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly

## News

### [A Smarter Path to Artificial Intelligence?](https://www.nytimes.com/2018/06/20/technology/deep-learning-artificial-intelligence.html)

Here is an NYT article on whether deep learning is the only way of AI. If you are members of AIDL, perhaps you already see this kinds of articles. But this piece has a special twist: Can startups create solutions that can use "Small Data"? And indeed, couple of companies in the article do demonstrate some capability of using only few samples in training.

To give a perspective though, while many has been criticizing deep learning for its demand of large amount of data. There are vibrant research in deep learning focusing on using only small amount of data too. e.g. transfer learning is a way to pivot a pre-trained model to a new training set, and it is a prominent technique in image classification.

Of course, we are not saying the debate is meaningless. e.g. Kyndi and Vicarious, mentioned in the article , are also seeking for *interpretability* of an ML algorithm as well. And deep learning is [notoriously bad in explaining itself](https://www.quantamagazine.org/new-theory-cracks-open-the-black-box-of-deep-learning-20170921/).

[nytimes.com](https://www.nytimes.com/2018/06/20/technology/deep-learning-artificial-intelligence.html)

---

### [Bons.ai is acquired by MS](https://www.geekwire.com/2018/microsoft-acquire-machine-learning-training-startup-bonsai-bolstering-ai-efforts/)

Mark Hammond was [our guest in AIDL office hour](https://www.youtube.com/watch?utm_campaign=Artificial%2BIntelligence%2Band%2BDeep%2BLearning%2BWeekly&utm_medium=web&utm_source=Artificial_Intelligence_and_Deep_Learning_Weekly_18&v=-0hkSq_x-AY) and a panel of AIDL's "Attack of AI Startup". His company, Bons.ai, is now acquired by Microsoft. Congratulation, Mark!

[geekwire.com](https://www.geekwire.com/2018/microsoft-acquire-machine-learning-training-startup-bonsai-bolstering-ai-efforts/)

---

### Deals

- [BetterDoctor is acquired](https://www.axios.com/exclusive-betterdoctor-being-acquired-3c585ec5-a2c2-48a3-825b-0b75b81f92fd.html)
- [Tessian $13million round](https://venturebeat.com/2018/06/17/tessian-raises-13-million-to-use-machine-learning-for-securing-enterprise-email/)
- [Agari $40M round from Goldman Sachs](http://fortune.com/2018/06/21/goldman-sachs-agari/)
- [Paypal to buy Simility for $120M](https://techcrunch.com/2018/06/21/paypal-to-buy-simility-a-specialist-in-ai-based-fraud-and-risk-management-for-120m/)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [FB DensePose](https://research.fb.com/facebook-open-sources-densepose/)

Facebook is open sourcing DensePose, a database which map 2D RGB image to 3D surface models, which you can imagine, is a useful resource if you want to detect human action or posture from image.

[fb.com](https://research.fb.com/facebook-open-sources-densepose/)

## Paper/Thesis Review

### [The Medical Brain - Deep Learning Methods of EHR Analysis ](https://www.nature.com/articles/s41746-018-0029-1)

Recently a Bloomberg article mentioned [Google Medical Brain](https://www.bloomberg.com/news/articles/2018-06-18/google-is-training-machines-to-predict-when-a-patient-will-die)'s latest research on predicting mortality. And as you can imagine, the Bloomberg's piece stress on how advanced Google in terms of EHR analysis. The author of the article also questioned whether Google's research has violated patienti privacy, etcetra and so forth. That's what you expect from Bloomberg, which is more a financial news outlet.

Of course our concern is a little bit different at AIDL, we want to know more what Google is actually doing. And is it really a scientific advance? That we could only judge by looking at the original papers. So the paper in question is ["Scalable and accurate deep learning with electronic health records"](https://www.nature.com/articles/s41746-018-0029-1). If this is the first time you read a Nature paper, remember that most information about model architecture and data processing can only found in the paper's supplementary notes (as in ["Supplementary Material"](https://static-content.springer.com/esm/art%3A10.1038%2Fs41746-018-0029-1/MediaObjects/41746_2018_29_MOESM1_ESM.pdf) for this paper). Both the paper and the note appear to be in Creative Common, so we in the public can take a closer look.

The first question to ask here is what Google is modeling - what they are building is a predictor of "medical events", which is for example when would a patient die in the hospital, or "in-hospital mortality", or whether a patient will stay longer in a hospital, i.e. "prolonged length of stay". This prediction is, of course, very important for both the hospital and patients. But of course, Bloomberg has focused on just the in-hospital mortality prediction.

What is the input? The data you get is based on electronic health record (EHR). So you can think of it as a collection of all health information of a patient. This can be medication? Vital signs such as blood pressure? How much the patient paid their bills? And it can also include hand-written notes from doctors and care professional. So you may think what Google built is an EHR-based predictor. The model itself is based on deep neural network, in particular, recurrent neural network. This makes sense because your EHR reflect a time-based records that each day of the record can be seen as one point in a time series.

Is this thinking new? Not really, as the authors note, there was a body of literature on similar problem. For example, they note that there are already existing method which use linear models for prediction. For deep learning-based method, they quote this work titled ["Deep EHR: A Survey of Recent Advances in Deep Learning Techniques for Electronic Health Record (EHR) Analysis"](https://arxiv.org/pdf/1706.03446.pdf) for readers, which we also find it rather readable.

But did Medical Brain do something new? Absolutely. For starter, traditional approaches requires experts to first create an abstract representation. This process is usually called data harmonization. But Google's approach can work directly with the raw record such as free-text notes or manuscript. This in our view is the major reason Google can beat the current best results - the team was able to account for more data which was previously hidden. This approach yields very impressive results: area under curve (AUC) based on deep learning is 0.95, improved from 0.85 based on logistic regression which was the previous best approach.

Are there any problems with the method? I think the author said it the best: 

> Our study also has important limitations. First, it is a retrospective study, with all of the usual limitations. Second, although it is widely believed that accurate predictions can be used to improve care, this is not a foregone conclusion and prospective trials are needed to demonstrate this. Third, a necessary implication of personalized predictions is that they leverage many small data points specific to a particular EHR rather than a handful of common variables. . Future research is needed to determine how models trained at one site can be best applied to another site, which would be especially useful for sites with limited historical data for training.

Translation: 1. It is studying the past data, so we don't know if it will work for future data. i.e. standard disclaimer for any prediction system. 2. Just that you can predict better, it doesn't means you can cure better. 3. This third point is more complicated. With the new proposed method, we no longer just able to predict with few variables. We will then rely on the EHR of a hospital. Would data in one site work in another?

One more note: since deep learning requires large amount of data, the method also assume availability of such database. And gathering such data seems to be difficult. Just talking about this work, we are really talk about 200k samples. As you can imagine, the authors can only use de-anonymized data.

Overall speaking though, the Google's authors seem to follow the right methodology to conduct the research. Data as we said, is de-anonymized. They also have doctors as advisors of the team. They are probably learning a good lesson from their colleagues in DeepMind, another subsidiary of Alphabet. (See Issue 20 for [our coverage on DeepMind and patient privacy](http://aidl.io/issues/63#start). )

All-in-all, this is interesting and legit result.... oh .... we haven't talked about the modeling part. In a nutshell, the modeling is fun but not unimaginable - entries have embedding, model uses BLSTM with attention in time. But then we just point you to the [Supplementary Notes of the paper](https://static-content.springer.com/esm/art%3A10.1038%2Fs41746-018-0029-1/MediaObjects/41746_2018_29_MOESM1_ESM.pdf), you will find all the details.

[nature.com](https://www.nature.com/articles/s41746-018-0029-1)

## Humor

### [Activation Functions](https://www.facebook.com/faiz.cmg/posts/10156451790493684)

We bet you remember all activation functions from now on. :)

[facebook.com](https://www.facebook.com/faiz.cmg/posts/10156451790493684)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 150,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. **Join our community for real-time discussions with this iOS app here:** https://itunes.apple.com/us/app/expertify/id969850760

Artificial Intelligence and Deep Learning Weekly
