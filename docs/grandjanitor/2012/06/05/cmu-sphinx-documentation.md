---
title: "CMU Sphinx Documentation"
date: 2012-06-05
categories: ["cmu sphinx", "cmu sphinx documentation"]
---

# CMU Sphinx Documentation

I was browsing the documentation section of cmusphinx.org and was very impressed. Compared to my ad-hoc version of documents back in www.cs.cmu.edu/~archan, or the old robust group document, it is a huge improvement. 

What is the challenging to develop documentation for speech recognition? I believe the toughest part is that some people still see speech recognition as a programming task. In real-life though, speech recognition application should be viewed as a data analysis task. 

Here is why: suppose you work on a normal programming task, once you figure out the algorithm, you job is pretty much done. 

On a speech app though, that is just a tiny step towards a system which is good. For example, you might notice that your dictionary is not refined enough such that some of the words are not recognized correctly. Or you found that your language model has something wrong such that a certain trigrams never appears. 

Those tasks, in terms of skill sets, require a person to stay in front of the Linux console, then come up with a Eureka moment : "Oh, that's what's wrong!". So the job "Speech Scientist" usually requires knowledge of statistics, machine learning and more generally good analytic skills.

Your basic Linux skill is also extremely important: e.g. a senior researcher once shows me how he did many things solely on perl one-liner. As it turns out, when you can wield perl one-liner correctly, you can solve many text processing problem with one command! This would save you a lot of time in writing a throw-away script and allow you to focus on analysis why things are going wrong.

Back to good speech application documentation: one of the challenging part is to convey this real-life work-flow of Speech Scientist to the open source community. Many of us learn (and thrive to learn more...) this kind of skill in a hard way: writing reports, papers, presentations and be ready to get feedback from other people. You will also find yourself amazed by some brilliant insights and analyses too. (There are stupid analysis too but that's parts of life......)

The Sphinx project collectively has gone a long way on this front of development. If you have time, check out  
http://cmusphinx.org/wiki, I found much of material very useful. Check it out!

The Grand Janitor.
