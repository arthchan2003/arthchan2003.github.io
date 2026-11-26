---
title: "Sphinx 4 from a C background : Material for Learning Sphinx 4"
date: 2013-01-10
categories: ["3.5", "3.7", "C++", "java", "sphinx 3.X", "Sphinx 4", "Sphinx 4 from C background", "tutorial"]
---

# Sphinx 4 from a C background : Material for Learning Sphinx 4

I have been quite focused on SphinxTrain lately. So I haven't touched Sphinx 4 for a while. As I have one afternoon which I can use with leisure (not really), so I decide to take a look of some basic material again. 

Sphinx-4, as a recognizer, is interesting piece software to me, a recovering recognizer programmer. It seems remote but oddly familiar. It is sort of a dream-land for experimenting different decoding strategies. During Sphinx 3.5 to 3.7, I tried to make Sphinx 3.X to be more generalized in terms of search. Those effort was tough mainly because the programs were in C. As you might guess, those modification requires much reinvention of a lot of good software engineering mechanisms (such as class).

Sphinx-4 is now widely studied. There are many projects using Sphinx-4 and its architecture is analyzed in many sites. That's why I have abundant amount of material to learn the recognizer. (Yay! :) )

Here are the top 5 pages in my radar now and I am going to study them in detail:

1. [Introduction](http://cmusphinx.sourceforge.net/sphinx4/index.html#whitepaper) : What Sphinx-4 is? And how to use it.
2. [Sphinx 4 Application Programmer Guide](http://cmusphinx.sourceforge.net/wiki/tutorialsphinx4) : What excites me is model switching capability. I also love the way the current recognizer can be linked to multiple languages.
3. [Configuration Manager](http://cmusphinx.sourceforge.net/sphinx4/javadoc/edu/cmu/sphinx/util/props/doc-files/ConfigurationManagement.html) : That's an interesting part as well. That is a recognizer which is configurable for every components. Is it a good thing? There are pros and cons about a hierarchical configuration system. But for most of the time, I think that's a better way than flat command-line structure.
4. [Instrumentation](http://cmusphinx.sourceforge.net/sphinx4/javadoc/edu/cmu/sphinx/instrumentation/doc-files/Instrumentation.html) : How to test the decoder with examples on TIDIGITS and many more database.
5. [FAQ](http://cmusphinx.sourceforge.net/sphinx4/doc/Sphinx4-faq.html): Here is a list of questions which make me curious.
6. [The White Paper](http://cmusphinx.sourceforge.net/sphinx4/doc/Sphinx4Whitepaper.pdf) : Extremely illuminating, I also appreciate the scholarship when they compare different versions of Sphinxes.
7. The 2003 paper: I haven't gone through this one yet but it's certainly something I want to check out.

Arthur

Previous related articles:  
[Sphinx4 from a C background : first few steps](http://grandjanitor.blogspot.com/2012/12/sphinx4-from-c-background-first-few.html)  
[Sphinx4 from a C background : Installation of Eclipse](http://grandjanitor.blogspot.com/2012/12/sphinx4-from-c-background-installation.html)  
[Sphinx4 from a C Background : Setting up Eclipse ](http://grandjanitor.blogspot.com/2012/12/sphinx-4-from-c-background-setting-up.html)

---

## Comments

**Mauricio Pessoa** (2017-07-24):

Thanks a lot for the reply! I will take a look at it for sure :) Do you have any reference on books, papers, or any other material I should get to start? (Not only with sphinx, but with SR in general)

**Mauricio Pessoa** (2017-07-20):

Man, this is really going to help me. I'm doing some research for my master degree and I'll probably use sphinx to solve my problem. Thing is, I'm a novice on speech recognition, and I got caught on this "by surprise". But I'm excited with it. I want to learn it, and I'd like to thank you for your articles. I'd also like to ask for a little help. Any reference material on it would be extremely helpful. Can you mail me?

> **grandjanitor** (2017-07-23):
>
> Ah. I haven't worked on cmusphinx for a while. But the cmusphinx sourceforge forum should be very relevant to you. Would you check it out? Thanks!

