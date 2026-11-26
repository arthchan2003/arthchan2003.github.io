---
title: "AIDL Weekly #40 - Special Issue on NIPS 2017"
date: 2019-07-08
---

# AIDL Weekly #40 - Special Issue on NIPS 2017

# [Issue 40 *December 9th 2017* ](http://aidl.io/issues/40/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

Last week was the week of NIPS 2017. We chose 5 links from the conferences in this issue. 

The news this week is all about hardware, we point you to the new Titan V, the successor of the Titan series. Elon Musk is also teasing us the best AI hardware of the world. Let's take a closer look.

And as you might read from elsewhere: is Google building an AI which can build another AI? Our fact-checking section will tell you more.

Finally, we cover two papers this week: 
- The new DeepMind paper which describes how AlphaZero become master of chess and shogi as well,
- Fixing weight decay regularization in Adam.

---

Join our community for real-time discussions with this iOS app here: [https://itunes.apple.com/us/app/expertify/id969850760](http://apple.co/2z8Z7Qi)

As always, if you like our newsletter, feel free to subscribe/forward it to your colleagues.

Artificial Intelligence and Deep Learning Weekly

## News

### [New AI Hardware from Tesla](https://www.cnbc.com/2017/12/08/elon-musk-talks-up-teslas-upcoming-artificial-intelligence-hardware.html)

Elon Musk is teasing a new AI hardware from Teslas. In a non-stream conversation, he said "Jim is developing specialized AI hardware that we think will be the best in the world,", according to one person at the event. This CNBC report actually quotes [Stephen Merity](https://smerity.com/abme.html), which we know has a lot of credibility. 

[cnbc.com](https://www.cnbc.com/2017/12/08/elon-musk-talks-up-teslas-upcoming-artificial-intelligence-hardware.html)

---

### [Titan V](https://venturebeat.com/2017/12/07/nvidia-launches-new-titan-v-desktop-gpu-to-accelerate-ai-computation/)

One thing we learn from NIPS 2017. Titan X has a successor: Titan V. It now has 110 teraflops of raw computing capability, 9x of its predecessor. But it costs $3000. This is close to a low-end Tesla card such as K2000 or K4000. Jensen Huang told us this is the best card for desktop, we have no doubt. 

[venturebeat.com](https://venturebeat.com/2017/12/07/nvidia-launches-new-titan-v-desktop-gpu-to-accelerate-ai-computation/)

## Factchecking

### On Google's "AI Built an AI That Outperforms Any Made by Humans"

For those who are new at AIDL. AIDL has what we called "The Three Pillars of Posting". i.e. We require members to post articles which are relevant, non-commercial and non-sensational. When a piece of news with sensationalism start to spread, admin of AIDL (in this case, Arthur) would fact-check the relevant literature and source material and decide if certain pieces should be rejected. And this time we are going to fact-check a popular yet misleading piece "AI Built an AI That Outperforms Any Made by Humans". 
- The first thing to notice: "AI Built an AI That Outperforms Any Made by Humans" by a site which historically sensationalized news. The same site was involved in sensationalizing the early version of AutoML, as well as the notorious "AI learn language" fake news wave.
- So what is it this time? Well, it all starts from Google's [AutoML published in May 2017](https://research.googleblog.com/2017/05/using-machine-learning-to-explore.html) If you look at the page carefully, you will notice that it is basically just a tuning technique using reinforcement learning. At the time, The research only worked at CIFAR-10 and PennTree Banks.
- But then Google's AutoML released another version in November. The gist is that Google beat SOTA results in Coco and Imagenet. Of course, if you are a researcher, you will simply interpret it as "Oh, now automatic tuning now became a thing, it could be a staple of the latest evaluation!" The model is now distributed as [NASnet](https://arxiv.org/abs/1707.07012).
- Unfortunately, this is not how the popular outlets interpret. e.g. Sites were claiming "AI Built an AI That Outperforms Any Made by Humans". Even more outrageous is some sites are claiming "AI is creating its own 'AI child'". Both claims are false. Why?
- As we just said, Google's program is an RL-based program which propose the child architecture, isn't this parent program still built by humans? So the first statement is refutable. It is just that someone wrote a tuning program, more sophisticated it is, but still a tuning program.
- And, if you are imagining "Oh AI is building itself!!" and have this imagery that AI is now self-replicating, you cannot be more wrong. Again, remember that the child architecture is used for other tasks such as image classification. These "children" doesn't create yet another group of descendants.
- A much less confusing way to put it is that "Google RL-based AI now able to tune results better than humans in some tasks." Don't get us wrong, this is still an exciting result, but it doesn't give any sense of "machine is procreating itself".

We hope this article clears up the matter. We rate the claim "AI Built an AI That Outperforms Any Made by Humans" **false**. 

Here is the original [Google's post](https://research.googleblog.com/2017/11/automl-for-large-scale-image.html).

Artificial Intelligence and Deep Learning Weekly

## NIPS 2017

### [Is Machine Learning Alchemy?](https://www.youtube.com/watch?v=Qi1Yry33TQE&feature=youtu.be)

Perhaps the highlight of this NIPS is the debate between NIPS Test of Time Award winner, Al Rahimi, and deep learning demi-god Prof. Yann Lecun. What happened? 

In the Award presentation, Rahim said "Machine learning has become alchemy." This is meant to be a counter to another well-known saying from Andrew Ng: "Artificial intelligence is the new electricity." He cuts deep into the current problem of machine learning: lacks of theoretical framework.

Prof. Lecun seems to be very upset by Rahimis' comment. In his long [Facebook post](https://www.facebook.com/yann.lecun/posts/10154938130592143), he raised his disagreement. His main point is that historically engineering effort always precede theoretical results. As he said, 

> the lens and the telescope preceded optics theory, the steam engine preceded thermodynamics, the airplane preceded flight aerodynamics, radio and data communication preceded information theory, the computer preceded computer science.

This exchange spawns a great debate within the community. e.g. Ferenc Huszár in [Alchemy, Rigour and Engineering](http://www.inference.vc/my-thoughts-on-alchemy/), he raised a good point that while you can have incomplete or non-rigorous theoretically understanding, but having non-rigorous testing method like many papers is bad.

We really don't want to take side in the debates. But let's wrap it up with the rhyme battle between "Bored Yann LeCun"(The parody account of Prof. LeCun) and Ali Rahimi? 

> Rocking that alchemy // from my penthouse balcony // my empirical, lyrical modality // it's like fine sashimi, Ali Rahimi // I choose elbow grease // over rigor police #feelthelearn

for which Ali Rahimi replied, 

> phat beats to the dome // like weights dropped at random // my training methodology // exposes yours' pathology // i'm getting warmed up // take your ball and go home

[youtube.com](https://www.youtube.com/watch?v=Qi1Yry33TQE&feature=youtu.be)

---

### [DeepMind at NIPS 2017](https://deepmind.com/blog/deepmind-papers-nips-2017/)

Here's a list of paper published by DeepMind at NIPS 2017. 

[deepmind.com](https://deepmind.com/blog/deepmind-papers-nips-2017/)

---

### [Papers for NIPS Machine Learning for Creativity and Design 2017](https://nips2017creativity.github.io/)

Shared by David Ha. Here are all the papers accepted at NIPS Creativity workshop. 

[github.io](https://nips2017creativity.github.io/)

---

### [NIPS live video](https://www.facebook.com/nipsfoundation/videos/1554402331317667/?hc_ref=ARQjwKWf_ZV6VKWfdNcVnJxGLOvFjXalZFaUU-IVSC-aQ0g2wePkjfmDIpXnTVJ7HuQ&fref=gs&dti=107107546348803&hc_location=group)

Here is a feed for NIPS 2017 live video. 

[facebook.com](https://www.facebook.com/nipsfoundation/videos/1554402331317667/?hc_ref=ARQjwKWf_ZV6VKWfdNcVnJxGLOvFjXalZFaUU-IVSC-aQ0g2wePkjfmDIpXnTVJ7HuQ&fref=gs&dti=107107546348803&hc_location=group)

---

[*[image not recovered: twenty_by_nine_extra_large_d2ffb584-4a1a-44d2-9946-f5fcf5ff7b12.jpg]*](https://twitter.com/goodfellow_ian/status/938554659051941888) 

### [Cake We All Love](https://twitter.com/goodfellow_ian/status/938554659051941888)

Enough said 

[twitter.com](https://twitter.com/goodfellow_ian/status/938554659051941888)

## Blog Posts

### [Optimization for Deep Learning Highlights in 2017 ](http://ruder.io/deep-learning-optimization-2017/index.html)

Another great article by Sebastian Ruder, which you can see it as a sequel of his [An overview of gradient descent optimization algorithms](http://ruder.io/optimizing-gradient-descent/). This includes a short but concrete explanation of the latest ADAM with proper implementation of weight decay, warm restart, latest studies of generalization and more. 

[ruder.io](http://ruder.io/deep-learning-optimization-2017/index.html)

---

### [The Last 5 Years In Deep Learning](https://adeshpande3.github.io/adeshpande3.github.io/The-Last-5-Years-in-Deep-Learning)

Adit Deshpande wrote a great article on the development of deep learning the last 5 years. We enjoy it a lot - not only it summarized what happened, it also gives a set of great pointers to different papers and resources. 

[github.io](https://adeshpande3.github.io/adeshpande3.github.io/The-Last-5-Years-in-Deep-Learning)

---

### [Intelligence Augmentation ](https://distill.pub/2017/aia/)

This is a brilliant article written by Shan Carter and Michael Nielsen. It explains how generative technology of AI help humans to create. Long time readers of AIDL shouldn't find Nielsen foreign. He is the author of the very educational [Neural Network and Deep Learning](http://neuralnetworksanddeeplearning.com/). Of course, he is more well-known to write the popular textbook [Quantum Computation and Quantum Information](https://www.amazon.com/Quantum-Computation-Information-10th-Anniversary/dp/1107002176). 

[distill.pub](https://distill.pub/2017/aia/)

## Open Source

### [VGG Face2 Database](http://www.robots.ox.ac.uk/~vgg/data/vgg_face2/)

Here is update of the very popular VGG Face database. Pretrained model is included. 

[ox.ac.uk](http://www.robots.ox.ac.uk/~vgg/data/vgg_face2/)

---

### [PyTorch v0.3.0](https://github.com/pytorch/pytorch/releases/tag/v0.3.0)

PyTorch v0.3.0 is just released, featuring new layers and ONNX supports. 

[github.com](https://github.com/pytorch/pytorch/releases/tag/v0.3.0)

## Member's Question

### How do you read Duda and Hart's "Pattern Classification"?

Question (rephrase): I was reading the book "Pattern Classification" by Duda and Hart, but I found it difficult to follow the mathematics, what should I do? 

Answer: (*by Arthur*) You are reading a good book - Duda and Hart is known to be one of the Bibles in the field. But perhaps is slightly beyond your skill at this point.

My suggestion is to make sure you understand basic derivations such as linear regression and perceptron. Also if you get stuck with the book for a long time, try to go through Andrew Ng's Machine Learning. Granted the course is much easier than Duda and Hart, but you would also have the outline what you are trying to prove.

One specific advice on the derivation of NN - I recommend you to read Chapter 2 of Michael Nielsen's book first because he is very good at defining clear notation. e.g. meaning of the letter z changes in different text books, but it is crucial to know exactly what it means to follow a derivation.

Artificial Intelligence and Deep Learning Weekly

## Paper/Thesis Review

### [Fixing Weight Decay Regularization in Adam](https://arxiv.org/abs/1711.05101)

Here is a read on the paper "Fixing Weight Decay Regularization in Adam", a major correction of how weight decay with ADAM should be used together. 
- The key to understand this paper is that weight decay is often implemented as L2 regularization in the optimization function. And we often think that the two concepts, weight decay and L2 regularization, are the same.
- But then the authors, Loshchilov and Hutter observed a very simple fact: which is if you implement weight decay through L2 regularization often reduce the effect of weight decay. So that explain why ADAM has poorer generalization power.
- We will just refer you guys to Algorithm 1 and 2 on p.3. And if you follow the text you will quickly realize the past implementation was just wrong. The authors also proposed how you can fix the update to get weight decay correctly. (The green highlights.)
- Reading the paper also required you to understand the idea of warm restarts. You can read it from the paper [SGDR: Stochastic Gradient Descent with Warm Restarts](https://arxiv.org/abs/1608.03983).
- The authors went ahead to show that the idea works well on Top-1 Error of CIFAR-10 and Top-5 Error of Imagenet32x32, a downsampled Imagenet. Looks good.
- This sounds like a great idea. In fact, the author of ADAM, DP Kingma, [thought so too](https://twitter.com/dpkingma/status/930849593767608320). So is Jeremy Howard, the technique is already implemented in fast.ai's code.

The original Link can be found at [here](https://www.facebook.com/groups/aidl.ld/permalink/916627038501963/). 

[arxiv.org](https://arxiv.org/abs/1711.05101)

---

### [Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm](https://arxiv.org/pdf/1712.01815.pdf)

- As you know the story, AlphaZero is not only just playing Go, and is now playing Chess and Shogi. By itself this is a significant event, because most stoa board game engine are specific to games. General game playing engines are seen as novelties but not a norm.
- Another note, most Chess and Shogi engines are based on alpha-beta search. But then AlphaZero is now using Monte-Carlo Tree Search which simulate board positions. Positions are order by scores from a board NN. State is entered in the order of visit counts and value of the board according to NN. So you can see this is not just AlphaZero is beating up more games, it will be more a paradigm shift of both computer Chess and Shogi community.
- As you know, AlphaZero beats the strongest program in 2016, Stockfish. But one analysis which caught my eyes: In chess, DeepMind researchers also fix the first few moves of AlphaZero so that it follows the top 12 most-play openings for black and white. If you are into chess, Queen's Gambit, several Sicilian Defences, The French, KID. They show that AlphaZero can beat Stockfish in multiple type of situations, and openings doesn't matter too much.
- But then, would AlphaZero beat all computer players such as Shredder or Komodo? No one knows the answers yet.
- One more thing: AlphaZero doesn't assume zero knowledge neither. As [Denny Britz](https://twitter.com/dennybritz/status/938253382430597120) points out in his tweet, AlphaZero was provided with perfect knowledge in terms of rules. So intriguing rules such as castling, threefold repetition or 50-move drawing rules are all provided to the machine. Perhaps Britz points out, may be we want to focus on how to let the machine to figure out the rules themselves in the future.

[arxiv.org](https://arxiv.org/pdf/1712.01815.pdf)
