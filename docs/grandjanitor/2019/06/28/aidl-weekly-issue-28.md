---
title: "AIDL Weekly Issue 28: MyriadX, ChainerCV and DLSS 2017 Videos"
date: 2019-06-28
---

# AIDL Weekly Issue 28: MyriadX, ChainerCV and DLSS 2017 Videos

# [Issue 28 *September 1st 2017* ](http://aidl.io/issues/28/index.html#start)

## Editorial

*[image not recovered: original_ratio_extra_large_d68693c3-82b6-48cf-b49a-14fed4635ae0.jpg]*

### Thoughts From Your Humble Curators

It's the final week of August, and we are lighter on A.I. news. But if you pay attention, you may also hear the stories like Intel MyriadX, partnership between Microsoft and Amazon's voice assistants. We also learn the exodus of Apple's engineers to Zoox. 

There are also many exciting developments in open source, such as ChainerCV, which re-implements several object detection algorithm and promises simpler training. Videos from DLSS 2017 are also released. Just from the titles, they look very entertaining. Check them out.

Finally, as pointed out by courtesy of [David Ha](https://www.linkedin.com/in/david-ha-168a012/), a Google Brain resident, in our [FB group](https://www.facebook.com/groups/DeepNetGroup/), you know A.I. is hot when even Yves Saint Laurent features a Stanford A.I. researcher in its perfume billboard ad (photo above).

Hey, A.I. guys need to smell good too.

---

As always, if you like our newsletter, remember to subscribe and forward it your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Intel Myriad-X](https://newsroom.intel.com/editorials/introducing-myriad-x-unleashing-ai-at-the-edge/?utm_content=buffere3057&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer)

Intel comes with a new chip, Myriad-X. We are not too surprised because Movidius, which Intel acquired in 2016 has perfect capability to create such chip. But we are still happy to see the power of the Myriad-X which not only accelerates deep learning, but also has the capability to speed up vision-related functionality such as optical flows.

The original Intel's coverage has more marketing terms such as visual processing unit (VPU) or visual intelligence. In terms of applications, we wonder if Myriad-X can compete in key market such as SDC, where Nvidia is dominant in its nascent stage and establish many partnership with autos.

[intel.com](https://newsroom.intel.com/editorials/introducing-myriad-x-unleashing-ai-at-the-edge/?utm_content=buffere3057&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer)

---

### [Amazon and Microsoft agree their voice assistants will talk](https://techcrunch.com/2017/08/30/amazon-and-microsoft-agree-their-voice-assistants-will-talk-to-each-other/?ncid=rss&utm_source=tctwreshare&utm_medium=feed&utm_campaign=Feed%3A+Techcrunch+%28TechCrunch%29&sr_share=twitter)

TC's [Natasha Lomas](https://techcrunch.com/author/natasha-lomas/) sum up this new deal between Amazon and Microsoft well: 

> Those betting big on AI making voice the dominant user interface of the future are not betting so big as to believe their respective artificially intelligent voice assistants will be the sole vocal oracle that Internet users want or need.

This is an interesting alliance between Microsoft and Amazon. We wonder how much of this is driven by competitive pressure from Google. We also wonder if this will last beyond what might be an experiment. Amazon and Microsoft compete heavily on the cloud side and Amazon is encroaching more on Microsoft's application software stack on the enterprise collaboration side with recent product releases.

That said, the idea that one bot assistant platform could be the end-all-and-be-all for a consumer isn't exactly a foregone conclusion. If anything, we believe in a more heterogenous vision where different bots could interact with each other and each platform and bot could specialize (each one becoming essentially loosely coupled micro-services). We hope this alliance could potentially form an archetype of how that would work.

[techcrunch.com](https://techcrunch.com/2017/08/30/amazon-and-microsoft-agree-their-voice-assistants-will-talk-to-each-other/?ncid=rss&utm_source=tctwreshare&utm_medium=feed&utm_campaign=Feed%3A+Techcrunch+%28TechCrunch%29&sr_share=twitter)

---

### [Apple Auto Engineers Joining Startup Zoox](https://www.bloomberg.com/news/articles/2017-08-30/group-of-17-apple-auto-engineers-is-said-to-join-startup-zoox)

It's not exactly news that Apple is scaling back its SDC development. We heard it from this [NYT post](https://www.nytimes.com/2017/08/22/technology/apple-self-driving-car.html?mcubz=0) also from [Slate](http://www.slate.com/articles/technology/technology/2017/08/apple_s_future_isn_t_a_self_driving_car_it_s_siri.html). But then a high-profile exodus of Apple engineers is still a rather unusual event.

What is clear to us : many people think that it is the difficulty of development SDC that trips Apple, the truth seems to be that AI development within Apple is just slower than other major competitors such as Google and Facebook.

[bloomberg.com](https://www.bloomberg.com/news/articles/2017-08-30/group-of-17-apple-auto-engineers-is-said-to-join-startup-zoox)

## Blog Posts

### [Quick Impression on Heroes of Deep Learning - Interview with Prof. Yoshua Bengio](/grandjanitor/2017/08/21/quick-impression-on-deeplearning-ai-after-finishing-coursework/?fref=gc)

Here is another impression by Arthur, on Heroes of Deep Learning. This time is Prof. Ng. Interview with Prof. Yoshua Bengio.

[thegrandjanitor.com](/grandjanitor/2017/08/21/quick-impression-on-deeplearning-ai-after-finishing-coursework/?fref=gc)

---

### [DeepRLHacks](https://github.com/williamFalcon/DeepRLHacks)

Written by William Falcon, a nice set of notes extracted from the talk by John Schulman titled "The Nuts and Bolts of Deep RL Research".

[github.com](https://github.com/williamFalcon/DeepRLHacks)

## Open Source

### [ChainerCV](https://arxiv.org/abs/1708.08169v1)

What caught our eyes in ChainerCV is its reimplementation of certain object detection algorithms such as Faster R-CNN and SSD. As well as Segnet, this is incredibly useful because all these well-known algorithms are there, but coming up an implementation is tough. More importantly, ChainerCV provides "reference code and tools to train models, which is guaranteed to perform on par with the published results". This part is also important because repeating published results is not easy.

[arxiv.org](https://arxiv.org/abs/1708.08169v1)

---

### [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist/blob/master/README.md)

Here is a new dataset Fashion-MNIST, which is meant to replace MNIST. In fact, it was a while people are voicing to move away from MNIST - indeed when a benchmark can reach the 99.7%. And Kagglers can game it so much that all of them seem to be able to get close to perfect results, it's really hard to keep using it as a benchmark. Fashion-MNIST seems to have fairly good popularity, see [here](https://github.com/hwalsuklee/tensorflow-generative-model-collections). You can also find the original paper at [here](https://arxiv.org/abs/1708.07747v1).

[github.com](https://github.com/zalandoresearch/fashion-mnist/blob/master/README.md)

---

### [Game Of Throne Book Generator](https://github.com/zackthoutt/got-book-6)

Enough said.

[github.com](https://github.com/zackthoutt/got-book-6)

## Video

### [DLSS 2017 Videos](http://videolectures.net/deeplearning2017_montreal/)

Finally, video lectures of deep learning summer school 2017 are finally there. Several topics such as "Theoretical Neuroscience and Deep Learning Theory" and "Deep Learning in the Brain" look incredibly interesting.

[videolectures.net](http://videolectures.net/deeplearning2017_montreal/)

## Paper/Thesis Review

### [Interpretation of Mammogram and Chest Radiograph Reports using Deep Neural Networks - Preliminary Results](https://arxiv.org/abs/1708.09254)

We all heard by now deep learning is getting into healthcare. So here is a paper from U. of Toronto, which gives preliminary results on using deep learning to interpret mamograms and chess radiograph reports. The study, as titled, is preliminary, because it is still at the stage of comparing against good old AI techniques such as random forrest and SVM. But then there are several interesting architectural choices in the work which worth your time to take a look. e.g. the use of bi-CNN instead of just CNN.

[arxiv.org](https://arxiv.org/abs/1708.09254)

---

### [Towards an Automatic Turing Test: Learning to Evaluate Dialogue Responses](https://arxiv.org/abs/1708.07149v1)

In this paper by the MILA group, with Yoshua Bengio as the last author, proposed a rather intriguing idea to evaluate dialogue system. First off, some context, usually a dialogue system, deep learning or not, is evaluated using evaluation techniques for statistical machine translation (SMT) such as BLEU or ROUGE. In a nutshell, both of these techniques require human references and correctness of the response will cross-check with the reference. So if there are more words from the reference in the response, generally you get a higher score.

But then we know that dialogue system is not exactly machine translation. Aren't there many ways just to come up with the same response in a dialogue? Like "Great", "Good", "Fine" pretty much are responses for the question "How are you?" But what if the references only have just "Great" and "Good"? That's the problem of what the authors called "word overlap" metric. Indeed if the word doesn't appear in the reference, even if your response make sense, you can't get high score.

So instead of doing a whole word comparison, the author think "can't we just compare in the embedded word space"? That's the idea of word embedding. And the intriguing part about the paper is that it posed dialogue evaluation as measuring distance in this embedded word space. The authors use HRED, which they found a good representation of the reference dialogue.

That results in a rather powerful method. Not only it shows a high correlation with human scores. Also, new response can be more easily evaluated because the comparison happens in the semantic space.

We think this is a highly interesting paper of the week. So check it out!

[arxiv.org](https://arxiv.org/abs/1708.07149v1)
