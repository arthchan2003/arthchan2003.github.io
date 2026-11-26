---
title: "AIDL Weekly Issue 29 - A Sobering Look at IBM Watson, Google in Beijing and Amazon in Barcelona,"
date: 2019-07-02
---

# AIDL Weekly Issue 29 - A Sobering Look at IBM Watson, Google in Beijing and Amazon in Barcelona,

# [Issue 29 *September 8th 2017* ](http://aidl.io/issues/29/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Summer is gone, and AI/DL development is heating up again. You heard that Google is building a new team in Beijing, and Amazon is having a new R&D center in Barcelona? The internationalization of A.I., partly due to talent scarcity, will continue to be a theme. 

In other news, StatNews investigates whether IBM Watson is fulfilling is promise in the domain of cancer care. Watson's challenges in healthcare do reflect in some ways the same challenges in the more general deep learning community. So this article should be interesting for you all.

We also cover interesting technical topics such as Uber's Michaelangelo and PassGAN in our blog and paper sections. So check it out!

---

As always, if you like our newsletter, feel free to subscribe/forward it to your colleagues!

Artificial Intelligence and Deep Learning Weekly

---

*[image not recovered: twenty_by_nine_extra_large_ba319109-7a0f-4fe9-b530-a36f63a47c19.jpg]*

### Meme of The Week

Courtesy from Nikolay Pavlov from Ukrainian AI Community. 

