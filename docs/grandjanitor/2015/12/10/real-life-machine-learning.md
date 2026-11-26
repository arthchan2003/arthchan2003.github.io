---
title: "Experience in Real-Life Machine Learning"
date: 2015-12-10
categories: ["Classification", "Debugging", "Machine Learning", "Programming"]
tags: ["gender detection", "Machine Learning"]
---

# Experience in Real-Life Machine Learning

I have been refreshing myself on the general topic of machine learning. Mostly motivated by job requirements as well as my own curiosity. That's why you saw my review post on the famed [Andrew Ng's class](/grandjanitor/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/). And I have been taking the [Dragomir Radev's NLP class](https://www.coursera.org/course/nlpintro), as well as the [Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning) by Emily Fox and Carlos Guestrin [1]. When you are at work, it's *tough to learn*. But so far, I managed to learn something from each class and was able to apply them in my job.

So, one question you might ask is how applicable are on-line or even university machine learning courses in real life? Short answer, *they are* *quite different*. Let me try to answer this question by giving an example that come up to me recently.

It is a gender detection task based on voice. This comes up at work and I was tasked to improve the company's existing detector. For the majority of the my time, I tried to divide the data set, which has around 1 million data point to train/validation/test sets. Furthermore, from the beginning of the task I decided to create sets of dataset with increasing size. For example, 2k, 5k, 10k..... and up to 1 million. This simple exercise, done mostly in python, took me close to a week.

Training, aka *the fun part*, was comparatively short and *anti-climatic*. I just chose couple of well-known methods in the field. And test on the progressively sized data set. Since prototyping a system is so easy, I was able to weed out weaker methods very early and come up with a better system. I was able to get high relative performance gain. Before I submitted the system to my boss, I also worked out an analysis of why the system doesn't give 100%. No surprise. it turns out volume of the speech matters, and some individual of the world doesn't like their sex stereotypes. But so far the tasks are still quite well-done because we get better performance as well as we know why certain things don't work well. Those are good knowledge in practice.

One twist here, after finishing the system, I found that the method which gives the best classification performance doesn't give the best speed performance. So I decided to choose a cheaper but still rather effective method. It hurts my heart to see the best method wasn't used but that's the way it is sometimes.

Eventually, as one of the architects of the system, I also spent time to make sure integration is correct. That took coding, much of it was done in C/C++/python. Since there were couple of bugs from some existing code, I was spending about a week to trace code with gdb.

The whole thing took me about three months. Around 80% of my time was spent on data preparation and coding. Machine learning you do in class happens, but it only took me around 2 weeks to determine the best model. I could make these 2 weeks shorter by using more cores. But compare to other tasks, the machine learning you do in class, which is usually in the very nice form, "Here is a training set, go train and evaluate it with evaluation set.", seldom appears in real-life. Most of the time, *you are the one who prepare the training and evaluation set.*

So if you happen to work on machine learning, do expect to work on tasks such as web crawling and scraping if you work on text processing, listen to thousands of waveforms if you work on speech or music processing, watch videos that you might not like to watch if you try to classify videos. *That's machine learning in real-life.*  If you happen to be also the one who decide which algorithm to use, yes, you will have some fun. If you happen to design a new algorithm. then you will have a lot of fun. But most of the time, practitioners need to handle issues, which can just be .... mundane. Tasks such as web crawling, is certainly not as enjoyable as to apply advanced mathematics to a problem. But they are incredibly important and they will take up most of time of your or your organization as a whole.

Perhaps that's why you heard of the term "data munging" or in Bill Howe's class: "data jujitsu". This is a well-known skill but not very advertised and unlikely to be seen as important. But in real-life, such data processing skill is crucial. For example, in my case, if I didn't have a progressive sized datasets, prototyping could take a long time. And I might need to spend 4 to 5 times more experimental time to determine what the best method is. Of course, debugging will also be slower if you only have a huge data set.

In short, data scientists and machine learning practitioners spend majority of their time as data janitors. I think that's a well-known phenomenon for a long time. But now as machine learning become a thing, there are more awareness [2]. I think this is a good thing because it helps better scheduling and division of labors if you want to manage a group of engineers in a machine learning task.

[1] I might do a review at a certain point. [2] [e.g. This NYT article](http://www.nytimes.com/2014/08/18/technology/for-big-data-scientists-hurdle-to-insights-is-janitor-work.html?_r=0).
