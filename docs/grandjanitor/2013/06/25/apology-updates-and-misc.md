---
title: "Apology, Updates and Misc."
date: 2013-06-25
categories: ["Dragon", "Goldman", "history", "Microsoft", "MMIE", "oop", "perl", "Python", "Sphinx"]
---

# Apology, Updates and Misc.

There are some questions on LinkedIn about the whereabouts of this blog. As you may notice, I haven't done any updates for a while. I was crazy busy by work in Voci (Good!) and many life challenges, just like everyone. Having a lot of fun with programming, as I am working with two of my most favorite languages - C and Python. Life is not bad at all. 

My apology to all readers though, it could be tough to blog sometimes. Hopefully, this situation will change later this year.....

Couple of worthwhile news in ASR, [Goldman-Sach won the trial in the Dragon law suit](http://www.bloomberg.com/news/2013-06-12/goldman-sachs-s-trial-win-in-dragon-systems-deal-upheld.html). There is also the VB's piece of [MS doubling up speed in their recognizer](http://spectrum.ieee.org/tech-talk/computing/software/microsoft-boosts-speech-recognition-for-its-smartphone). 

I don't know how to make out of the lawsuit but only feel a bit sad. Dragon has been the homes of many elite speech programmers/developers/researchers. Many old-timers of speech were there. Most of them sigh about the whole L&H fiasco. If I were them, I would feel the same too. In fact, once you know a bit of ASR history, you would notice that the fall of L&H gave rise to one you-know-its-name player nowadays. So in a way, the fate of two generations of ASR guys are altered.

As for the MS piece, we are following another trend these days, which is the emergence of DBN. Is it surprising? Probably not, it's rather easy to speed up neural network calculation. (Training is harder, but that's what DBN is strong compared to previous NN approach.)

On Sphinx, I will point out one recent bug contributed by Ricky Chan, which exposed a problem in bw's MMIE training. I am yet to try it but I believe Nick has already incorporated into the open-source code base.

Another items which Nick has been stressing lately is to use python, instead of perl, as the scripting language of SphinxTrain. I think that's a good trend. I like perl and use one-liner, map/grep type of program a lot. Generally though, it's hard to find a concrete coding standard for perl. Whereas python seems to be cleaner and naturally lead to OOP. This is an important issue - perl programmers and perl programming style seems to be spawned from many different type of languages. The original (bad) C programmer would fondly use globals and write functions with 10 arguments. The original C++ programmer might expect language support on OOP but find that "it is just a hash". These style difference could make perl training script hard to maintain.

That's why I like python more. Even very bad script seems to convert itself to more maintainable script. There is also a good pathway for python/C connect. (Cython is probably the best.)

In any case, that's what I have this time. I owe all of you many articles. Let's see if I can write some in the near future.

Arthur

---

## Comments

**Nickolay Shmyrev** (2013-06-27):

&gt; Cython is probably the best

Cython is being dropped from pocketsphinx right now. The common bindgings for Java and Python and Ruby will be implemented through SWIG.

**Arthur Chan** (2013-06-27):

Curious. Is there any reason why we are choosing SWIG instead of cython?

