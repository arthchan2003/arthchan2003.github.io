---
title: "Some Useful Links on Neural Machine Translation"
date: 2017-09-09
categories: ["attention", "deep learning", "deep neural network", "neural machine translation", "recurrent neural network"]
tags: ["attention", "DNN", "NNMT", "OpenNMT", "RNN"]
---

# Some Useful Links on Neural Machine Translation

Some good resources for NNMT

Tutorial: 
- [NMT tutorial written by Thang Luong](https://github.com/tensorflow/nmt?utm_campaign=Artificial%2BIntelligence%2Band%2BDeep%2BLearning%2BWeekly&utm_medium=web&utm_source=Artificial_Intelligence_and_Deep_Learning_Weekly_21) - my impression is that it is a shorter tutorial with step-by-step procedure. The part which is slightly disappointing is that it doesn't quite record exactly how the benchmarking experiments were run and evaluated. Of course, it's kind of trivial to fix it, but it did take me a bit of time.
- [The original Tensorflow seq2seq tutorial](https://www.tensorflow.org/tutorials/seq2seq) - more a big gun of SMT, the first experiment I played with. Now we are talking about the WMT15 set.
- [tf-seq2seq](https://google.github.io/seq2seq/nmt/) (blog post: [here](https://research.googleblog.com/2017/04/introducing-tf-seq2seq-open-source.html))
- [Graham Neubig's tutorial](https://arxiv.org/abs/1703.01619)
- [Nematus](https://github.com/EdinburghNLP/nematus)
- [OpenNMT](http://opennmt.net/) - this is PyTorch-based, if you are using OpenNMT-py with python 2.7, use a [patched version of mine](https://github.com/arthchan2003/OpenNMT-py)?
- [NeuralMonkey (Tensorflow-based)](https://github.com/ufal/neuralmonkey)
- [Prof. Philip Koehn's new chapter on NMT.](https://arxiv.org/abs/1709.07809) I also check out his "[6 Challenges in Neural Machine Translation](https://arxiv.org/abs/1706.03872)".

a bit special: [Tensor2Tensor](https://github.com/tensorflow/tensor2tensor) uses a novel architecture instead of pure RNN/CNN decoder/encoder. It gives a surprisingly large amount of gain. So it's likely that it will become a trend in NNMT in the future.

Important papers: 
- *Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation* by Cho Et al. ([link](http://emnlp2014.org/papers/pdf/EMNLP2014179.pdf)) - Very innovative and smart paper by Kyunghyun Cho. It also introduces GRU.
- *Sequence to Sequence Learning with Neural Networks* by Ilya Sutskever ([link](https://papers.nips.cc/paper/5346-sequence-to-sequence-learning-with-neural-networks.pdf)) - By Google's researchers, and perhaps it shows for the first time an NMT system is comparable to the traditional pipeline.
- *Google’s Neural Machine Translation System: Bridging the Gap between Human and Machine Translation* ([link](https://arxiv.org/pdf/1609.08144.pdf))
- **Neural Machine Translation by Joint Learning to Align and Translate by [Dzmitry Bahdanau](https://arxiv.org/find/cs/1/au:+Bahdanau_D/0/1/0/all/0/1) ([link](https://arxiv.org/abs/1409.0473)) -** The paper which introduce attention
- *Neural Machine Translation* by Min-Thuong Luong ([link](https://github.com/lmthang/thesis/blob/master/thesis.pdf))
- Effective Approaches to Attention-based Neural Machine Translation by Min-Thuong Luong ([link](https://arxiv.org/abs/1508.04025)) - On how to improve attention approach based on local attention.
- *Massive Exploration of Neural Machine Translation Architectures* by Britz et al ([link](https://arxiv.org/pdf/1703.03906.pdf))
- *Recurrent Convolutional Neural Networks for Discourse Compositionality* by Kalchbrenner and Blunsom ([link](https://arxiv.org/pdf/1306.3584.pdf))

Important Blog Posts/Web page: 
- [Attention and Augmented Recurrent Neural Networks](https://distill.pub/2016/augmented-rnns/): Only partially relevant to attention-based RNN, but Olah's writing is always worthwhile to read.
- [Stanford NMT research page](https://nlp.stanford.edu/projects/nmt/): Related to Luong, See and Manning's work on NMT. Very entertaining to look at recent techniques. Tutorial/code/models are available.
- If you are just curious about how the old IBM Models work, you should check out the old Bible of the field: Prof. Phillip Koehn's [Statistical Machine Translation](https://www.amazon.com/Statistical-Machine-Translation-Philipp-Koehn/dp/0521874157).

Summarization: 
- The more old-style summarization. You may take a look of [this survey](https://arxiv.org/pdf/1707.02268.pdf).
- Easy to read blog posts on NN-based summarization: [A Gentle Introduction to Text Summarization. ](https://machinelearningmastery.com/gentle-introduction-text-summarization/)
- Also [this from Pavel Surmerok](http://pavel.surmenok.com/2016/10/15/how-to-run-text-summarization-with-tensorflow/), which is fairly well-written.
- Papers: 
        - [A Neural Attention Model for Abstractive Sentence Summarization](https://arxiv.org/pdf/1509.00685.pdf)
        - [Get To The Point: Summarization with Pointer-Generator Networks](https://arxiv.org/abs/1704.04368)
- Resources I can't beat: 
        - [Awesome Text Summarization by icoxfog47](https://github.com/icoxfog417/awesome-text-summarization)
        - [Awesome Text Summarization by mathsyouth](https://github.com/mathsyouth/awesome-text-summarization) , especially under "Abstractive Text Summarization".

Usage in Dialogue System: 
- [An earlier paper (2015) ](https://arxiv.org/pdf/1510.03055.pdf)which discusses how to improve diversity of a generator.

Others: (Unsorted, and seems less important) 
- JayPark's Github [https://github.com/JayParks/tf-seq2seq](https://github.com/JayParks/tf-seq2seq)
- [https://github.com/ematvey/tensorflow-seq2seq-tutorials](https://github.com/ematvey/tensorflow-seq2seq-tutorials)
- [https://indico.io/blog/the-good-bad-ugly-of-tensorflow/](https://indico.io/blog/the-good-bad-ugly-of-tensorflow/)
- [https://www.reddit.com/r/MachineLearning/comments/43fw8s/simple_seq2seq_example_in_tensorflow/](https://www.reddit.com/r/MachineLearning/comments/43fw8s/simple_seq2seq_example_in_tensorflow/)
- [https://r2rt.com/recurrent-neural-networks-in-tensorflow-iii-variable-length-sequences.html](https://r2rt.com/recurrent-neural-networks-in-tensorflow-iii-variable-length-sequences.html)
- [http://forums.fast.ai/t/the-wonders-of-the-new-version-of-tensorflow-1-2rc0/3491](http://forums.fast.ai/t/the-wonders-of-the-new-version-of-tensorflow-1-2rc0/3491)
- [http://monik.in/a-noobs-guide-to-implementing-rnn-lstm-using-tensorflow/](http://monik.in/a-noobs-guide-to-implementing-rnn-lstm-using-tensorflow/)
- [http://suriyadeepan.github.io/2016-12-31-practical-seq2seq/](http://suriyadeepan.github.io/2016-12-31-practical-seq2seq/)
