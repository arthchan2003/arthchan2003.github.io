---
title: "Resources on Kaldi"
date: 2020-05-25
---

# Resources on Kaldi

## Introduction:

Kaldi is one of the three active open source ASR projects which is based on hybrid approach. It has perhaps the best feature sets, but it is seen to be more advanced as a toolkit. 

I like the toolkit because it works. Also ASR developers are colorful people (, sometimes too colorful), and I enjoy reading their source code.

(Yes, you need to read source code to understand kaldi.) 

## General Resources:

- [awesome-kaldi.](https://github.com/YoavRamon/awesome-kaldi) - Well-deserved to be called "awesome". Tons of useful links.
- this page.

## Basic Tutorials - the structure of kaldi, running from egs/ etc

Once a CMU professor told me that knowing how to use a hybrid ASR toolkits like htk, kaldi and sphinx are for really for bright kids. He is not wrong. All three toolkits require you to understand ASR enough to wield them effectively. Here are bunch of resources which you can help you. 
- [HTK Book](http://htk.eng.cam.ac.uk/) - We are talking about kaldi, why bring up HTK then? Well, kaldi was a response to htk. Both were written as unix command-line tools. Comparing kaldi with htk, htk was developed as a company codebase (Entropic). So the code is thought as more refined, but harder to change. Looking at both toolkit now (2020), I still find that the HTK tutorial is easier to follow.
- [The original kaldi tutorial ](https://kaldi-asr.org/doc/tutorial.html)- it uses RM, so if you don't have RM, nah, this is not going to help you run end-to-end. But it will teach you basics of the resources.
- [The original ICASSP 2011 lecture](https://www.superlectures.com/icassp2011/downloadFile.php?id=184&type=slides&filename=running-the-example-scripts).
- [Eleanor Chodroff's tutorial](https://eleanorchodroff.com/tutorial/intro.html) - Rare wordy explanation of the toolkits. With some decent notes on what #senones really means.
- [Qianhui Wan's runthrough of stages in a kaldi training](https://medium.com/@qianhwan) - Good high-level run through of kaldi's script.

## More advanced topics:

- First, a survival note. For the most part, working with Kaldi means you work with Unix and sometimes dive deep into its C++/C level code. You would get crushed if you expect "tensorflow-style" of problem solving.
- [HBKA](https://cs.nyu.edu/~mohri/pub/hbka.pdf) - WFST is one of the cores of a kaldi-based ASR system. But it's also rather hard to grok. These days, HBKA is seen as the Bible of learning WFST. The key algorithms in WFST are determinization and minimization. Well, they are actually variants of the FST. (In the case of minimization, you just use the FST version to minimize.) So to understand what you are doing, you also want to have the basics of some classic FST algorithms. So a computational complexity book is very useful too. (I use Hopcraft and Ullman) .
- If you want to dig deeper, several papers which contain the detail algorithms (and proofs) of determinization and minimization. are [here](https://www.aclweb.org/anthology/J97-2003.pdf) and [here. ](https://www.sciencedirect.com/science/article/pii/S0304397598001157) If HBKA is the Bible, these papers might be the Words. :)
- Other more wordy tutorials on WFST: [Vassil Panayotov's](http://vpanayotov.blogspot.com/2012/06/kaldi-decoding-graph-construction.html) [Josh Meyer's ](http://jrmeyer.github.io/asr/2016/02/01/Kaldi-notes.html)
- Btw, talking about internals of WFST these days i seen as "advanced" topics. Most people are using TF/Pytorch. So revolutionary technologies such as WFST were forgotten.

## When you need to hack kaldi......

- Changing source code of kaldi, or in general, open source speech recognizers, is not the worst thing happen to a hacker. For the most part, you can derive most information by reading the source code. There are modules which are terse . e.g. nnet3. Say if you want to add a new computation command, then you want to go through several classes to make it works. On the same vein, you don't really see any description of how individual command works. Think of it as assembly code to C, you will need to work it through yourself.
- The good news is ...... it's possible. As always, you just need some coffee and a comfortable chair.
- What if you want to read some documentation then? Then go with https://kaldi-asr.org/doc/index.html. You will be able to read high-level understanding of some algorithms.
- I never work with Dr. Povey. But I often think his code and description are terse. i.e. He certainly know what he is doing, and many critics just don't miss his points, but you need to be experienced in ASR to understand some of his "moves".
- Also see the next section on specific questions you may ask about Kaldi.

## Questions you will ask when using Kaldi

- Many data structures in kaldi are not "*created with human readability as the first priority*". (I chucked when I read this phrase from Kaldi doc. :) ) ** But then users often convinced Povey to come up with a terse yet readable description.
- **Tree-related:** How does the decision tree look like? Check out copytree. How does decision tree work in kaldi? Oh you better learn what [Event Maps](http://kaldi-asr.org/doc/tree_internals.html) is. The link also brings you to what the [internal of decision tree building](http://kaldi-asr.org/doc/tree_internals.html) looks like. A more high-level description can be found at [here](http://kaldi-asr.org/doc/tree_externals.html).
- **Transition ID:**  What is transition ID? Two important answers: it is a 5-tuples including the identity of transitions, source, forward and self-loop transID and the phone. It is also an ID which the minimal description of a compiled decoding graph. See [here. ](http://kaldi-asr.org/doc/hmm.html)
- **Lattice-related**: [here](http://kaldi-asr.org/doc/lattices.html). Also lattice-copy is your friends.
- **nnet3-related**: How does neural network computation work? How was an NN compiled? What optimization was used on the NN? Actually, what are the optimizations? If you feel confused about this question, check out all nnet3 links from the "[nnet3 setup](http://kaldi-asr.org/doc/dnn3.html)" page.
- **Example generation for NN training:** That... if you never "read between the pipes", you will never understand. Various Chinese hackers have analyze the chain though. You can easily look it up on Google.

Acknowledgement

You always want to thank Dan Povey and the kaldi team for their great work. Hybrid approach is not going away soon because of them.

Update Logs:

(Sep 7, 2020) Add notes on interesting topics such as tree, transition ID and neural network computation. (Before Sep 7, 2020) Wrote the backbone of the note.
