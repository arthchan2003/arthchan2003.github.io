---
title: "Different HMMSets in HTK"
date: 2015-08-02
categories: ["ASR"]
tags: ["ASR", "HMM/GMM"]
---

# Different HMMSets in HTK

HTK was my first speech toolkit. It's fun to use and you can learn a lot of ASR by following the manual carefully and deliberately.

If you are still using HMM/GMM technology (interesting but why?), here is a thread a year ago on why there are different HMM Types in HTK.

One thought I have: when I first start out in ASR, I seldom think of any human elements in a design. Of course, it has to deal with the difficulty of understanding all these terminologies and algorithms.

Yet ASR research has to do a lot with rival groups come up with different ideas, each try to bet against each other on the success of a certain technique.

So sometimes you would hope that competition would make technology finer. Yet a highly competitive environment only nurture followers, rather than competitive loner groups such as Prof. Young's , or MSR (whom AFAIK built the first working version of DNN-based ASR).

Arthur

" *Hi,*

*I'm a student who's looking into the HTK source code to get some idea* * about practical implementation of HMMs. I have a question related to* * the design choices of HTK.*

*AFAIK, the current working set of HMMs (HMMSet) has 4 types: plain,* * shared, tied, discrete.* * HMM sets with normal continuous emission densities are "plain" and* * "shared", only difference being that some parameters are shared in the* * latter. Sets with semi-continuous emission densities (shared Gaussian* * pools for each stream) are called "tied" and discrete emission* * densities are "discrete".*

*If someone uses HTK, isn't there a high chance of using only one of* * these types? The usage of these types is probably mutually exclusive.* * So my question is, why not have separate training and recognition* * tools for continuous, semi-continuous and discrete HMM sets? Here are* * some pros and cons of the current design I can think of, which of* * course can be wrong:*

*pros:* * - less code duplication* * - simpler interface for the user*

*cons:* * - more code complexity* * - more contextual information required to read, more code jumps* * - unused variables and memory, examples: vq and fv in struct* * Observation, mixture alignment in discrete case*

*If I were to implement HMMs supporting all these emission densities,* * what path should I follow? How feasible is it to use OOP principles to* * create a better design? If so, why weren't they leveraged in HTK?*

*Warm regards,* * Max*"

(I trimmed out Mr. Neil Nelson's reply, which basically suggest people should use Kaldi instead.)

" *Max and Neil*

*I don’t usually respond to HTK questions, but this one was hard to resist.*

*I designed the first version of HTK in Cambridge in 1988 soon after moving from Manchester where I worked for a while on programming language and compiler design. I was a strong advocate of modular design, abstraction and OOP. However, at that time, C++ was a bit of a nightmare. There was little standardisation across operating systems and some implementations were very inefficient. As a result I decided that since HTK had to be very efficient and portable across platforms, it would be written in C, but the architecture would be modular and class like. Hence, header files look like class interfaces, and body files look like class method implementations.*

*When HTK was first designed, the “experts” in the US DARPA program had decided that continuous density HMMs would never scale and that discrete and semi-continous HMMs were the way to go. I thought they were wrong, but decided to hedge my bets and built in support for all three - whilst at the same time taking care that the implementation of continuous densities was not compromised by the parallel support for discrete and semi-continuous. By 1993 the Cambridge group (and the LIMSI group in France) were demonstrating that continuous density HMMs were significantly better than the other modelling approaches. So although we tried to maintain support for different emission density models, in practice we only used continuous densities for all of our research in Cambridge.*

*It is a source of considerable astonishment to me that HTK is still in active use 25 years later. Of course a lot has been added over the years, but the basic architecture is little changed from the initial implementation. So I guess I got something right - but as Neil says, things have moved on and today there are good alternatives to HTK. Which is best depends on what you want to do with it!*

*Steve Young*"
