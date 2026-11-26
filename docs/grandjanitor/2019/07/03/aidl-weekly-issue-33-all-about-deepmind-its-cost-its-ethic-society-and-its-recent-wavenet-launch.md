---
title: "AIDL Weekly Issue 33 - All About DeepMind - Its Cost, Its Ethic Society and Its Recent Wavenet Launch"
date: 2019-07-03
---

# AIDL Weekly Issue 33 - All About DeepMind - Its Cost, Its Ethic Society and Its Recent Wavenet Launch

## Editorial

### Thoughts From Your Humble Curators

We learnt more about DeepMind last week - we learn the hefty price to run it and its struggle to correct its image since the debacle of DeepMind Health-Royal Free event. But we also learnt that our beloved Wavenet is now in production within Google Assistant, and it's whopping 1000 times faster. This week, we'll cover DeepMind more in-depth. 

We also have an issue filled with contents: "Confession of AI researchers" is our favorite link. We answer our member question on how to come up with new AI idea in "Questions from Members". And we dive into an interesting paper: "Unsupervised Hypernym Detection by Distributional Inclusion Vector Embedding" by Haw-Shiuan et al.

---

As always, if you like our newsletter, feel free to subscribe and forward it to friends!

Artificial Intelligence and Deep Learning Weekly

## News

### [How Much Does DeepMind Cost?](https://qz.com/1095833/how-much-googles-deepmind-ai-research-costs-goog/)

As it turns out: it lost ~$162 million last year. It makes around $40 million, but mostly work for its parent company Alphabet. 

