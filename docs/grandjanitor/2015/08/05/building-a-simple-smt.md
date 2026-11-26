---
title: "Building a simple SMT"
date: 2015-08-05
categories: ["SMT"]
tags: ["Machine Learning", "SMT"]
---

# Building a simple SMT

I had couple of vacation days last week. For fun, I decided to train a statistical machine translator (SMT). Since I want to use tools from open source. The natural choice is Moses w GIZA++. So this note is how you can start smoothly. I don't plan to write a detail tutorial because Moses' tutorial is nice enough already. What I note here is more on how you should deal with different stumbling blocks. 

## Which Tutorial to Follow?

If you never run an SMT training before, perhaps the more solid way to start is to follow the ["Baseline System" link](http://www.statmt.org/moses/?n=Moses.Baseline) (a better name could be "How to train a baseline system"). At here, there is a rather detail tutorial on how to train a sets of models from WMT13 mini news commentary. 

## Compilation

I found that the most difficult part of the process is to compile moses. I don't blame anybody, C++ program can generally be difficult to compile. 

### Boost

Use source of boost, make sure libbz2 was first installed. Then life would be much easier. 

### cmph

While it is not mandatory, I would highly recommend you to install cmph first before compiling moses because compiling cmph would trigger compilation of file compressing tools such as *processPhraseTableMin* and *processLexicalTableMin*. Without them, it will take a long long time to do decoding. 

### Actual bjaming

Do ./bjam --with-boost=&lt;boost_dir&gt; --with-cmph=&lt;cmph_dir&gt; -j 4

works fairly well for me until I tried to compile the ./misc directory. That I found I need to manually add a path of boost to the compilation. 

## Training

Training is fairly trivial once you have moses compiled correctly and put everything in your root directory.

On the hand, if you compiled your code somewhere other than ~/, do expect some debugging is necessary. e.g. mert-moses.pl would require full path at the --merdir argument. 

## Results:

BLEU = 23.34, 60.1/29.7/16.7/9.9 (BP=1.000, ratio=1.018, hyp_len=76112, ref_len=7475) 

## Conclusion

Here you have it. Some notes on the simplest recipe for non-expert (like me). If I have a chance, I would analyze how the source code works. Again just for fun.

Arthur
