---
title: "A read on \" Unsupervised Machine Translation Using Monolingual Corpora Only\""
date: 2018-05-09
---

# A read on " Unsupervised Machine Translation Using Monolingual Corpora Only"

(First published on AIDL-LD and AIDL Weekly.)

"This is an impressive paper by FAIR authors which claims that one only need to use monolingual corpora to train a usable translation model. So how does it work? Here are some notes.

\* For starter, indeed you don't need to use a parallel corpora, but you still need a bidirectional dictionary to generate translation. You also need to have monolingual corpora in both languages. That's why the title is about monolingual corpora (plural) but not monolingual corpus (singular). 

\* Then, there is the issue of how you actually create translation. It's actually much simpler than you thought, first imagine there is a latent language which both your source and target languages mapped to.

\* How do you train? So let's just use the source language as an example first. What you can do is create an encoder-decoder architecture which translate your source to the latent space, then translate it back. Using BLEU score, you can then setup an optimization criteria.

\* Now this doesn't quite do the translation. Now you apply the same procedure on both source and target language. Don't you now have a common latent space? In actual translation, what you need to do is to first map the target language in the common latent space, then map it back to the source language.

\* Many of you might recognize that such encoder-decoder scheme which map the language to itself as very similar to autoencoder. Indeed, the authors in the paper actually use a version of autoencoder: denoising autoencoder(dA) to train the model.

\* The final interesting idea I spot is to idea of iterative training. In this case, you can imagine that you can first train an initial translator, but then use its output as the truth and retrain another one. The authors found tremendous gain in BLEU score in the process.

\* The results are stunning if you consider no parallel corpus is involved. BLEU score is around 10 points lower, but do remember: deep learning has pretty much improved BLEU scores by absolute 7-8 points anyway from the classical phrased based translation models."
