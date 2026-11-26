---
title: "How to use Latex in WordPress?"
date: 2015-07-11
tags: ["latex", "wordpress"]
---

# How to use Latex in WordPress?

This is one of these small things it could take you a while to figure out. In your "Text" tab, what you want to do is type:

**$****latex your-latex-code-here$**

For example

**$****latex \\gamma$** would give you

$\gamma$.

So what could go wrong?

If you mistakenly put space in after the first dollar sign. e.g. **$[SPACE]****latex \\gamma$** 

Then you will get the latex code on the screen. (Argh.)

Her are some more complicated examples:

**$ latex \\int_0^1 f(x) \\, \\mathrm{d} x $** is

$\int_0^1 f(x) \, \mathrm{d} x$

And

**$ latex \\displaystyle \\sum\_{n=1}^\\infty \\frac{1}{n^2} = \\frac{\\pi^2}{6}. $** is

$\displaystyle \sum_{n=1}^\infty \frac{1}{n^2} = \frac{\pi^2}{6}.$

I think this is a useful thing to know because if you copy latex formula from the web it would take you a while to get it right and nice. 

Arthur
