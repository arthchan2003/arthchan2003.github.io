---
title: "What does an NLP Engineer do?"
date: 2015-12-31
categories: ["Natural Language Processing"]
---

# What does an NLP Engineer do?

After taking the very enjoyable class from [Prof. Radev](http://clair.si.umich.edu/~radev/), I was browsing the forum for some interesting topics. Here one I found, posted by an anonymous student, (rephrase)

*"After taking this course, I still have only a vague grasp of what an NLP Software Engineer does on a daily basis.* *Will the job involve data analysis and modeling? Or data engineering? Or theoretical NLP research? Could anybody share some thoughts?"*

I took a stab, here is a rewritten and extended version:

"It's a good question, it's also a tough one to answer well. In general, it depends on the company you work on. Let's say you work in a bigger company which there is a research department, which is separated from standard programming team. I would also add that some NLP engineers are actually managers. So their role was mostly general organization of the activity of a team.

If you minus pure coding and pure programming task, I would say there are usually 2 types of task you will encounter: 
1. *NLP component update and improvement:* e.g. Say you are working on a word sense disambiguation routine. Through data collection, you were able to increase the amount of the data by 10 times, so your boss assign you to re-train the existing SVM which you trained a while ago. Your job in this case, is not that different from HW3 (***Arthur: i.e. a WSD exercise using machine learning***) : you are going to massage the data, train a model, benchmark it and present it to your group. Hopefully and eventually deploy it to real-life.
2. *Integration:* Now suppose you are more coding-oriented, then it's possible that you are asked to incorporate a pre-existing program written by your colleagues. So your major task is to be the one who is responsible for such process. Note that this requires different skill set from a vanilla programmer, you do need to understand the underlying NLP technology quite well to integrate an NLP component. Of course, there will be issues remained from your more research oriented colleague to you. That includes speed or memory optimization, etc.

Both task 1 or 2 can be infinitely complex and difficult in real-life. e.g. You might be handed a task which is very difficult to improve upon. May be because previous research has exhausted most of the routes of improvement. Then in that case, you will play the role of pure researcher and think up new methods to improve the task. Or if you are working on modeling, then significant amount of your time would be spent on modeling, tending different experiments, as well as data preparation (see below).

Similarly, in task 2, you can be handed with a program which consists of 100k+ lines of C/C++ code. You need to take care of all system-related issues, pop up gdb and spend couple of waking time to fix a multi-thread program. Or you will need to make sure the plumbing of your application works with your researcher colleague. Those are also difficult skills which take years to refine.

In my case, I am more an integrator on speech recognition components. I also do quite a dose of R&D on other ML components (see [this post](/grandjanitor/2015/12/10/real-life-machine-learning/)). In the past, my role was more on the pure research side. For example, my BBN role was a kind of experimenter to work on unsupervised topic detection.

In any case, I think Prof Radev's class presents students a very good summary of what real-life NLP people do. Because we are mostly try to practice on task 1 and task 2.

There are perhaps two exceptions of task 1 and 2: 
1. First exception I would mention is **data preparation**. Normally you will have to prepare data yourself. The very nice thing happens in our homework that a TA wrote a working XML parser for input data? It seldom happens. That explains why many people claim "data preparation is 80% of machine learning.
2. The second exception is you might ask to analyze and present your results. i.e. **data analysis.** Analysis is more the arena of statistics and data science. It is also an important skill. But in my experience, product-oriented engineers are spending less time on those aspects. Because most of the time you are either researching or developing the product. Your analytical skill is mostly used when you are stuck. For example, I seldom use data analysis in my work (descriptive? exploratory? casual?) unless I saw a rare phenomenon. But a data scientist is more likely to use those skills daily. "

Arthur
