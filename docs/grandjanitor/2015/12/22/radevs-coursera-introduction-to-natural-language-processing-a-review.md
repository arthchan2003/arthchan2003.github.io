---
title: "Radev's Coursera Introduction to Natural Language Processing - A Review"
date: 2015-12-22
categories: ["Dan Jurafsky", "Dependency Parsing", "Dragomir Radev", "HMM", "Language Modeling", "Machine Learning", "Natural Language Processing", "Parsing", "POS tagging", "Programming", "Python", "SMT", "Word Sense Disambiguation"]
tags: ["Michael Collins"]
---

# Radev's Coursera Introduction to Natural Language Processing - A Review

As I promised [earlier](/grandjanitor/2015/12/10/real-life-machine-learning/), I was going to review Prof. Dragomir Radev's [introductory class on natural language processing](https://www.coursera.org/course/nlpintro). Few words about Prof. Radev: from [his Wikipedia entry](https://en.wikipedia.org/wiki/Dragomir_R._Radev), Prof Radev is an award winning Professor, who co-found [North American Computational Linguistics Olympiad ](https://en.wikipedia.org/wiki/North_American_Computational_Linguistics_Olympiad)(NACLO), which is the equivalent of [USAMO](https://en.wikipedia.org/wiki/North_American_Computational_Linguistics_Olympiad) in computational linguistics. He was also the coach of U.S. coach of International Language Olympiad 2011 and helped the team won several medals [1]. I think these are great contributions to the speech and language community. In late 90s, when I was still in undergraduate, there was not much recognition of computational language processing as an important computation skill. With competition in high-school or college level, there will be a generation of young minds who would aspire to build intelligent conversation agent, robust speech recognizer and versatile question and answering machine. (Or else everyone would think Linux kernel is the only cool hack in town. :) ) 

# The Class

So how about the class? I got to say I am more than surprised and happy with it. I was searching for an intro NLP class, so the two natural choices was [Prof. Jurafsky' and Manning' s ](https://www.coursera.org/course/nlp)and [Prof. Collin's](https://www.coursera.org/course/nlangp) Natural Language Processing. Both classes received great praise and comments and few of my friends recommend to take both. Unfortunately, there was no class offering recently so I could only watch the material off-line.

Then there comes the Radev's class, it is as Prof. Radev explains: "more introductory" than Collin's class and "more focused on Linguistics and resources" than Jurafsky and Manning. So it is good for two types of learners: 
1. Those who just started out in NLP.
2. Those who want to gather useful resources and start projects on NLP.

I belong to both types. My job requires me to have more comprehensive knowledge of language and speech processing. 

# The Syllabus and The Lectures

The class itself is a brief survey of many important topics of NLP. There are the basics: parsing, tagging, language modeling. There are the advanced topics such as summarization, statistical machine translation (SMT), semantic analysis and dialogue modeling. The lectures, except occasionally mistakes, are quite well done and filled with interesting examples.

My only criticism is perhaps the length of videos, I would hope that most videos I watch would be less than 10 minutes. That makes it easier to rotate with my other daily tasks.

The material is not too difficult to absorb for newcomers. For starter, advanced topic such as SMT is not covered in too much detail mathematically. (So no need to derive EM on IBM models.) That I think it's quite appropriate for first time learners like me.

One more unique feature of the lectures: it fills with interesting NACLO problems. While NACLO is more a high-school level competition, most of the problems are challenging even for experienced practitioners. And I found them quite stimulating. 

# The Prerequisites and The Homework Assignments

To me, the fun part is the homework. There were 3 of them, they focus on, 
1. Nivre's Dependency Parser,
2. Language Modeling and POS Tagging,
3. Word Sense Disambiguation

All homework are based on python. If you know what you are doing, they are not that difficult to do. For me, I spent around 12-14 hours on each. (Those are usually weekends.) Just like [Ng's Machine Learning class](https://www.coursera.org/learn/machine-learning), you need to match numbers with the golden reference. I think that's the right approach to learn any machine learning task the first time. Blindly come up with a system and hope it works never get you anywhere.

The homework does speak about an issue of the class, i.e. you *do need to know the basics of Machine Learning* . Also, if you never had any programming experience would find the homework very difficult. This probably described many linguistic students but never take any computer science classes. [3] You can still "power it through" and pass. But it can be unnecessarily hard.

So I will recommend you first take the Ng's class or perhaps the latest Machine Learning specialization from Guestrin and Fox first. Those are the classes which would give you some basics of programming as well as basic concept of Machine Learning.

If you didn't take any machine learning class, one way to go through more difficult classes like this is to read forum messages. There are many nice people in the course was answering various questions. To be frank, if the forum doesn't exist, then it will take me around 3 times more time to finish all assignments. 

# Final Word

All-in-all, I highly recommend Prof. Radev's class to anyone who is interested in NLP. As I mentioned though, the class does require prerequisite such as basics of programming and machine learning. So I would recommend any learners to first take the Ng's class before taking this one.

In any case, I want to thank Prof. Radev and all teaching staffs who prepare this wonderful course. I also thank to many classmates who help me through the homework.

Arthur 

# Postscript at 2017 April

After I wrote this review, Coursera had since upgraded to the new format. It's a pity none of the NLP classes, including Prof. Radev's survive. To bad for NLP lovers!

There is also a seismic shift in the field of NLP toward deep learning. While deep learning does not dominate evaluations like in computer vision or speech recognition, it is perhaps the most actively researched direction right now. So if you are curious about what's new, consider to take the latest [Standford cs224n 2017](https://www.youtube.com/watch?v=OQQ-W_63UgQ&list=PL3FW7Lu3i5Jsnh1rnUwq_TcylNr7EkRe6) or [Oxford's Deep Learning for NLP](https://www.youtube.com/playlist?list=PL613dYIGMXoZBtZhbyiBqb0QtgK6oJbpm).

[1] http://www.eecs.umich.edu/eecs/about/articles/2010/Radev-Linguistics.html

[2] Week 1 Lecture 1 Introduction

[3] One anecdote: In the forum, some students was asking why you can't just sum all data points of a class together and pour into scikit-learn's fit(). I don't blame the student because she started late and lacks of prerequisite. She later finished all assignment and I really admire her determination.
