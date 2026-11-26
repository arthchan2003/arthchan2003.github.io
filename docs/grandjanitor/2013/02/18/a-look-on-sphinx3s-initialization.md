---
title: "A look on Sphinx3's initialization"
date: 2013-02-18
categories: ["kb", "kbcore", "pocketsphinx", "sphinx3", "Sphinx4"]
---

# A look on Sphinx3's initialization

I worked on [Sphinx 3 ](http://grandjanitor.blogspot.com/2012/05/development-of-sphinx-3x-x-6-to-8-and.html)a lot. In these days, it was generally regarded as an "old-style" recognizer as compared to Sphinx 4 and PocketSphinx. It is also not support officially by the SF's guys.

Coders of speech recognition think a little bit different. They usually stick to a certain codebase which they feel comfortable with. For me, it is not just a personal preference, it also reflects how much I know about a certain recognizer. For example, I know quite a bit of how Sphinx 3 performs. In these days, I tried to learn how Sphinx 4 fare as well. So far, if you ask me to choose an accurate recognizer, I will still probably choose Sphinx 3, not because the search technology is better (Sphinx 4 is way superior), but because it can easily made to support several advanced modeling types. This seems to be how the[2010 developer meeting concluded](http://cmusphinx.sourceforge.net/2010/03/development-meeting-notes/#more-157) as well. 

But that was just me. In fact, I am bullish on all Sphinx recognizers. One thing I want to note is the power of Sphinx 4 in development. There are many projects are based on Sphinx 4. In these days, if you want to get a job on speech recognizer, knowing Sphinx 4 is probably a good ticket. That's why I am quite keen on learning it more so hopefully I can write on both recognizers more. 

In any case, this is a Sphinx 3's article. I will probably write more on each components. Feel free to comments.  

#### How Sphinx3 is initialized:

Here is a listing of function used on how Sphinx 3 is initialized I got from Sphinx 3.0.8. Essentially, there are 3 layers of initialization, kb_init, kbcore_init and s3_am_init. Separating kb_init and kbcore_init probably starts very early in Sphinx 3. Whereas separating s3_am_init from kbcore_init was probably from me. (So all blames on me.) That is to support -hmmdir.

```
 kb_init  
     -> kbcore_init (*)  
     -> beam_init  
     -> pl_init  
     -> fe_init  
     -> feat_array  
     -> stat_init  
     -> adapt_am_init  
     -> set operation mode  
     -> srch_init  
 kbcore_init  
     -> Look for feat.params very early on.   
     -> logmath_init  
     -> feat_init  
     -> s3_am_init (*)  
     -> cmn_init  
     -> dict_init  
     -> misc. models init  
       mgau_init such as  
       -> subvq_init  
       -> gs_read  
     -> lmset_init  
     -> fillpen_init  
     -> dict2pid_build <- Should put into search  
 s3_am_init   
     -> read_lda  
     -> read in mdef.   
     -> depends on -senmgau type  
       .cont. mgau_init  
       .s2semi. s2_semi_mgau_init  
           if (-kdtree)  
           s2_semi_mgau_load_kdtree  
       .semi or .s3cont.   
           ms_mgau_init  
     -> tmat_init  
  
```

Note:

- \-hmmdir override all other sub-parameters.

Arthur
