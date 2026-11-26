---
title: "C++ vs C"
date: 2013-03-23
categories: ["C++"]
---

# C++ vs C

I have been mainly a C programmer. Because of work though, I have been working with many codebase which is written in C++. 

Many programmers will tell you C++ is a necessary evil. I agreed. Using C to emulate object oriented feature such as polymorphism, inheritance or even the idea of objects is not easy. It also easily confused novice programmer.

So why C++ frustrates many programmers then? I guess my major complaint is that its standard has be evolving and many compilers cannot catch up with the latest. 

For example, it's very hard for gcc 4.7 to compile code which can be compiled by gcc 4.2 . Chances are some of the language feature is outdated and they will generate compiler error.

On the other hand, C exhibit much greater stability across compiler. If you look at the C portion of the triplet (PocketSphinx, SphinxTrain, Sphinxbase), i.e. 99% of the code. Most of them just compile across different generation of gcc. This makes things easier to maintain.

Arthur
