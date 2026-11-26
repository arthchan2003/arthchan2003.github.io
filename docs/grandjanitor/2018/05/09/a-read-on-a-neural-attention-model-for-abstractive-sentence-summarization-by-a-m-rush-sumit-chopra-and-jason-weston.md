---
title: "A Read on \"A Neural Attention Model for Abstractive Sentence Summarization\" by A.M. Rush, Sumit Chopra and Jason Weston."
date: 2018-05-09
---

# A Read on "A Neural Attention Model for Abstractive Sentence Summarization" by A.M. Rush, Sumit Chopra and Jason Weston.

(First appeared in AIDL-LD and AIDL Weekly.)

This is a read on the paper "A Neural Attention Model for Abstractive Sentence Summarization" by A.M. Rush, Sumit Chopra and Jason Weston.

\* Video: [https://vimeo.com/159993537](https://l.facebook.com/l.php?u=https%3A%2F%2Fvimeo.com%2F159993537&h=ATNLDj8qKlLlY7_jUOqQX5RgPUebQwQEW-96IIXARpgyW-8VMAbfulAAe0x5YAgxDZm-FNGi50lNIpxagEK8ZNMnlYGzytIJx9_41aoyY6CaqQ_VOEiIwXq72Kig3FE2OB56_4QxZQwG6JHhWz7D1Gkm) . Github: [https://github.com/facebookarchive/NAMAS](https://github.com/facebookarchive/NAMAS)

\* The paper was written at 2015, and is more a classic paper on NN-based summarization. It is published slightly later than classic papers on NN-based translation such as those written by Cho or Badhanau. We assume you have some basic understanding on NN-based translation and attention.

\* There is a github ([https://github.com/facebookarchive/NAMAS](https://l.facebook.com/l.php?u=https%3A%2F%2Fgithub.com%2Ffacebookarchive%2FNAMAS&h=ATNiWnCHfAgcRoSEYqUoVFa8aVJanSKhbtqDLHAvnz3FmkNMnPf5Z2e74JYOKYiOe3SHgu4v_Xuonv0LJvPv58AGFCiNwk3v2rr3cwhz1ewXT7KuSR36vKrtF-ba_dUXVij8KAW-OXYf9Oz4ksAR6SBN)) and a video ([https://vimeo.com/159993537](https://l.facebook.com/l.php?u=https%3A%2F%2Fvimeo.com%2F159993537&h=ATNi6Sy_e-xqV72Htd58ujRTIiR1lyo8HblZyz-ZgNDkrwhhNiuqw7kKyveJuMRy-7TcwuX1R9p_RkR9CghiPnFsfkgkK8URKJpXPHZYEKXMtOHqBuPZv4Cu36bg583G8uns7UyIr2ueByQa6_ejy3TF)) for the paper.

\* If you haven't worked on summarization, you can broadly think of techniques as extractive or abstractive. Given the text you want to summarize, "extractive" means you just usehe word from the input text, whereas "abstractive" means you can use any words you like, even the words which are in the input text.

\* So this is why summarization is seen as similar problem as translation: you just think that there is a "translation" from the original text to the summary.

\* Section 2 is a fairly nice mathematical background of summarization. One thing to note, the video also bring up noisy channel formulation. But as Rush said, their paper is to completely do away noisy-channel but do direct mapping.

\* The next nuance you want to look at is the type of LM and the encoder used. That can all be found in Section 3. e.g. it uses the forward NNLM proposed by Bengio. Rush mentioned that he was trying RNNLM, but at that time, he get small gain. It feels like he can probably get better results if RNNLM is used.

\* Then it's the type of encoder, there is a nice comparison between bag-of-words and attention models. Since there are words embeddings, the "bag-of-words" is actually all the input words embedded down to a certain size. Attention model, on the other hand, is what we know today, which contains a weight matrix P which map the context to input.

\* Here is an insightful note from Rush: "Informally we can think of this model as simply replacing the uniform distribution in bag-of-words with a learned soft alignment, P, between the input and the summary."

\* Section 4 is more on decoding, in Section 2, Markov assumption was made, this simplifies the decoding quite a lot. The authors were using beam search, so you can use trick such as path combination.

\* Another cute thing is that the authors also comes up with method such that make the summarization more extractive. For that it uses a log-linear model to also weigh features such as unigram to trigram. See Section 5.

\* Why would the author wants to make the summarization more extractive? That probably has to do with the metric. ROUGE usually favors words which are extracted from the input text.

\* We will stop at this point. Here are several interesting commentaries about the paper.

mathyouth's: [https://github.com/mathsyouth/awesome-text-summarization](https://github.com/mathsyouth/awesome-text-summarization) Denny Britz': [https://github.com/…/neural-attention-model-for-abstractive…](https://github.com/dennybritz/deeplearning-papernotes/blob/master/notes/neural-attention-model-for-abstractive-sentence-summarization.md)

[https://arxiv.org/abs/1509.00685](https://arxiv.org/abs/1509.00685)
