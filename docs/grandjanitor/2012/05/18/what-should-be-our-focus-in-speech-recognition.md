---
title: "What should be our focus in Speech Recognition?"
date: 2012-05-18
categories: ["cmu sphinx", "decoder", "dictionary", "HTK", "Speech Recognition", "Thought", "training"]
---

# What should be our focus in Speech Recognition?

If you worked in a business long enough, you start to understand better what type of work are important. As many things in life, sometimes the answer is not trivial. For example, in speech recognition, what are the important ingredients to work on? 

Many people will instinctively say the decoder. For many, the decoder, the speech recognizer, oorr the "computer thing" which does all the magic of recognizing speech, is the core of the works. 

Indeed, working on a decoding is loads of fun. If you a fresh new programmer, it is also one of those experiences, which will teach you a lot of things. Unlike thousands of small, "cool" algorithms, writing a speech recognizer requires you to work out a lot of file format issues, system issues. You will also touch a fairly advanced dynamic programming problem : writing a Viterbi search. For many, it means several years of studying source code bases from the greats such as HTK, Sphinx and perhaps in house recognizers. 

Writing a speech recognizer is also very important when you need to deal with speed issues. You might want to fit a recognizer into your mobile phone or even just a chip. For example, in Voci, an FPGA-based speech recognizer was built to cater ultra-high speed speech recognition (faster than 100xRT). All these system-related issues required understanding of the decoder itself. 

This makes speech recognition an exciting field similar to chess programming. Indeed the two fields are very similar in terms of code development. Both require deep understanding of search as a process. Both have eccentric figures popped up and popped out. There are more stories untold than told in both field. Both are fascinating fields.

There is one thing which speech recognition and chess programming are very different. This is also a subtle point which even many savvy and resourceful programmers don't understand. That is how each of these machines derived their knowledge sources. In speech, you need to have a good model to do decent jobs for your task. In chess though, most programmers can proceed to write a chess player with the standard piece values. As a result, there is a process before anyone can use a speech recognizer. That is to first train an acoustic model and a language model. 

The same decoder, having different acoustic models and language models, can give users perceptions ranging from a total trainwreck to the a modern wonder, borderline to magic. Those are the true ingredients of our magic. Unlike magicians though, we are never shy to talk about these secret ingredients. They are just too subtle to discuss. For example, you won't go to a party and tell your friends that "Using an ML estimate is not as good as using an MPFE estimate in speech recognition. It usually results in absolutely 10% performance gap." Those are not party talks. Those are talks when you want to have no friends. :)

In both type of tasks, one require learning different from a programming training. 10 years ago, those skill are generally carried by "Mathematician, Statistician or People who specialized in Machine Learning". Now there is new name : "Big Data Analyst". 

Before I stopped, let me mention another type of work, which are important in real life. What I want to say is transcription and dictionary work. If you asked some high-minded researchers in the field, they will almost think those are not interesting work. Yet, in real-life, you can almost always learn something new and improve your systems based on them. May be I will talk about this more next time.

The Grand Janitor
