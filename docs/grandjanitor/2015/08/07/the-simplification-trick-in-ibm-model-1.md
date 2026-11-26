---
title: "The Simplification Trick in IBM Model 1"
date: 2015-08-07
---

# The Simplification Trick in IBM Model 1

As a daily reading routine, I try to browse through "Statistical Machine Translation" by Koehn, a famous researcher in the field. Of course, the basic of SMT is IBM Models and the basic of IBM Models is IBM Model 1. So one key derivation is how come when there exponential alignment (${l_f}^{l_e}$) to a computational complexity linear to ($latex{l_f}) and ($latex{l_e}). So it boils down the derivation at equation 4.10:

(Here I assume the readers know the basic formulation of t-tables. Please refer to Ch 4 of [1])

$p(e|f)$

$=\sum_{a} p(e,a|f) ..... (1)$

$= \sum_{a(1)=0}^{l_f}\ldots\sum_{a(l_e)=0}^{l_f} p(e,a|f) ...... (2)$

$= \sum_{a(1)=0}^{l_f} \ldots\sum_{a(l_e)=0}^{l_f}\frac{\epsilon}{(l_f + 1)^{l_e}} \prod_{j=1}^{l_e} t(e_j|f_{a(j)}) ...... (3)$

$= \frac{\epsilon}{(l_f + 1)^{l_e}}\sum_{a(1)=0}^{l_f} \ldots\sum_{a(l_e)=0}^{l_f}\prod_{j=1}^{l_e} t(e_j|f_{a(j)}) ...... (4)$

$= \frac{\epsilon}{(l_f + 1)^{l_e}}\prod_{j=1}^{l_e}\sum_{i=0}^{l_f}t(e_j|f_i) ...... (5)$

It must be trivial to some very smart people, but how come $(4)$ became $(5)$ all the sudden? 

It turns out this is an important trick, it was used in deriving the count function $c$ later in equation 4.13. (An exercise at the back of Chapter 4.) The same trick was also used in Model 2 when alignment probability is modeled. So it might worth a bit of our time to understand why. 

Usually this kind of expression reduction can be formally solved by mathematical induction. But as noted in [2]. Mathematical induction doesn't usually give you useful insight. So let us use another approach. 

Let us first consider the expression with $l_e$ summation signs in equation $(4)$:

$\sum_{a(1)=0}^{l_f} \prod_{j=1}^{l_e}t(e_j|f_i) ...... (6)$

So further we consider the first term of the expression at $(6)$. What is it? It's simply:

$t(e_1 | f_0) \prod_{j=2}^{l_e}t(e_j|f_i)$. 

The second term?

$t(e_1 | f_1) \prod_{j=2}^{l_e}t(e_j|f_i)$. 

So you probably start to get the drift. The $m$-th term of expression $(6)$ is

$t(e_1 | f_m) \prod_{j=2}^{l_e}t(e_j|f_i)$. 

Since all $l_f$ terms have the common factor $\prod_{j=2}^{l_e}t(e_j|f_i)$, you can factorize $(6)$ as 

$(t(e_1|f_0) + t(e_1|f_1) + \ldots + t(e_1 | f_{l_f})\prod_{j=2}^{l_e}t(e_j|f_i)$ 

or

$\sum_{i=0}^{l_f}t(e_1|f_i)\prod_{j=2}^{l_e}t(e_j|f_i)$ 

As a result, you reduce the number of products by one term (in case you don't notice. $j$ is now 2). 

So back to our question. You just need to follow above procedure for $l_e$-times, you will end up re-express equation $(4)$ as 

$(\sum_{i=0}^{l_f}t(e_1|f_i)) \times (\sum_{i=0}^{l_f}t(e_2|f_i)) \ldots \times (\sum_{i=0}^{l_f}t(e_{l_e}|f_i))$ 

So here come equation $(5)$

$= \frac{\epsilon}{(l_f + 1)^{l_e}}\prod_{j=1}^{l_e}\sum_{i=0}^{l_f}t(e_j|f_i)$

Straightly speaking this is not a post for SMT, but more on how one can simplify summands and multiplicands. In many papers, this kind of math is usually skipped and assume the readers know what to do. (I can imagine some friends of mine would say "if you don't know these stuffs, you don't deserve to do ....!") Of course, for mere mortals like us, it could take some time and effort to figure it out. 

Direct manipulation is certainly one way to go. There are also interested rules on how summation indices which sometimes greatly simplify the derivation. If you are interested to read more about the topic, I found that Chapter 2 of Concrete Mathematics ([2]) is a good start. 

Reference: [1] Statistical Machine Translation, Philip Koehn 2010. [2] Concrete Mathematics, Graham et al 2002.