(Yeah.... We know that there should be activation functions. And all the weight should be indexed in terms of layers. But hey, it's still funny.)

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [A Sobering Look at IBM Watson on Cancer Care](https://www.statnews.com/2017/09/05/watson-ibm-cancer/)

Statnews' Carey Ross and Ike Swetlit investigated how well IBM Watson actually works in cancer care. It is a sobering look at the challenges Watson encountered. For eample, how do you deal with frequent updates of medical literature and standard? How do you address the "do no harm" concerns of doctors? How do you balance privacy and data? This StatNews piece explore each of these issues. 

The investigation is thorough. One of the key areas the authors peeled back is that currently Watson doesn't seem to provide any scientific evaluation of how well Watson works: 

> The actual capabilities of Watson for Oncology are not well-understood by the public, and even by some of the hospitals that use it. It’s taken nearly six years of painstaking work by data engineers and doctors to train Watson in just seven types of cancer, and keep the system updated with the latest knowledge.

Another question posed by the authors is how well Watson's advice would be valid outside America: 

> In Denmark, oncologists at one hospital said they have dropped the project altogether after finding that local doctors agreed with Watson in only about 33 percent of cases.

We think the conclusion of the authors were mild, but valid: 

> But the outlook for Watson for Oncology is challenging, say those who have worked closest with it. Kris, the lead trainer at Memorial Sloan Kettering, said the system has the potential to improve care and ensure more patients get expert treatment. But like a medical student, Watson is just learning to perform in the real world.

Whereas if you recall the Gizmodo's [piece](http://gizmodo.com/why-everyone-is-hating-on-watson-including-the-people-w-1797510888) back in Aug 11, 2017, a quote from Claudia Perlich, a ex-data scientist from IBM: 

> “The reality however is what Watson as a commercial product represents is very different, even from a technology perspective, from Watson who won Jeopardy!”

Our take: IBM's problem could be another example where technology could not yet quite catch up with the moon-shoot promise from the marketing department. IBM still has many talented AI researchers. Also, perhaps more importantly, what IBM is encountering is what other deep learning researchers may increasingly encounter - beware of the hype.

[statnews.com](https://www.statnews.com/2017/09/05/watson-ibm-cancer/)

---

### [Google Build an ML team in Beijing](http://www.scmp.com/tech/enterprises/article/2109719/google-looking-build-its-own-team-artificial-intelligence)

South China Morning Post (SCMP) as well as Financial Times, reported that Google is looking to build a new ML team in Beijing. If you are familiar with the relationship between Google and China, this is interesting news. China's censorship policy doesn't go with Google well, and it was known that back in 2010, [Google decided to quit the China market](https://www.forbes.com/forbes/welcome/?toURL=https://www.forbes.com/2010/01/15/baidu-china-search-intelligent-technology-google.html), and only at 2016, the company decides to reenter the [market](https://www.theatlantic.com/technology/archive/2016/01/why-google-quit-china-and-why-its-heading-back/424482/). Initially the deal was based on Android but now it seems like Google start to further developed in A.I. activity in China as well. 

So what make Beijing an ideal site? The political seat of power, tech startup ecosystem and both Beijing University and Tsinghua are all located there.

Specific to A.I., perhaps the more important reason here is that several companies such as MS already heavily invest in A.I. talents in Beijing. e.g. As you know MSR China is the one that came up with the innovative techniques such as Resnet. Google cannot afford not to have a presence in the ML ecosystem in China.

[scmp.com](http://www.scmp.com/tech/enterprises/article/2109719/google-looking-build-its-own-team-artificial-intelligence)

---

### [Amazon New Research Center in Barcelona](https://venturebeat.com/2017/09/07/amazon-to-open-machine-learning-rd-hub-in-barcelona/)

Another expansion news from tech giant, Amazon is planning to hire more than 100 engineers and scientists in the Barcelona engineering center. The goal of the center is not surprising - part of it is to allow Amazon to keep tap of talents in local universities, part of it is to develop non-English version of products such as Alexa. 

[venturebeat.com](https://venturebeat.com/2017/09/07/amazon-to-open-machine-learning-rd-hub-in-barcelona/)

---

### [U.S. House passed a Bill to test 100k SDC](https://www.recode.net/2017/9/6/16259306/house-senate-self-driving-driverless-cars-autonomous)

This is a quiet yet significant piece of news. U.S. House just passed a bi-partisan bill, or SELF-DRIVE Act, which allow exemptions of autos/tech companies to get exemptions from federal regulations. As such, close to 100k autonomous vehicles can be tested on the road. The bill is not yet a law, and it still has to go through U.S. Senate. 

[recode.net](https://www.recode.net/2017/9/6/16259306/house-senate-self-driving-driverless-cars-autonomous)

## Blog Posts

### [How I failed to replicate an $86 million project in 1 line of code](https://medium.com/@ryanfb/how-i-failed-to-replicate-an-86-million-project-in-1-line-of-code-615048a1f9d0)

This is a response to the article [How I replicated an $86 million project in 57 lines of code](https://medium.freecodecamp.org/how-i-replicated-an-86-million-project-in-57-lines-of-code-277031330ee9) in which the author claims that he comes up with a 57-line python system which can replace an 86 million system. 

While the intention was good, we found that "How I replicated an $86 million project in 57 lines of code" is an exaggerating title. That's why Ryan Baumann's response is called for. Also, many members at AIDL points out that the original article is meant to be a proof-of-concept (POC), while we agreed, but a more modest title could be "How I create a POC with 57 lines of code".

[medium.com](https://medium.com/@ryanfb/how-i-failed-to-replicate-an-86-million-project-in-1-line-of-code-615048a1f9d0)

---

### [Uber's ML Platform: Michelangelo](https://eng.uber.com/michelangelo/)

Despite the many negative news reporting of Uber of late, it still remains one of the most technically interesting companies in the planet. We were introduced to Michaelangelo, the company internal ML platform. The system sounds incredibly cool - it can control data and flow of training. More importantly it allows experimenters to share their workflow. 

[uber.com](https://eng.uber.com/michelangelo/)

## Open Source

### [Tutorial on Deep Generative Models by Shakir Mohamed and Danilo Rezende](http://www.shakirm.com/slides/DeepGenModelsTutorial.pdf)

This tutorial published by DeepMind authors, Shakir Mohamed and Danilo Rezende, go through applications of generative models and its several important classes. 

[shakirm.com](http://www.shakirm.com/slides/DeepGenModelsTutorial.pdf)

---

### [ONNX](https://research.fb.com/facebook-and-microsoft-introduce-new-open-ecosystem-for-interchangeable-ai-frameworks/)

In the world filled with different deep learning toolkits, FB and MSFT announcement on Open Neural Network Exchange format is surprising. If you ever use multiple frameworks to train deep models, you know that one of the headaches is that models are not necessarily compatible with one another. And you can imagine different companies don't always have the incentives to share the models with one another. Here comes ONNX, which can supposedly run in both Facebook's Caffe2 and PyTorch, as well as MS' cognitive toolkit. It is a strong plus for users to use PyTorch/Cognitive Toolkit. 

It remains to see if Google/TF would follow the suit. Generally, we love this piece of news, because open format is the key for efficient development.

[fb.com](https://research.fb.com/facebook-and-microsoft-introduce-new-open-ecosystem-for-interchangeable-ai-frameworks/)

## Paper/Thesis Review

### [PassGAN](https://arxiv.org/abs/1709.00440)

No, no, no. This is not exactly a password guesser. This is a password list generator. But the thinking is very smart - can we just train a ML model from a large open password lists and use it to generate passwords? That's PassGAN, the training method is based on I. Gulrajani's IWGAN. 

[arxiv.org](https://arxiv.org/abs/1709.00440)

---

### [EuroSAT](https://arxiv.org/abs/1709.00029)

This is a mid-size database for land use classification using satellite image. Just judging the number (98.45%), it seems to be slightly harder than MNIST, but a bit easier than CIFAR-10, which can make it a good data set to test for papers. 

[arxiv.org](https://arxiv.org/abs/1709.00029)
