---
title: "AIDL Weekly #22 - Apple New ML Blog, Elon Musk The Alarmist, and Hassabis' View on AI+Neuroscience"
date: 2019-06-22
---

# AIDL Weekly #22 - Apple New ML Blog, Elon Musk The Alarmist, and Hassabis' View on AI+Neuroscience

# [Issue 22 *July 22nd 2017* ](http://aidl.io/issues/22/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

What a week! Apple just started a new machine learning blog; Audi is going to sell the first self-driving car with L3 autonomy; Elon Musk is telling us (again) that AI is an imminent danger. Would Apple's new blog clash with its secrecy culture? How real is Audi's L3 Autonomy? Should we care about Musk's alarmist view? We will find out more in this issue. We also cover results from the last Imagenet, Verge's interview with Hassabis, François Chollet's view on deep learning and more.

Oh! Did we mention [AIDL](https://www.facebook.com/groups/DeepNetGroup/) just hit [30000 members](https://www.facebook.com/groups/DeepNetGroup/search/?query=30000)?

---

As always, if you like our newsletter, subscribe and forward it to your friends/colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Apple Machine Learning Blog](https://machinelearning.apple.com/)

Apple starts a new ML blog! It is surprising because Apple is known for its defense-level of secrecy. We just couldn't help to feel.... "Ah, Apple really wants to get into the A.I. bandwagon."

But the hints of secrecy is still there. For example, whereas Google is very open on core technologies such as speech recognition or machine translation, Apple chose research subjects such as GAN-based synthetic images. In that way, nothing relevant to its core IP would be disclosed.

Looking at the technical content, which is mostly on GAN and how to use it well. No surprise that Apple has its own captain of deep learning like [Soumith Chintala](https://research.fb.com/people/chintala-soumith/). But who is he/she? No one knows! Once again, it is Apple's secrecy at work - all the posts are written by "Apple engineers". In that way, Apple leave its competitors no way to poach any of its very competent employees.

All-in-all, we learn that Apple is taking steps on A.I. and deep learning, but we couldn't help to wonder - In the future, would Apple's culture of secrecy works well with the current more open culture of AI/DL? Would this clash impede AI development within Apple?

[apple.com](https://machinelearning.apple.com/)

---

### [The Last Imagenet Results](http://image-net.org/challenges/LSVRC/2017/results)

Imagenet 2017 results came out last week. In terms of classification, it went from [2\.94% last year](ILSVRC2016%20-%20ImageNet) to 2.25% this year. Talking about stars in last two years of Imagenet, we have to talk about teams from China. e.g. The winner this year is a team from Beijing's [Momenta.ai](https://www.momenta.ai/) and a postdoc researcher from U. Oxford. While we don't see the dramatic improvement back in the first few Imagenets, the improvement is still fairly impressive (\*).

At first we thought it is just another ensemble type of work. Yet the Momenta.ai+Oxford team did design a new learning block called "squeeze-and-excite", they also improve the GPU memory pipeline. The team also promise to release a report later on.

It's unfortunate that this is the last Imagenet, and as we know major sites haven't participate since last year. But we are always grateful with the pioneering effort of collection of the database as it has resulted in many breakthroughs in deep learning and computer vision.

Footnote: Normally, we measure the *relative improvement* when working on a task. So with 0.75% absolute improvement and we start from 2.94%, you can think the improvement is ~25%.

[image-net.org](http://image-net.org/challenges/LSVRC/2017/results)

---

### [World's First Self-Driving Car with L3 Autonomy](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/the-audi-a8-the-worlds-first-production-car-to-achieve-level-3-autonomy)

For a long time, SDC we know are at L2 autonomy, that is so-called "hands-off", which is the driver can take their hands off the wheel, but only monitor and engage in driving if necessary. As we know, Google was more the champion in L2 - it only requires [engagement for every 5000 miles](https://www.recode.net/2017/3/16/14938116/uber-travis-kalanick-self-driving-internal-metrics-slow-progress?utm_campaign=Artificial%2BIntelligence%2Band%2BDeep%2BLearning%2BWeekly&utm_medium=web&utm_source=Artificial_Intelligence_and_Deep_Learning_Weekly_6). (Uber? Every Mile.) But L2 was more known to be the status quo.

Then Audi comes in and claim that it has L3 on its Cardiallac CT3, that is "eyes-off" which allows users to take their eyes off and only require to attend driving in special limited time. More surprising here is that Audi is a large auto, and it has the reputation of strong quality control.

One thing for sure, Germany' autos companies are [among the first](https://en.wikipedia.org/wiki/Autonomous_car#History) which researched on SDC. Of course, it was much more popularized as illuminaries such as [Prof. Sebastian Thrun](http://robots.stanford.edu/) has competed in [DARPA Grand Challenge](https://en.wikipedia.org/wiki/DARPA_Grand_Challenge). And eventually brought SDC technology to many research institutions of the States. So we shouldn't feel too surprised that Audi has also researched on SDC, and apparently it is for sale now.

CT3 costs 98k euros, and it's certainly for the die-hard fan of SDC, it will first be on-sale in selected are in Europe.

[ieee.org](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/the-audi-a8-the-worlds-first-production-car-to-achieve-level-3-autonomy)

---

### [DeepMind's Founder on AI and Neuroscience](https://www.theverge.com/2017/7/19/15998610/ai-neuroscience-machine-learning-deepmind-demis-hassabis-interview)

Here is an interview from Verge with DeepMind Founder David Hassabis on his views about the current separation of two fields: artificial intelligence and neuroscience. Indeed, while neuroscience class these days would still concern on how computation can emerge from human biology, AI nowadays usually focus on practical applications. Should it be that way? We share Hassabis' view - it shouldn't be. There are many directions of AI research which can be inspired by neuroscience. And modern AI techniques which process large sets of data, can also shed light on unsolved problems in neuroscience. We can see much of these fusions in both our main FB group [AIDL](https://www.facebook.com/groups/DeepNetGroup/) and our satellite group [Computational Neuroscience and Neurobiology](https://www.facebook.com/groups/cnagi/).

Hassabis's paper was published in the prestigious Cell. Here is the [link](http://www.cell.com/neuron/fulltext/S0896-6273%2817%2930509-3?_returnURL=http%3A%2F%2Flinkinghub.elsevier.com%2Fretrieve%2Fpii%2FS0896627317305093%3Fshowall%3Dtrue).

[theverge.com](https://www.theverge.com/2017/7/19/15998610/ai-neuroscience-machine-learning-deepmind-demis-hassabis-interview)

## Blog Posts

### [iRobots Founder on Musk ](https://techcrunch.com/2017/07/19/this-famous-roboticist-doesnt-think-elon-musk-understands-ai/)

This is TC's interview with Rodney Brooks, the famed researcher who start MIT’s Computer Science and Artificial Intelligence Lab and iRobots. By itself, it's an interesting interview. But perhaps the part which deserve your attention is how Brooks look at Elon's warning on AI's purported dangers.

Let's go back - earlier this week, Musk warned of the [imminent danger of AI](https://www.theverge.com/2017/7/17/15980954/elon-musk-ai-regulation-existential-threat), and was widely reported by major outlets. In fact, there are also state-level discussion on how to properly regulate A.I.

Our view is not too different from Rodney. Let's quote him: 

> So you’re going to regulate now. If you’re going to have a regulation now, either it applies to something and changes something in the world, or it doesn’t apply to anything. If it doesn’t apply to anything, what the hell do you have the regulation for? Tell me, what behavior do you want to change, Elon? By the way, let’s talk about regulation on self-driving Teslas, because that’s a real issue.

[techcrunch.com](https://techcrunch.com/2017/07/19/this-famous-roboticist-doesnt-think-elon-musk-understands-ai/)

---

### [Google Facets](https://research.googleblog.com/2017/07/facets-open-source-visualization-tool.html?m=1)

Here is a new tools published by Google which can visualizes dataset. It's quite versatile - you can use it on categorical data such as UCI Census dataset, as well as image data set such as CIFAR-10.

[googleblog.com](https://research.googleblog.com/2017/07/facets-open-source-visualization-tool.html?m=1)

---

### [The Limitations and The Future of Deep Learning. ](https://blog.keras.io/the-limitations-of-deep-learning.html)

Here are two articles written by [François Chollet](https://twitter.com/fchollet), with Keras fame, on what's the [limitation](https://blog.keras.io/the-limitations-of-deep-learning.html) and the [future] of deep learning. As an important captain of the deep learning industry, his words deserve your time. We see many hypes on deep learning lately. Many beginners just see deep learning as the hot new thing, and they all expected career opportunities from the skill sets. Yet real-life problem requires extensive knowledge in other fields in machine learning. So Chollet's essay reminds us such ignorance is danger.

He also gives us an outlook of the possible future research directions on DL and other ideas such as program synthesis and life long learning.

[keras.io](https://blog.keras.io/the-limitations-of-deep-learning.html)

---

### List of Interesting Blog posts From Major Research Sites.

There are many interesting blog post published last week from major research sites. Here are some for your enjoyment:

Google: 
- [Teaching Robots to Understand Semantic Concepts](https://research.googleblog.com/2017/07/teaching-robots-to-understand-semantic.html)
- [An Update to Open Images - Now with Bounding-Boxes](https://research.googleblog.com/2017/07/an-update-to-open-images-now-with.html)

BAIR 
- [Learning to Learn](http://bair.berkeley.edu/blog/2017/07/18/learning-to-learn/)

OpenAI 
- [Agents that imagine and plan](https://deepmind.com/blog/agents-imagine-and-plan/)
- [Proximal Policy Optimization](https://blog.openai.com/openai-baselines-ppo/)

Artificial Intelligence and Deep Learning Weekly

## Open Source

### [Harvard Machine Learning Project.](https://github.com/Spandan-Madan/DeepLearningProject)

Here is a well-written python notebook written by [Spandan Madan](https://iacs.seas.harvard.edu/people/spandan-madan) on how to establish a machine learning pipeline with deep learning toolkits such as Keras.

[github.com](https://github.com/Spandan-Madan/DeepLearningProject)
