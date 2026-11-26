---
title: "A Read on \"Non-Autoregressive Neural Machine Translation\""
date: 2018-05-09
---

# A Read on "Non-Autoregressive Neural Machine Translation"

(First published at AIDL-LD and AIDL Weekly.)

This is the second of the two papers from Salesforce, " "Non-Autoregressive Neural Machine Translation" . Unlike the "Weighted Transformer, I don't believe it improves SOTA results. But then it introduces a cute idea into a purely attention-based NNMT, I would suggest you my previous post before you read on: [https://www.facebook.com/groups/aidl.ld/permalink/902138936617440/](https://www.facebook.com/groups/aidl.ld/permalink/902138936617440/)

Okay. The key idea introduced in the paper is fertility. So this is to address one of the issues introduced by a purely attention-based model introduced from "Attention is all you need". If you are doing translation, the translated word can 1) be expanded to multiple words, 2) transform to a totally different word location. 

In the older world of statistical machine translation, or what we called IBM models. The latter model is called "Model 2" which decide the "absolute alignment" of source/target language pair. The former is called fertility model or "Model 3". Of course, in the world of NNMT, these two models were thought to be obsolete. Why not just use RNN in the Encoder/Decoder structure to solve the problem?

(Btw, there are totally 5 layers in the original IBM Models. If you are into SMT, you should probably learn it up.)

But then in the world of purely attention-based NNMT, idea such as absolute alignment and fertility become important again. Because you don't have memory within your model. So in the original "Attention is all you need" paper, there is already the thought of "positional encoding".

So the new Salesforce paper actually introduce another layer which reintroduce fertility. Instead of just feeding the output of encoder directly into the decoder. It will feed to a fertility layer to decide if a certain word should have higher fertility first. e.g. a fertility of 2 means that it should be copied twice. 0 means the word shouldn't be copy.

I think the cute thing about the paper is two fold. One is that it is an obvious expansion of the whole idea of attention-based NNMT . Then there is the Socher's group is reintroducing classical SMT idea back to NNMT.

The result though is not working as well as the standard NNMT. As you can see in Table 1. There is still some degradation using the attention-based approach. That's perhaps why when the Google Research Blog mention the Salesforce results : it said "\*towards\* non-autoregressive translation". It implies that the results is not yet satisfying.