[qz.com](https://qz.com/1095833/how-much-googles-deepmind-ai-research-costs-goog/)

---

### [DeepMind Ethics & Society](https://www.theguardian.com/technology/2017/oct/04/google-deepmind-ai-artificial-intelligence-ethics-group-problems)

This Guardian piece is perhaps the best at describing the new DeepMind Ethics & Society. At first, we thought that this is repurposing the older DeepMind Health [advisor panel](https://deepmind.com/blog/independent-reviewers-annual-report-2017/) but then the piece clearly stated that it is a separate society. 

This move is in response to the previous year debacle of DeepMind on how to treat patient data. As we reported in [Issue #20](http://aidl.io/issues/20#start), an independent commissioner commented on the how DeepMind inappropriately treat patient data: "Just that you can, doesn't mean that you should." The whole event also cost 5 times the legal fee for DeepMind than previous year (see the previous piece on "How Much Does DeepMind Cost?").

[theguardian.com](https://www.theguardian.com/technology/2017/oct/04/google-deepmind-ai-artificial-intelligence-ethics-group-problems)

## Blog Posts

### [DeepMind Launches Wavenet In Google Assistant. ](https://deepmind.com/blog/wavenet-launches-google-assistant/)

DeepMind launching Wavenet in production system is perhaps one of the most exciting news last week. What is amazing - it's **1000** times faster than [one-year-old version](original%20WaveNet%20blog%20post) and it can run on a TPU. The speed up doesn't seem lossy - MOS around ~4.35 which human voice is not too far away: 4.67. 

[deepmind.com](https://deepmind.com/blog/wavenet-launches-google-assistant/)

---

### [Confession as an AI researcher; seeking advice](https://www.reddit.com/r/MachineLearning/comments/73n9pm/d_confession_as_an_ai_researcher_seeking_advice/)

This is an interesting thread on how one could overcome the issue of lacking enough Mathematics background when doing research or reading AI papers. Well, 1) there's never enough Math and 2) everyone actually feels as inadequate as you do. Everyone has impostor syndrome except maybe for Geoffrey Hinton. 

[reddit.com](https://www.reddit.com/r/MachineLearning/comments/73n9pm/d_confession_as_an_ai_researcher_seeking_advice/)

---

### [Why Continuous Learning is the key towards Machine Intelligence](https://medium.com/@vlomonaco/why-continuous-learning-is-the-key-towards-machine-intelligence-1851cb57c308)

Here is a good overview of continuous learning, its pros and cons, and some of its latest development. 

[medium.com](https://medium.com/@vlomonaco/why-continuous-learning-is-the-key-towards-machine-intelligence-1851cb57c308)

---

### [Nonlinear Computation in Deep Linear Networks](https://blog.openai.com/nonlinear-computation-in-linear-networks/)

Here is an interesting article from OpenAI's Jakob Foerster, which we think it's a very cute idea - using the non-linearity of IEEE float, Foerster was able to use the a linear network to achieve non-linearity based on evolution strategy. 

[openai.com](https://blog.openai.com/nonlinear-computation-in-linear-networks/)

---

### [Blizzard and DeepMind cohost StarCraft II AI Workshop](http://us.battle.net/sc2/en/blog/21048078/announcing-the-starcraft-ii-ai-workshop-10-4-2017)

Applied by Oct 11, happened at the same time of Blizzconf 2017. 

[battle.net](http://us.battle.net/sc2/en/blog/21048078/announcing-the-starcraft-ii-ai-workshop-10-4-2017)

## Open Source

### [NIHS Release 100k Anonymized Chest X-Ray Images](https://www.nih.gov/news-events/news-releases/nih-clinical-center-provides-one-largest-publicly-available-chest-x-ray-datasets-scientific-community)

This is perhaps one of the largest dataset of the same type. 

[nih.gov](https://www.nih.gov/news-events/news-releases/nih-clinical-center-provides-one-largest-publicly-available-chest-x-ray-datasets-scientific-community)

## Video

### [Cognitive Computational Neuroscience 2017](http://ccneuro.org/2017videos/)

Here are all the videos of the first Cognitive Computational Neuroscience (CCN) conference. Perhaps the ones which interest us is the opening remark from [Yann Lecun](https://www.youtube.com/watch?v=cWzi38-vDbE) and the closing remark from [Yoshua Bengio](https://www.youtube.com/watch?v=W86H4DpFnLY). 

[ccneuro.org](http://ccneuro.org/2017videos/)

## Member's Question

### [How to Think of a New Idea in AI or Machine Learning.](/grandjanitor/2017/10/05/how-to-think-of-new-idea-in-a-i/)

Answer (from Arthur): 

1, What other people are doing and is it possible to make a twist about it?

2, What is a problem which *you* want to solve in your life. Then think, is there anyway AI/ML can help you? Everyone has some - e.g. I really like to make a the old-style Nintendo Final Fantasy style game. But then drawing the graphics of bitmap character takes insanely amount of time. So is there any way A.I. can help me? Yes, one potential idea is to create an image generator.

Would these ideas work? Who knows? But that's how you come up with ideas. You ignore the feasibility part for the moment. If you feel it is really hard for you to come up with ideas, chances are you are too caught up with the technical field. Read some books, listen to music, make some art and daydream a bit. Then ideas will come.

See the full discussion at this [thread](https://www.facebook.com/groups/DeepNetGroup/permalink/509996249393262/)

[thegrandjanitor.com](/grandjanitor/2017/10/05/how-to-think-of-new-idea-in-a-i/)

## Paper/Thesis Review

### [Unsupervised Hypernym Detection by Distributional Inclusion Vector Embedding](https://arxiv.org/pdf/1710.00880.pdf)

Modified from my note at [here](https://www.facebook.com/groups/aidl.ld/) 

Some notes and thoughts: 
- This work is to model relationship such as "poodle is-a dog" or generally the word entailment problem in computational linguistic.
- But what it follows is the more modern word-embedding-based approach. The hypernym problems are more often solved by Bag of Words (BOW) model. So this paper is perhaps one of the more earlier papers which used word embedding type of method on hypernym detection.
- It's good to think of why this method works. So in the case of synonyms, we all know about the distributional hypothesis - or from Firth: "a word is characterized by the company it keeps".
- What about hypernyms? the corresponding hypotheses are perhaps two "Distribution Informativeness Hypothesis" and "Distributional Inclusion Hypothesis". First stated that semantically general word occur more often. Second states that context sets of the words tends to be subset of the hypernym. So combining the two, "chihuahua" would occur less often than "dog", and adjective which can be applied to "chihuahua" can all be applied to "dog", but not necessarily vice versa.
- Then there is DIVE. So in essence, it is a modification of Mikolov's skipgram but with two major modificiations: Non-negativity of skip-gram as well as weighting the negative sample with the inverse of how often a word appears. That's pretty much is what DIVE is.
- Then there is another part about PMI (point-wise mutual information). In a nutshell, Levy and Goldberg proved that the skip-gram formulation is equivalent to matrix factorization with elements equals to PMI or (p(w,c)/p(w)p(c). The authors also give a similar formulation to DIVE. The nifty part is they also apply a filter to the PMI matrix if the occurring words are too small.
- Then there is a fairly extensive evaluation on the technique which include 11 datasets. And the authors have tested their technique with breakdown such as with/without DIVE, with/without PMI filtering. There is a very good improvement from SBOW approach.

Interesting enough. This doesn't seem to be picked by arxiv-sanity. Perhaps hypernym is more a side topic in linguistic. But it's certainly a good read. Let's see how other members think about this?

[arxiv.org](https://arxiv.org/pdf/1710.00880.pdf)
