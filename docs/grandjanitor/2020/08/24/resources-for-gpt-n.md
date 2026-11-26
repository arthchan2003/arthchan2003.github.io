---
title: "Resources for GPT-N"
date: 2020-08-24
categories: ["deep leaerning"]
tags: ["deep learning", "GPT-3"]
---

# Resources for GPT-N

Official papers/blogs 
- GPT-1: ([blog post](https://openai.com/blog/language-unsupervised/)) paper: [Improving Language Understanding by Generative Pretraining - ](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)
- GPT-2: ([blog post](https://openai.com/blog/better-language-models/)) paper: [Language Models are Unsupervised Learners](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
- GPT-3: ([API and blog post](https://openai.com/blog/openai-api/)) paper: [Language Models are Few-Shot Learners](https://arxiv.org/abs/2005.14165)
- An important paper on the bigger context of GPT-N : How CE loss scales with model size? "[Scaling Laws of Neural Language Mode](https://arxiv.org/pdf/2001.08361.pdf)l"
- Image-GPT: ([blog post](https://openai.com/blog/image-gpt/)) paper: [Generative Pretraining from Pixels](https://cdn.openai.com/papers/Generative_Pretraining_from_Pixels_V1_ICML.pdf)

While I am quite aware of the technology back at GPT-1, I started writing this blog post at the time of GPT-3. So I will focus on GPT-3 and image GPT, which you may think they are the iteration which fascinate the public most. But I will also dovetail back to GPT-1/2 on technical reference. 

### Resources on GPT-3

- [Top 10 demo](https://machinelearningtokyo.com/2020/07/26/10-cool-gpt-3-demos/) curated by [Suzana Ilić](https://twitter.com/suzatweet).
- [Awesome GPT-3 ](https://github.com/elyase/awesome-gpt3)
- [Excellent discussion on GPT-3+ extensive experiments on poetry/essay generation](https://www.gwern.net/GPT-3) from Gwern Branwen
- [Another excellent discussion on GPT-3, focusing on GPT-3 addition capability ](https://slatestarcodex.com/2020/06/10/the-obligatory-gpt-3-post/)
- [Another one](https://nostalgebraist.tumblr.com/post/619511470655504384/the-gpt-3-paper-cites-another-recent-jan-2020).
- Some notes on the original paper: 
        - **It works on various NLP tasks**: "*For example, GPT-3 achieves 81.5 F1 on CoQA in the zero-shot setting, 84.0 F1 on CoQA in the one-shot setting, 85.0 F1 in the few-shot setting. Similarly, GPT-3 achieves 64.3% accuracy on TriviaQA in the zero-shot setting, 68.0% in the one-shot setting, and 71.2% in the few-shot setting, the last of which is state-of-the-art relative to fine-tuned models operating in the same closed-book setting.*"
        - **Surprisingly, GPT-3 excels at several few-shot learning tasks**: (p.5) "*GPT-3 also displays one-shot and few-shot proficiency at tasks designed to test rapid adaption or on-the-fly reasoning, which include unscrambling words, performing arithmetic, and using novel words in a sentence after seeing them defined only once. We also show that in the few-shot setting, GPT-3 can generate synthetic news articles which human evaluators have difficulty distinguishing from human-generated articles."*
        - **Unsurprisingly, GPT-3 struggle in several tasks in few-shot learning tasks**: (p.5 same paragraph as above) "*At the same time, we also find some tasks on which few-shot performance struggles, even at the scale of GPT-3. This includes natural language inference tasks like the ANLI dataset, and some reading comprehension datasets like RACE or QuAC*."
        - **But data contamination issue is real**: "We also undertake a systematic study of “data contamination” – a growing problem when training high capacity models on datasets such as Common Crawl, which can potentially include content from test datasets simply because such content often exists on the web. In this paper we develop systematic tools to measure data contamination and quantify its distorting effects"
- Performance on individual tasks: 
        - Few-shot learning allows OpenGPT-3 to do NMT, (p.14) it beats the best unsupervised learning SOTA.
        - With few-shot learning, it beats the SOTA of PIQA.
        - [TBD]

## Training:

- [GPT2: Karparthay's GPT training mostly on images. ](https://github.com/karpathy/minGPT/blob/master/play_image.ipynb)
- [GPT2: Coursera Guided Task](https://www.coursera.org/projects/deep-learning-nlp-gpt-2)

## Interesting links:

- https://transformer.huggingface.co/
- [Speech-based GPT-2 for speaker recognition](https://arxiv.org/abs/2007.00659)
