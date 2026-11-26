---
title: "Acoustic Score and Its Signness"
date: 2013-01-25
categories: ["acoustic score", "cmu sphinx", "linguistic score.", "Speech Recognition"]
---

# Acoustic Score and Its Signness

Over the years, I got asked about why acoustic score could be a positive number all the time. That occasionally lead to a kind of big confusion from beginner users. So I write this article as a kind of road sign for people.

Acoustic score per frame is essentially the log value of continuous distribution function (cdf). In Sphinx's case, the cdf is a multi-dimensional Gaussian distribution. So Acoustic score per phone will be the log likelihood of the phone HMM. You can extend this definition to word HMM.

For the sign. If you think of a discrete probability distribution, then this acoustic score thingy should always be negative. (Because log of a decimal number is negative.) In the case of a Gaussian distribution though, when the standard deviation is small, it is possible that the value is larger than 1. (Also see this [link](http://blog.stata.com/2011/02/16/positive-log-likelihood-values-happen/)). So those are the time you will see a positive value.

One thing you might feel disharmonious is the magnitude of the likelihood you see. Bear in mind, Sphinx2 or Sphinx3 are using a very small logbase. We are also talking about a multi-dimensional Gaussian distribution. It makes numerical values become bigger.

Arthur

Also see:  
[My answer on the Sphinx Forum](https://sourceforge.net/p/cmusphinx/discussion/sphinx4/thread/3f9456d9/?limit=25)

---

## Comments

**Jigar Gada** (2013-04-01):

Hey,

while computing the log likelihood, the denominator has a **determinant** of variance term (Mahabalonis distance).
Each of the variance values are on an average 0.01 and multiplication for 39 such terms would lead to 10^(-60) which is a very small number.
Log of reciprocal of that number will be very high which will totally overcome the values of (x - mu)^2.
My question is whether we should consider the determinant.?

**三十三博** (2013-04-01):

Hey Jigar,

My two cents......

The determinant term in a multi-variate Gaussian distribution has the purpose of normalize the exponential terms such that the integral is 1. Most of the systems I know preserved such mathematical nicety.

So what if you deviate from it? Say you have a Baum-Welch algorithm and trained a correct HMM with corresponding GMMS, but in Viterbi, you decided to not use ther determinant terms, what will happen? My experience is the system will still work, probably 2-3% relatively worse than the original.

The reason is practical Viterbi algorithm doesn't have any checking on the correctness of Gaussian distribution you put in. What it cares is a score in absolute log value. We see similar situations in transition probability and language model probability. Not all practical systems follow the rules of summing probabilities to 1. Say when things don't sum to 1, the system usually won't break.
In the case of CDFs, the checking is probably more complicated.

Saying so, why you couldn't see anyone make a system with such an option? I think one of the reasons, no one can predict mathematically how such a defunct Gaussian distribution would behave. Say how you train it? The Math would be wrong. Also when you implement such options, should it be just in Viterbi, or just in BW? Remember, if you trained in one, you better do it in both to avoid mismatch.

Arthur

