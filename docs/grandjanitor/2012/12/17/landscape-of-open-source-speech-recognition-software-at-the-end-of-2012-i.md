---
title: "Landscape of Open Source Speech Recognition software at the end of 2012 (I)"
date: 2012-12-17
categories: ["HTK", "Julius", "Kaldi", "open source speech recognition", "Thought"]
---

# Landscape of Open Source Speech Recognition software at the end of 2012 (I)

As I am back, I start to visit all my old friends - all open source speech recognition toolkits. The usual suspects are still around. There are also many new kids in town so this is a good place to take a look. 

It was a good exercise for me, 5 years of not thinking about open source speech recognition is a bit long. It feels like I am getting in touch with my body again.

I will skip CMU Sphinx in this blog post as you probably know something about it if you are reading this blog. Sphinx is also quite a complicated projects so it is rather hard to describe entirely in one post. This post serves only as an overview. Most of the toolkit listed here have rich documentation. You will find much useful information there.

### HTK

I checked out the [Cambridge HTK web page](http://htk.eng.cam.ac.uk/docs/history.shtml). Disappointingly, the latest version is still 3.4.1, so we are still talking about MPE and MMIE, which is still great but not as exciting as other new kids in town such as KALDI. 

HTK has always been one of my top 3 speech recognition systems since most of my graduate work are done using HTK. There are also many tricks you can do with the tools. 

As a toolkit, I also find its software engineering practice admirable. For example, the software command was based on common libraries written beneath. (Earlier versions such as 1.5 or 2.1 would restrict access to the memory allocation library HMem.) When reading the source code, you feel much regularities and there doesn't seem to be much duplicated code. 

The license disallows commercial use but that's okay. With [ATK](http://mi.eng.cam.ac.uk/research/dialogue/atk_status.html), which is released in a freer license, you can also include the decoder code into a commercial application.

### [Kaldi](http://kaldi.sourceforge.net/index.html)

The new kid in town. It is headed by Dr. Dan Povey, who researched many advanced acoustic modeling techniques. His recognizers attract much interest as it has implemented features such as subspace GMM and FST-based speech recognizer. Of all, this features feel like more "modern". 

I only have little exposure on the toolkit (but determined to learn more). Unlike Sphinx and HTK, it is written in C++ instead of C. As of this writing, Kaldi's compilation takes a long time and the binaries are \*huge\*. In my setup, it took me around 5G of disc space to compile. It probably means I haven't setup correctly ...... or more likely, the executable is not stripped. That means working on Kaldi's source code actively would take some discretion in terms of HD. 

Another interesting part of Kaldi is that it is using weighted finite state transducer (WFST) as the unifying knowledge source representation. To contrast this, you may say most of the current open source speech recognizers are using **ad-hoc** knowledge source.**** 

**  
**

Are there any differences in terms of performance you ask? In my opinion, probably not much if you are doing an apple to apple comparison. The strength of using WFST is that when you need to introduce new knowledge, in theory you don't have to hack the recognizer. You just need to write your knowledge in an FST and compose it with your knowledge network, then you are all set. 

In reality, the WFST-based technology seems to still have practice problem. As the vocabulary size goes large and knowledge source got more complicated, the composed decoding WFST would naturally outgrow the system memory. As a result, many sites propose different technique to make decoding algorithm works. 

Those are downsides but the appeal of the technique should not be overlooked. That's why Kaldi becomes one of my favorite toolkits recently. 

### [Julius](http://julius.sourceforge.jp/en_index.php?q=index-en.html)

Julius is still around! And I am absolutely jubilant about it. Julius is a high-speed speech recognizer which can decode a 60k vocabulary. One speed-up techniques of Sphinx 3.X was context-independent phone Gaussian mixture model selection (CIGMMS) and I borrowed this idea from Julius when I first wrote. 

Julius is only the decoder and the beauty of it is that it never claims to be more than that. Accompanied with the software, there is a new Juliusbook, which is the guide on how to use the software. I think the documentation are in greater-depth than other similar documentations. 

Julius comes with a set of Japanese models, not English. This might be one of the reasons why it is not as popular (more like talk about) as HTK/Sphinx/Kaldi. 

(Note at 20130320: I later learned that Julius also comes with an English model now. In fact, some anecdotes suggest the system is more accurate than Sphinx 4 with broadcast news. I am not surprised. HTK was as acoustic model trainer.)

### So far......

I went through three of my favorite recognition toolkits. In the next post, I will cover several other toolkits available. 

Arthur

---

## Comments

**三十三博** (2012-12-24):

Glad to be in touch with you. Hope I can keep on.

Arthur

**Christophe Gerard** (2012-12-24):

Glad to be back in touch, and glad to hear about Open Source Speech Recognition

