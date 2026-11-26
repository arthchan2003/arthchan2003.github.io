---
title: "Sphinx 3.6 is officially released"
date: 2006-06-16
---

# Sphinx 3.6 is officially released

Sphinx 3.6 Official Release   
^^^^^^^^^^^^^^^^^^^^^^^^^^^ 

Sphinx 3.6 official release included all changes one found in Sphinx 3.6 RC I. 

From 3.6 RC I to 3.6 official: 

New Features:   
\-Added support for sphinx 2-style semi-continuous HMM in Sphinx 3.   
\-Added sphinx3_continuous which performs on-line decoding in both windows and linux platforms.   
\-Synchronized the frontend with Sphinx2, adding implementation of VTLN. (i.e. -warp_type = inverse_linear, piewise_linear, affine) 

Changes:   
\-Prefix "sphinx3\_" has been added to programs align, allphone, astar, dag, decode, decode_anytopo, ep to avoid confusion in some unix systems. 

For Developers:   
\-All public headers (\*.h) are now put under $root/include instead of the same directories as their source .c file.   
\-The directory name libutil is now changed to libs3util   
\-Sphinx3, as well as all other modules in the CMU Sphinx   
project, is now versioned by Subversion. 

Bug Fixes:   
\-[1459402] Serious memory relocation is fixed.   
\-In RCI, -dither was not properly implemented, this has been fixed. 

Known Problem:   
\-When the model contains nan, there will be abnormal output of the result. At this point, this issue is resolved in SphinxTrain 

Sphinx 3.6 Release Candidate I   
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^   
The corresponding SphinxTrain's tag is SPHINX3_6_CMU_INTERNAL_RELEASE   
One can check out the matching SphinxTrain of the sphinx3.6 release by command,   
svn co https://svn.sourceforge.net/svnroot/cmusphinx/tags/SPHINX3_6_CMU_INTERNAL_RELEASE/SphinxTrain 

A Summary of Sphinx 3.6 RC I   
\---------------------------- 

Sphinx 3.6 is a gently refactored version of Sphinx 3.5. Our programming is defensive and we only aim at further consolidation and unification our code-bases in Sphinx 3. 

Despite our programming is defensive, there are still several interesting and new features could be found in this   
release. Their details could be found in the "New Feature"   
section below. Here is a brief summary: 

1, Further speed-up of CIGMMS in the 4 level GMM Computation Schemes (4LGC)   
2, Multiple regression classes an MAP adaptation in SphinxTrain   
3, Better support in using LM in Sphinx 3.X.   
4, FSG search is now supported. This is adapted from Sphinx 2.   
5, Support of full triphone search in flat lexicon search.   
6, Some support of different character sets other than of   
Sphinx 3.X. Models in multiple languages are now tested in   
Sphinx 3.X. 

We hope you enjoy this release candidate. In future, we will   
continue to improve the quality of CMU Sphinx and CMU Sphinx's related software. 

New Features   
\------------   
\-Speaker Adaptation:   
a, Multiple regression class (phoneme-based) is now supported. 

\-GMM Computation   
a, Improvements of CIGMMs is now incorporated.   
i, One could specify the upper limit of the number of CD   
senones to be computed in each frame by specifying -maxcdsenpf.   
ii, The best Gaussian index (BGI) are not stored and could   
be used as a mechanism to speed up GMM computation   
iii, tightening-factor (-tighten_factor) is introduced to   
smooth between fix naive down-sampling technique and CI-GMMS.   
b, Support of SCHMM and FCHMM   
i, decode will fully support computation of SCHMM. 

\-Language Model   
a, reading an LM in ARPA text format is now supported. Users now have an option to by-pass the use of lm3g2dmp.   
b, live decoding API now supports switching of language models.   
c, full support of class-based LM. See also the Bug fixes section   
d, lm_convert is introduced. lm_convert supersede the functionalities of lm3g2dmp. Not only could lm_convert convert an LM from TXT format to DMP format. It could also do the reverse. 

\-Search   
This part will detail the change we make in different search   
algorithms.   
In 3.6, collection of algorithms could all be used under a   
single executable decode. decode_anytopo is still reserved   
for backward compatibility purpose.   
Decode now support three modes of search.   
Mode 2 (FSG): (Adapted from Sphinx 2) FSG search.   
Mode 3 (FLAT): Flat-lexicon search. (The original search in decode_anytopo in 3.X (X &lt; 6))   
Mode 4 (TREE): Tree-lexicion search. (The original search in decode in 3.X (x&lt;6) 

Some of these functionalities will only be applicable in one   
particular search. We will mark them with FSG, FLAT and TREE. 

a, One could now turn off -bt_wsil to control whether silence should be used as the ending word. (FLAT, TREE)   
b, In FLAT, full triphones could be used instead of   
multiplexed triphones.   
c, FSG is a new added routine in 3.6 which is adapted from   
Sphinx 2.5 

\-Frontend   
a, -dither is now supported in live_pretend and   
live_decode, the initial seed could always be set the command   
\-seed. (Jerry Wolf will be very happy about this feature.) 

\-Miscellaneous   
a, One could turn on built-in letter-to-sound rule in dict.c by using -lts_mismatch.   
b, current Sphinx 3.6 is tested to work on setup of English,   
Chinese Mandarin, French and English.   
c, changes in allphone: allphone can now generate a match and a matchseg just like decode\* recognizers. 

Bug fixes   
\---------   
\-Miscellaneous memory leak fixed in the tree search (mode 4)   
\-Initialization class-based LM routine use to switch the order of   
word insertion penalty and language model weight. This is now fixed.   
\-Assertion generated vithist.c is now turn into an error   
message. Instead of causing the whole program stopped. The decoding will just fail for that sentnece. We suspect that this is the problem which caused possible wipe out of memory in Sphinx   
3\.4 & 3.5   
\-Number of CI phones could now be at most 32767 (instead of 127)   
\-[1236322]: libutilstr2words special character bugs. 

Behavior Changes   
\----------------   
\-Endpointer (ep) now used computation of s3 log. 

\-Multi-stream GMM computation will not truncate the pdf to 8 bit anymore. This will avoid confusion of programmer. However 

\-Except in allphone and align, When .cont. is used in   
\-senmgau, the code will automatically turn to use fast GMM computation routine. To make sure the multiple-stream GMM computation will be in effect, one need to specify .s3cont. 

\-executable dag hadn't accounted for the language weight. Now this issue is fixed. 

\-(See Bug fixes also) decode will now return error message   
when vithist was fed in with history -1. Instead of asserting the problem. The recognizer will dump Warning message. Usually that means beam widths need to increase. 

Functions still under test   
\-----------------------------------------   
\-Encoding conversion in lm_convert.   
\-LIUM contribution: LM could now represented as AT&T fsm format. 

Known bugs   
\------------------------------------------   
\-Confidence estimation, the computations of forward and   
backward posterior probability have mismatch   
\-In allphone, sometimes the scores generated in the matchseg file will have very low scores.   
\-Regression test on second-stage search still have bugs. 

Corresponding changes in SphinxTrain   
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^   
Please note that SphinxTrain is distributed as a separate package and you can get it by:   
svn co https://svn.sourceforge.net/svnroot/cmusphinx/tags/SPHINX3_6_CMU_INTERNAL_RELEASE/SphinxTrain 

\-Support for generation of MAP, multiple-class MLLR.   
\-Support for BBI tree generation
