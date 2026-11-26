---
title: "How to Ask Questions in the Sphinx Forum?"
date: 2012-12-18
categories: ["acoustic modeling", "data collection", "Language Modeling", "MFE", "MMIE", "MPE", "open source speech recognition", "Sphinx", "Thought"]
---

# How to Ask Questions in the Sphinx Forum?

Many go to different open source toolkits to look for a ready-to-use speech recognizer, and seldom get what they want. Many feel disappointed and curse that developers of open source speech recognizer just couldn't catch up with commercial product. Few know why and few decide to write about the reason. 

People in the field blame Hollywood for lion share of the problem. Indeed, many people believe ASR should work similarly to scenes of Space Odyssey 2001 or Star Trek. We are far far away from there. You may say SIRI is getting close. True. But when you look closer, SIRI doesn't always get what you say right, her strength lies on the very intelligent response system.

Unlike compilers such as GCC, speech recognition toolkit such as the CMU Sphinx project HTK are toolkits. The mathematical models these toolkits provided were trained and fit to certain group of samples. Whereas, applications such as Google Voice or SIRI gather 100 or even 1000 times more data when they train a model. This is the fundamental reason why you don't get the premium recognition rate you think you entitled to.

Many people (me included) saw that as a problem. Unfortunately, to collect clean transcribed data has always been a problem. Voxforge is the only attempt I am aware of to resolve the issue. They are still growing up but it will be a while they can collect enough data to rival with commercial applications.

\* \* \*  
Now what does that tell you when you ask questions in CMU Sphinx or other speech recognition forum? For users who expect out-of-the-box super performance, I would say "Sorry, we are not there yet." In fact, speech recognition, in general, is probably not in performance shown in the original Star Trek yet (that will require accent adaptation and very good noise cancellation since the characters seem to be able to use the recognizer any time they like).

How about many users who have a little bit (or much) programming background? I would say one thing important. As a programmer, you probably get used to look at the code, understand what it's done, do something cute and feel awesome from time-to-time. You can't do that if you seriously want to develop a speech recognition system.

Rather, you should think like a data analyst. For example, when you feel the recognition rate is bad, what is your evidence? What is your data set? What is the size of your data set? If you have a set, can you share the set? If you don't have numerical measure, have you at least use pencil or paper to mark down at least some results and some mistakes? Report them when you ask questions, then you will get useful answers back.

If you go to look at programming forum, many ask questions with the source such that people can repeat the problem easily. Some even go further to pinpoint location of the problem. This is probably what you want to do if you get stuck. 

\* \* \*

Before I end this post, let's also bring up the issue of how usually ASR problem is solved? Like...... if you see performance is bad, what should you do?

Some speech recognition problems can be solved readily. For example, if you try to recognize digit strings but only get one digit at a time, chances are your grammar was written incorrectly. If you see completely crappy speech recognition performance, then I will first check if the front-end of decoder match exactly as the front-end used to train the models. 

For the rest, the strength of the model is really the issue. So most of your time should spend on learning and understanding techniques of model improvement. For example, do you want to collect data and boost up your acoustic model? Or if you know more about the domain, can you crawl some text on the web and help your language model? Those are the first ideas you should think about. 

There are also an exoteric group of people in the world who ask a different question, "Can we use a different estimation algorithm to make the better?" That is the basis of MMIE, MPE and MFE. If you found yourself mathematically proficient (perhaps need to be very proficient......), then learning those techniques and implement some of them would help boosting up the performance as well. What I mentioned such as MMIE are just the basics, each site has their own specialized technique and you might want to know. 

Of course, you normally don't have to think so deep. Adding more data is usually the first step of ASR improvement. If you start to think something advance and if you can, please try to put your implementation somewhere public such that everyone in the world can try it out. These are something small to do, but I believe if we keep on doing something small *right,* there will be a day we can make open source speech recognizers as the commercial ones.

Arthur
