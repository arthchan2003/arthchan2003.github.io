---
title: "The Probability Integral"
date: 2016-01-04
categories: ["Special Functions", "Statistics"]
tags: ["Math", "Probability Integral"]
---

# The Probability Integral

Math of machine learning boils down to probability theory, calculus and linear algebra/matrix analysis. The one gem which mesmerizes me most is the so called "probability integral", termed by [Prof. Paul J. Nahin](https://en.wikipedia.org/wiki/Paul_J._Nahin), author of *[Inside Interesting Integrals](http://www.amazon.com/Inside-Interesting-Integrals-Substitutions-Undergraduate/dp/1493912763) [1].* Or as you might learn in either probability theory or random process class:

$F(x)=\int_{-\infty}^{\infty}e^{\frac{-x^2}{2}}dx$

Of course, this is related to [the Gaussian distribution](https://en.wikipedia.org/wiki/Normal_distribution). When I learnt the probability integral, I first learned the now standard trick of "polar integration" [2]. i.e. We first create a double integral, then transform the integrand using polar coordinate transformation. Here is the detail. Since $F(x)$ is an even function. We just need to consider

$I=\int_{0}^{\infty}e^{\frac{-x^2}{2}}dx$

$I^2=\int_{0}^{\infty} e^{\frac{-x^2}{2}}dx \int_{0}^{\infty} e^{\frac{-y^2}{2}}dy=\int_{0}^{\infty}\int_{0}^{\infty}e^{\frac{-x^2}{2}}e^{\frac{-y^2}{2}}dxdy=\int_{0}^{\infty}\int_{0}^{\infty}e^{\frac{-(x^2+y^2)}{2}}dxdy$

Then let $x=r\cos\theta$, and $y=r\sin\theta$, the Jacobians

$\frac{\partial(r,\theta)}{\partial(x,y)}=\begin{vmatrix}\cos\theta & -r\sin\theta \\ \sin\theta & r\cos\theta\end{vmatrix} = r (\sin^2\theta+cos^2\theta) =r$.

Substitute to $1$.

$I^2=\int_{0}^{\frac{\pi}{2}}\int_{0}^{\infty}re^{\frac{-r^2}{2}}drd\theta$

$=\int_{0}^{\frac{\pi}{2}}(\left.-e^{-r^2}\right|_{0}^{\infty})d\theta=\int_{0}^{\frac{\pi}{2}} (0 - (-1))d\theta=\int_{0}^{\frac{\pi}{2}}d\theta= \frac{\pi}{2},$

or $I = \sqrt{\frac{\pi}{2}}.$

So $F(x) = 2 * \sqrt{\frac{\pi}{2}} = \sqrt{2\pi}$.

This is a well known result, you can find it in almost all introductory book on probability distribution.

This derivation is a *trick.* Quite frankly, without reading the textbook. I wouldn't have the imagination to come up with smart way to derive integrals. Perhaps that's why Prof. Nahin said in his book *Inside Interesting Integral [4] :* 

> THIS IS ABOUT AS CLOSE TO A MIRACLE AS YOU'LL GET IN MATHEMATICS.

and in *Solved Problems in Analysis [5]*, Orin J. Farrell did a similar integral like $I$,

$F_{1}(x)=\int_{0}^{\infty}e^{-x^2}dx$.

And again he used the polar coordinate transform. He then said "*Indeed, its discoverer was surely a person with great mathematical ingenuity.*" I concur. While the whole proof procedure is only using elementary calculus known by undergraduates. It takes quite a bit of imagination to come up with such method. It's easier for us to use the trick but the originator must be very smart.

I also think this is one of the key Calculus trick to learn if you want to learn more daunting distributions such as [gamma](https://en.wikipedia.org/wiki/Gamma_distribution), [beta](https://en.wikipedia.org/wiki/Beta_distribution) or [Dirichlet's distribution](https://en.wikipedia.org/wiki/Dirichlet_distribution). So let me give several quick notes on the proof above: 
1. You can use similar idea to prove the famous gamma and beta function are related as $\Gamma(a+b)=\Gamma(a)\Gamma(b)B(a,b)$. There are many proofs of this fundamental relationship between gamma and beta function. e.g. PRML[3] ex 2.6 outlines one way to a proof. But I found that first transforming the gamma function with $x=y^2$ and follow the above polar coordinate transformation trick is the easiest way to proof the relationship.
2. As mentioned before, the same proof can also be used in calculating $\Gamma(\frac{1}{2})$ (Also from [5]).
3. The polar coordinate trick is not the only way to calculate the probability integral. Look at note [6] on the history of its derivation.

Each of these points deserve a post on its own. So let's say I owe you some more posts.

References: [1] Paul J. Nahin, *Inside Interesting Integrals.*

[2] Alberto Leon-Garcia, *Probability and Random Processes for Electrical Engineering 2nd Edition.*

[3] Christopher M. Bishop, *Pattern Recognition and Machine Learning.*

[4] Paul J. Nahin, *Inside Interesting Integrals. p.4.*

[5] Orin J. Farrell and Bertram Ross, *Solved Problems in Analysis p.11.*

[6] Author Unknown, *The Probability Integral Link:* http://www.york.ac.uk/depts/maths/histstat/normal_history.pdf
