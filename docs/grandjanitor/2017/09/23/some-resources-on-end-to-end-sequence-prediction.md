---
title: "Some Resources on End-to-End Sequence Prediction"
date: 2017-09-23
---

# Some Resources on End-to-End Sequence Prediction

Important Papers: 
- [Connectionist Temporal Classification ](https://www.cs.toronto.edu/~graves/preprint.pdf)&lt;- the book 
        - But I found that Grave's [thesis](https://www.cs.toronto.edu/~graves/phd.pdf) is easier to follow. e.g. the definition of alpha and beta in the book doesn't make sense to me.
        - Few Alex Grave's papers. ([here](http://SPEECH%20RECOGNITION%20WITH%20DEEP%20RECURRENT%20NEURAL%20NETWORKS), [here](http://proceedings.mlr.press/v32/graves14.pdf), [here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.75.6306&rep=rep1&type=pdf))
        - [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](https://arxiv.org/pdf/1512.02595.pdf) Baidu's production system based on CTC
        - [Flat Start Training of CD-CTC-SMBR LSTM RNN Acoustic Models](http://www.mirlab.org/conference_papers/International_Conference/ICASSP%202016/pdfs/0005405.pdf)
        - Very good explanation on the Math by Andrew Gibiansky: http://andrew.gibiansky.com/blog/machine-learning/speech-recognition-neural-networks/
        - A comprehensive [explanation of CTC on distll](https://distill.pub/2017/ctc/).
- Attention-based seq2seq model: 
        - [END-TO-END ATTENTION-BASED LARGE VOCABULARY SPEECH RECOGNITION](https://arxiv.org/pdf/1508.04395.pdf)
        - Work from Bengio's group
- [Listen, Attend and Spell](https://arxiv.org/pdf/1508.01211.pdf) by William Chan ([his thesis](http://repository.cmu.edu/cgi/viewcontent.cgi?article=1762&context=dissertations))
- Very good presentation by [Markus Nussbaum-Thom](http://llcao.net/cu-deeplearning17/lecture/lecture6_Markus.pdf).

Unsorted: 
- [http://www.isca-speech.org/archive/Interspeech_2017/pdfs/0233.PDF](http://www.isca-speech.org/archive/Interspeech_2017/pdfs/0233.PDF)
- [https://arxiv.org/pdf/1707.07167.pdf](https://arxiv.org/pdf/1707.07167.pdf)
- Wav2letter: https://www.openreview.net/pdf?id=BkUDvt5gg
- http://publications.idiap.ch/downloads/papers/2017/Palaz_THESIS_2016.pdf
- http://ttic.uchicago.edu/~llu/pdf/liang_ttic_slides.pdf
- https://arxiv.org/pdf/1709.07814.pdf

Important Implementations: 
- EESEN: https://github.com/srvk/eesen
- Stanford-CTC: https://github.com/amaas/stanford-ctc
- Warp-CTC from Baidu: https://github.com/baidu-research/warp-ctc
- [Mozilla's implementation](https://github.com/mozilla/DeepSpeech)
- [Neon's implementation ](https://github.com/NervanaSystems/deepspeech)
- [Kaldi-ctc](https://github.com/lingochamp/kaldi-ctc/tree/master/egs/librispeech)
- https://github.com/zzw922cn/Automatic_Speech_Recognition

For reference, here are some papers on the hybrid approach: 
- [Acoustic Modeling using Deep Belief Networks](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.337.7548&rep=rep1&type=pdf)
- http://www.cs.toronto.edu/~asamir/papers/SPM_DNN_12.pdf
- [Good Kaldi tutorial](https://engineering.jhu.edu/clsp/wp-content/uploads/sites/75/2016/06/Building-Speech-Recognition-Systems-with-the-Kaldi-Toolkit.pdf).
