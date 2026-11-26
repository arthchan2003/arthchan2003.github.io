---
title: "Learning ASR Through Coding"
date: 2013-11-17
categories: ["ASR"]
tags: ["DNN", "HTK", "Kaldi", "SGMM", "Sphinx", "WFST"]
---

# Learning ASR Through Coding

In a way, speech recognition is not that different from many skills. You need to have a lot of practice to really grasp how certain things can be done. e.g. if you never write a Viterbi algorithm, it's probably hard for you to convince anybody you know the search aspect of ASR. And if you never write an estimation algorithm, then your knowledge in training would be shaky.

Of course, this might be too hard for many people. Who will have time to write a decoder or a trainer? Fair enough. I guess the next best choice is to study implementations of open source speech recognizers, try to modify them to fit your goal. In the process, you will start to build up understanding. 

## Which recognizers?

Let me say one thing for learners these days: *you guys are lucky*. When I tried to learn to do any ASR coding back in 2000, you have to join a certain speech lab, get a license of HTK before you can do any tracing and modification. Now you have many choices, HTK, Sphinx, Kaldi, Julius, RWTH recognizer, etc..... So what will be the recognizers you should learn?

I will name three of them, HTK, Sphinx and Kaldi. Why? 

### Why HTK?

You want to learn HTK because it has a well-designed and coherent interface. It also has some of the best of training technology: its ML training is assumption free and take care of small issues such as silence/short-pauses, multiple pronunciations. It has one of the sort large vocabulary MMIE training. All of these work are very nice.

HTK also has a well-written tutorial. If you own either the TIMIT or the RM corpora, you can usually train the whole thing following through the instruction. While going through the tutorial, you gain valuable understanding on data structures commonly used in speech recognition.

Though I mainly worked on Sphinx, there were around 2-3 years of life I used HTK in a day-to-day basis. The menu itself is a good literature that can teach you a lot of things. I believe many designers of speech recognizers actually learn from HTK source code as well. 

### Why Sphinx?

"Because you work on Sphinx!" True, I am biased in this case. But I do have a legitimate reason to like Sphinx and claim that knowledge of Sphinx is more useful.

If you compare the history of HTK and Sphinx systems development, you will notice that HTK's very nice interface stemmed from design effort in Entropic stage. Whereas Sphinx as whole are more work from PhD students, faculties and staffs. In another words, Sphinx tools are more "hacky" than HTK. So as a project, you will find that Sphinx seems to be more incoherent. e.g. there are many recognizers written in C or Java. The system itself seems to require much learning curves.

Very true, those are weaknesses. But one thing I like about Sphinx is that it is fertile ground for any enthusiasts to play with. The free BSD license gives people are chance to incorporate any part of the code into their projects. As a result, historically, there are many companies which are using Sphinx in their company code.

Before we go, you may ask "Which Sphinx?" If you ask 5 guys from the CMU Sphinx project, they will give you 5 different answers. But let me just offer my point of view, which I think more related to learning. Nick, the current maintainer-at-large, and I once chat, he believed that current Sphinx project should only support triple: Sphinx4/pocketsphinx/SphinxTrain. I support that view. As a project, we should only support and maintain focused number of components.

Though if you are enthusiasts, I will highly recommend you to study more. Other than the triple, you will find Sphinx2 and Sphinx3 have their own interesting parts. Not all of them is transferred to Sphinx4 or pocketsphinx. But they are nonetheless fun code to read. e.g. how triphones were implemented in different sphinx? With all computation these days, I don't full triphone expansion works for real-time system. I believe in that aspect, 2 and 3 are very interesting. 

### Why Kaldi?

I am very excited about Kaldi. You can think of it as the "new HTK with the Sphinx license". The technology is strong and new. e.g. there is a branch which has all deep-neural network-based training. The recognizer is based on WFST. The best, all components are in very liberal licenses. So you can surely do many amazing things with it.

The only reason why I don't recommend it more is that it is still relatively new. Open source toolkits have strange lives : if they are being supported by funding, they can live forever. If they are not, their fate is quite unpredictable. Say MITLM toolkit, there were a year or so the maintainer left and there was no new maintainer. I am sure during the time users will need to patch a thing or two. It is certainly a very interesting toolkit. (Because automatic optimization of mKN smoothing weight.) But sometimes it's hard to predict what will happen.

In a way, development of Kaldi is rare, someone decides to share the best technology in our time to everybody. (WFST, SGMM, DNN are all examples.) I can only wish the project goes on. If I could, may be I want to contribute a thing or two.

Arthur

---

## Comments

**Yuchen Zhang** (2013-11-17):

Hi Arthur,

I liked your post a lot. Could you comment on which of the part of ASR do you think is easier to get hands dirty with those engines? (Like search, lattice generation, LM ... ) I've been running experiments and modifying pipelines, and even wrote a simple HMM-GMM based ASR myself, but I've never hacked a fully developed ASR before.

Thanks! Yuchen

> **grandjanitor** (2013-11-18):
>
> Hey Yuchen,
>
> Those are good questions. If you want simple ones, I would say alternative GMM computation could be a starting point. e.g. there are machine learning techniques these days which purportedly outperform GMM (e.g. DNN). You will find it very illuminating to train different machine learners and try to apply them into GMM computation. (Note: watch out what you are classifying!)
>
> Many people also found that rescoring on either the lattices or N-best are pretty simple to do. That's true too. But generally you will find both of these resources as the output stage of the decoder. So you end up not able to gain too much insight of what's going on with a decoder.
>
> A more difficult project would be to use different underlying data structure to implement Viterbi: graph, lexical trees. Those are usually tougher because debugging a search usually require more difficult techniques. e.g. You need to understand the dynamic search enough. If you are using gdb, you will find that putting the right breakpoint to debug a problem is closed to an art.
>
> Hope this help.
>
> Arthur

> > **Yuchen** (2013-11-19):
> >
> > Thank you for the advice Arthur! I'll try experimenting with the easier stuff : )

> > > **grandjanitor** (2013-11-19):
> > >
> > > You are welcomed!

