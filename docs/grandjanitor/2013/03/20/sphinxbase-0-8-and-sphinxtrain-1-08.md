---
title: "sphinxbase 0.8 and SphinxTrain 1.08"
date: 2013-03-20
categories: ["C++", "g2p", "sphinxbase", "sphinxtrain", "Thought"]
---

# sphinxbase 0.8 and SphinxTrain 1.08

I have done some analysis on sphinxbase0.8 and SphinxTrain 1.08 and try to understand if it is very different from sphinxbase0.7 and SphinxTrain1.0.7. I don't see big difference but it is still a good idea to upgrade.

- (sphinxbase) The bug in cmd_ln.c is a must fix. Basically the freeing was wrong for all ARG_STRING_LIST argument. So chances are you will get a crash when someone specify a wrong argument name and cmd_ln.c forces an exit. This will eventually lead to a cmd_ln_val_free.
- (sphinxbase) There were also couple of changes in fsg tools. Mostly I feel those are rewrites.
- (SphinxTrain) sphinxtrain, on the other hands, have new tools such as g2p framework. Those are mostly openfst-based tool. And it's worthwhile to put them into SphinxTrain.

One final note here: there is a tendency of CMUSphinx, in general, starts to turn to C++. C++ is something I love and hate. It could sometimes be nasty especially dealing with compilation. At the same time, using C to emulate OOP features is quite painful. So my hope is that we are using a subset of C++ which is robust across different compiler version. 

Arthur
