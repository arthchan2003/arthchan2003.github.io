---
title: "AIDL Weekly Issue #74 - Facebook vs Fake News (or AI vs Fake News?)"
date: 2019-07-25
---

# AIDL Weekly Issue #74 - Facebook vs Fake News (or AI vs Fake News?)

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 74 *September 17th 2018* ](http://aidl.io/issues/74/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we look into the details of Facebook's usage of machine learning in detecting misinformation. What is the purpose of their latest Rosetta system?. And how prepared is Facebook against faked news? 

As always, if you find this newsletter useful, feel free to share it with your friends/colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 173,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### [Tesla T4](https://www.tomshardware.com/news/nvidia-tesla-t4-turing-gpu,37788.html)

Tesla T4 was just announced. Let's take a look some notable features: 
- INT4 and INT1 (experimental) - once a team optimizes some deep learning code by lowering the floating point precision, the inevitable next step would be converting the floating point code into integer. Supporting INT4 and INT enable bleeding-edge team to create even faster product.
- TensorRT Hyperscale: A collection of packages which wrap around T4. Sounds exciting and TensorRT5 can be used to optimize inference-related operations.
- 16G: This sounds like a lot, if you think of resnet scale. But then, you can imagine real-life convnet already reaches this limit which is imposed by earlier version of the card.

Of course there are also spec improvements. But overall speaking, T4 feels incremental. (And yeah, what happens after INT1?) In some sense, we are all waiting for a mass availability of TPU-like product released either by Google or up-and-coming but ultra secretive company such as [Groq](https://www.crunchbase.com/organization/groq). This is especially true when we talk about inference time. 

[tomshardware.com](https://www.tomshardware.com/news/nvidia-tesla-t4-turing-gpu,37788.html)

---

### Deals and Acquisitions

[Microsoft Acquires Lobe](https://venturebeat.com/2018/09/13/microsoft-acquires-ai-startup-lobe-to-help-people-make-deep-learning-models-without-code/) 

Also take a look at [the trends in AI in healthcare fundings](https://www.cbinsights.com/research/report/ai-trends-healthcare/).

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [The Facebook Rosetta System](https://code.fb.com/ai-research/rosetta-understanding-text-in-images-and-videos-with-machine-learning/)

Facebook has been plagued by faked news and misinformation. It's a challenging problem. How would you solve it? 

As it turns out, one of the thorniest problem is detecting text within memes. Memes' text could come from different languages, have weird symbols, so a vanilla text detector is unlikely to give the best performance. As a result, Facebook comes up with Rosetta, their own text detection+recognition system.

So here are couple of notes on Rosetta which we think is quite interesting: 
- For starter, it is based on FasterRCNN. Technically, this is very interesting, because unlike YOLO, FasterRCNN is known to be more accurate yet much slower. How did FB guys speed it up? It turns out they use 1-year old idea (Shufflenet)[https://arxiv.org/pdf/1707.01083.pdf] to reduce the size of the networks. In the actual implementation, Facebook is using a non-trivial optimization of GEMM which utilized INT8. This further improves the speed of inference.
- Then there is recognition. Would it be an all-in-one network of both detection and recognition? It doesn't seem to be the case. Recognition itself is trained by [Connectionist temporal classification (CTC) cost function](https://www.cs.toronto.edu/~graves/icml_2006.pdf). As a side note, CTC seems to be a more popular method in OCR. Whereas in speech recognition, other seq2seq paradigm seems to be still in active research.
- With both detection and recognition network all set, we just need to tap the Facebook's unlimited amount of training data right? Ah, but then where are the labels? So the researchers decided to use a another approach which tries to generate text "in the wild". Classic example of data augmentation to come save the day.

Overall, Rosetta showcases a world-class level of engineering expertise. It churns out text and the input of many FB text analysis engines. The next big problem for FB now is how to engineer a programmatic system to fact-check at scale, which could be even more challenging.

For deeper dive into their text detection, take a look of the FB [impressive paper at KDD18](http://www.kdd.org/kdd2018/accepted-papers/view/rosetta-large-scale-system-for-text-detection-and-recognition-in-images)?

[fb.com](https://code.fb.com/ai-research/rosetta-understanding-text-in-images-and-videos-with-machine-learning/)

---

### [Zuckerberg's view on How prepared FB is on Faked New and Misinformation](https://www.facebook.com/notes/mark-zuckerberg/preparing-for-elections/10156300047606634/)

This is the widely-circulated write-up by Mark Zuckerberg. He discusses how well Facebook is prepared for the the upcoming US Mid-term election. 

As you might read in the news, US Justice Department has been pressing criminal charges on hackers (for example, see [here](https://www.independent.co.uk/life-style/gadgets-and-tech/news/tumblr-russian-hacking-us-presidential-election-fake-news-internet-research-agency-propaganda-bots-a8274321.html) ) which spread faked news on the internet, which allegedly affect US presidential election back in 2016. Of course, Facebook is in hot water when many of these fake information are spread through their network. How would they respond?

The question for us AIDLers is: Can we just create learning machines which filter out what is faked news or not? This seems to be just a simple text classification problem, but then several factors make the problem much harder. Actual human fact-checkers not only try to resolve if a piece of news is true or not, they also actively seek information from sources by interviewing them. The reason is simple: To determine if something is truth, you need to seek knowledge in the real world and decide. For a hypothetical example: to decide if a Pizza joint is actually selling pepperoni pizzas, just text doesn't give you enough information, someone will need to gather information from the restaurant directly and ask "Do you actually sell pepperoni pizza?" or even ask for a pepperoni pizza and see if the restaurant can prove they can produce one.

This knowledge of the world has a fancy term called "ontology". Ontology as a study comes from philosophy which dictionary would say it means "knowledge of being". But in our sense, it is more just a kind of "world knowledge". In some sense, human fact-checkers are able to effectively gather world-knowledge to judge a piece of news. Is it possible for us to replicate that capability? Unfortunately, while NLP driven by ontology is under active research, we don't see it matures any time sooner.

Now perhaps you can see how tough it is for machine-based fact-checking. If you look at Zuckerberg's address closely, machine learning only appears once and his focus in on automatic detection of fake accounts. And as we learn from the example of Rosetta, we also learn that FB has impressive effort to extract text from images such as memes. In the note, you may see Rosetta was used in detecting hate speech, which again we can think of as a more trivial case of text classification. But then, *none of these efforts really automate fact-checking*. That's why Facebook is using independent agency to fact-check news. So in a sense, we still need to resort to humans.

So when Zuckerberg said: 

> Today, Facebook is better prepared for these kinds of attacks.

We sense cautiousness ... and honesty from him. Compared to two years ago, technology has advanced such that we should be able to extract all texts (from images, from voice and from text) more easily. But to detect the "faked"ness of news? We are not yet "well-prepared".

[facebook.com](https://www.facebook.com/notes/mark-zuckerberg/preparing-for-elections/10156300047606634/)

---

### [How to get started with Keras, Deep Learning, and Python - by Adrian Rosebrock](https://www.pyimagesearch.com/2018/09/10/keras-tutorial-how-to-get-started-with-keras-deep-learning-and-python/)

Here is another post from Adrian Rosebrock. This time is about how you should use Keras. It sounds common but once again you should look at the strength of Rosebrock - he is always very detail-oriented and come up with genuinely useful blog posts. 

So what is the biggest problem of using Keras then? Well, installation. In fact, if you learn how to install a deep learning chain correctly on ... let's make a simpler case... Linux, then you are probably the favorite in your workplace. That's because deep learning, developed to now, has a complicated toolchain, which is similar to compiling a compiler or doing cross-compilation. That's why a detail tutorial would be nice.

So this is this Rosebrock's tutorial does. The first step he guide you through is to install Keras correctly. There are more and we don't want to give a spoiler. So take a look?

[pyimagesearch.com](https://www.pyimagesearch.com/2018/09/10/keras-tutorial-how-to-get-started-with-keras-deep-learning-and-python/)

---

### [Anatomy of AI System](https://anatomyof.ai/)

This is perhaps the most beautiful infographic on how a AI household product like Echo is actually made in practice. The graph includes many non-AI components, but that's just the realty of AI product development: algorithms, even machine learning is just a very small part of the equation. 

[anatomyof.ai](https://anatomyof.ai/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 173,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. 

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
