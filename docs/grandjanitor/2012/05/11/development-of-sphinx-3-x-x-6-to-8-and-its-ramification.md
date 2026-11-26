---
title: "Development of Sphinx 3.X (X = 6 to 8) and its Ramification."
date: 2012-05-11
categories: ["3.0", "3.5", "3.6", "3.7", "cmu sphinx", "sphinx 3"]
---

# Development of Sphinx 3.X (X = 6 to 8) and its Ramification.

One of the things I have done back in Sphinx is to so called "Great Refactoring" of Sphinx 3, SphinxTrain and sphinxbase. It was started by me but mostly took up by Dave (in a disgruntled manner :) ). I write this article to reflect the whole process and ask if I have done the right thing.

The background is like this: as you know, the CMU sphinx project has many recognizers. Sphinx2, 3, 4, PocketSphinx and MultiSphinx. It's easy to understand why that happened in the first place. CMU is an university and understandably would have many different types of projects. In essence, when someone think of a good new idea, they will simply implement a recognizer. The by-product of it would be a PhD thesis or some kind of project reports. 

There is nothing wrong with that. Think of the pain of understanding and changing a recognizer which has 10-30 thousand lines of code, you will know that it is not for the faint of heart. Many of the original programmers of the recognizers also have practical reason to ignore code re-usability - many of them have deadlines to meet. So I always feel empathy towards them. 

Of course, on the other side of the coin, having many recognizers gives users a mild amount of pain. Just to look at 3.0 and 3.3, command-line interface had changed (e.g. -meanfn becomes -mean). So when people need to interface with the code, it would take some understanding. The bigger problem is that do you expect a certain feature appears in one of the decoders to appear in another? This kind of inconsistency is very hard to explain to normal users. 

So here comes the first change at 3.5, or around 6-7 years ago, I decided to merge 3.0's series of tools and recognizer with 3.3, the fast decoder. I got to say, the decision is mainly driven by young naivete and year-long insomnia. ( :) ). There were also frustration from users which drove me to make those changes. In 3.5, the main thing I did was just to "port" the tool from the old 3.0 such as allphone, astar, align to 3.x. There are some command-line interface changes. So far, all are cool.

Then it comes to 3.6, at this point, I started to realize a lot of underlying functions and libraries are duplicated. For example, we have multiple GMM computation routines but you can't use them in all tools which call GMM computation. Like allphone in 3.5 used GMM computation, but you can't expect any fast GMM computation in 3.4 can be used in allphone. Simply because the library wasn't shared.

So what did young and naive me thought? Let's try to write a single architecture to incorporate all these different things! (!!!!) Now... this is what I think where things go wrong. 

Let me explain a little bit more. There is a legitimate reason why the original programmer (Ravi) decides to split the tools into multiple parts and let code duplicates. Simply because, the issue in align is not necessarily the issue of decode. If the programmer of align needs to consider issues of decode, then it will take a long time to really get any programming done.

This happens to be the case of Sphinx 3.X. Now for the development of Sphinx 3.X, there was another undesirable factor. That is I decided to leave - I simply couldn't overcome the economic force at the time - a startup company is willing to hire me. 

To complicate the matter, we \*also\* decide to factor out common parts between SphinxTrain and sphinx3 to avoid code duplication between the two. Again, it is driven by legitimate concern, the fact that there were two feature extraction routines in two packages constantly make users ask themselves whether the front-end are matched.

All of these except I am leaving are good things but they just entail coding time. Now the end effect is that it makes the effort too big, too time-consuming. 3.6 took me around 1 year to write and release. I release an official release at around mid of 2006 but there are still too many issues in the program. The latter 3.8, Dave has taken up and really fixed many bugs. So I always think it's Dave to make sphinx 3.X in the current stable form.

To the credit of the guys in the team, they really bash me : Evandro, being circumspect and consistent, always asked if it is a good idea in the first place. Ravi, always the wise man, had brought up the issues of merging the code. And of course, there is Dave, he deserves most of the credits for fixing a lot of nasty bugs. 

So, in fact, it is really I should be blamed in the process. I guess I am finally mature enough to apologize to everyone.

So you may wonder why I said all of these? Oh well, first of all, that's because I am going to put work on the recognizers again. Not just on Sphinx 3, but all other recognizers. So my first hope is that I don't repeat my past problems. 

Now given the code is being iterated in last 6 years, the benefit of merging the code in Sphinx 3 starts to really show up. People can do a lot of more things than the past. Is it good enough? I don't think so. Sphinx 3 has a lot of potentials but it's very misunderstood. In a nutshell, I need to put more work on it in the future.

The Grand Janitor
