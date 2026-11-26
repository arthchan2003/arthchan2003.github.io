---
title: "AIDL Weekly Issue 7 - The Last Imagenet, OpenAI's Evolution Strategy and AI Misinformation Epidemic"
date: 2019-05-24
---

# AIDL Weekly Issue 7 - The Last Imagenet, OpenAI's Evolution Strategy and AI Misinformation Epidemic

### Thoughts From Your Humble Curators

One of us (Waikit) is [teaching a class for MIT](https://twitter.com/maxcr/status/846936795598139393) in Brisbane, Australia. That's why we have a lighter issue. 

An interesting observation - In the MIT Entrepreneurship classes I'm teaching, there are 120 entrepreneurs from 34 countries spanning U.S to Vietnam to Kazakhstan. One of the top topics of interest and discussion was A.I. and Deep Learning. Surprising or not, some of the students were already implementing fairly advanced DL techniques in agriculture, etc. in emerging economies. It is clear that as A.I. democratizes from the ivory towers of Montreal, Stanford, CMU, FB, Google, Microsoft, etc., there will be some very long-tail positive implications in various economies over time. Is A.I. over-hyped? Sure. But people always over-estimate the short-term and under-estimate the long-term.

This week, we cover: 
- The last ImageNet
- OpenAI's new results on Evolution Strategy
- A new and popular Github, photo style transfer

We also incorporate an article from Zachary Lipton, in which he called out the hype of AI and misinformation spread from popular outlets.

If you like our letter, remember to forward to your friends and colleagues! Enjoy!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Cyclops.io turns your plain old whiteboard into a remote collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

No Download. No login. Get up and running in seconds. Ever wanted to do a quick whiteboarding session by pointing the camera at an actual whiteboard but remote guys can't read the content or collaborate together? We got you covered. We use computer vision to enhance the writing/drawing and allow anyone to annotate on it, enabling your team to [work together](http://i.imgur.com/dLyaRCX.gif) as if you're are all in the same room. You can email or post a snapshot of the whiteboard with your annotations into any Slack channels at any time. [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter) 

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [The Last Imagenet](http://image-net.org/challenges/beyond_ilsvrc.php)

The Imagenet has come to the end. Imagenet 1000's object classification performance is very close to human performance. Some authors started to evaluate on Imagenet-5k (e.g. FB [ResNeXt](https://arxiv.org/pdf/1611.05431.pdf)). It's also obvious that commercial interest on the competition also waned last year. So as the page read: 

> The workshop will mark the last of the ImageNet Challenge competitions, and focus on unanswered questions and directions for the future.

In any case, we sincerely thank to [Fei-Fei Li](http://vision.stanford.edu/feifeili/) who started the initiative, and the database has been a futile ground of object recognition/localization/detection research. 

[image-net.org](http://image-net.org/challenges/beyond_ilsvrc.php)

---

### [The Vector Institute](http://vectorinstitute.ai/)

I (Arthur) just learned this an hour before this issue published. Vector is a powerhouse of deep learning, with Geoff Hinton in the team, and Google, RBS as platinum sponsors. This is one institute which would likely generate much research in the future. 

> The Vector Institute will propel Canada to the forefront of the global shift to artificial intelligence (“AI”) by promoting and maintaining Canadian excellence in deep learning and machine learning more broadly, and by actively seeking ways to enable and sustain AI-based economic growth in Canada.

[vectorinstitute.ai](http://vectorinstitute.ai/) 

---

### [Talk by Ruslan Salakhutdinov](https://www.technologyreview.com/s/603912/apples-ai-director-heres-how-to-supercharge-deep-learning/)

It's rare to hear any news about Apple's AI, as the company is known for its secrecy. This piece, by MIT Technology Review reports on Ruslan Salakhutdinov's talk at EmTech. Salakhutdinov talks about his current research at Apple. Interesting enough, it is more about reinforcement learning, rather than Salakhutdinov's research on unsupervised learning. So we will wait and see what fruits it will bring. 

[technologyreview.com](https://www.technologyreview.com/s/603912/apples-ai-director-heres-how-to-supercharge-deep-learning/)

---

### [Talk by Gary Marcus](https://www.technologyreview.com/s/603945/is-artificial-intelligence-stuck-in-a-rut/)

Also from the MIT Technology Review, and also from the EmTech's conference. This one is by Gary Marcus, he is more vocal critic of the deep learning trend. Yet we found his argument is cogent and thought-provoking so we also include this piece here. 

[technologyreview.com](https://www.technologyreview.com/s/603945/is-artificial-intelligence-stuck-in-a-rut/)

---

### [Uber Suspends Testing SDC](https://www.nytimes.com/2017/03/25/business/uber-suspends-tests-of-self-driving-vehicles-after-arizona-crash.html)

Uber's SDC was involved in a collision last week. While there was [no serious injury reported](https://www.washingtonpost.com/news/innovations/wp/2017/03/29/we-know-more-about-that-crash-involving-ubers-self-driving-car/?utm_term=.e37f796a3b7b), soon after the company decided suspends testing of SDC. This is perhaps called for - safety of Uber's autonomous vehicle was questioned since [recode.net](https://www.recode.net/) has revealed a [leaked unfavorable disengagement document](https://www.recode.net/2017/3/16/14938116/uber-travis-kalanick-self-driving-internal-metrics-slow-progress) last week. 

(Edit: We reported earlier that there was a "fatal crash", but that's not the case, according to both [CNBC report](http://www.cnbc.com/2017/03/26/uber-self-driving-car-arizona-crash-suspended.html) and [Washington Post report](https://www.washingtonpost.com/news/innovations/wp/2017/03/29/we-know-more-about-that-crash-involving-ubers-self-driving-car/?utm_term=.e37f796a3b7b) , there was no serious injury. Apology for the mistake and thanks George Sung for pointing it.)

[nytimes.com](https://www.nytimes.com/2017/03/25/business/uber-suspends-tests-of-self-driving-vehicles-after-arizona-crash.html)

## Blog Posts

### [Evolution Strategy Proved to be Comparable as RL](https://blog.openai.com/evolution-strategies/)

OpenAI found that evolutionary strategy (ES) is found to be as competitive as reinforcement learning (RL) in modern games. There is a [paper version](https://arxiv.org/pdf/1703.03864.pdf) with more details, but I found the blog post summarized well. 

Notice that OpenAI is arguing ES is being more *parallelization-friendly* than RL. e.g. They are saying using 1440 cores on 80 machines, they can create comparably-performing system as RL in 10 minutes. Whereas RL system could only use 32 cores in one machine, and it takes 10 hours. If you compare the actual compute time, ES uses 1440x80=115200 core minutes, whereas RL system uses 32x10x60=19200 core minutes. From this calculation, even OpenAI's results suggests RL is still faster, but ES can achieve shorter wall-clock time. Perhaps that's why OpenAI says it is a *good alternative*.

If this result was proven in more domains, there would be many practical consequences. For one, in the time of deep learning, many companies abandon networks which have multiple multi-core machines, instead they prefer a few machines which has powerful GPU cards. This GPU-card-centric architecture is mostly motivated by backprop, which require gradient communication every iteration, which is hugely expensive.

ES, on the other hand, is episode-based, every core can just pick up one episode, evaluate fitness and generate *one scaler value*. Of course, that won't cause too much problem in communication and you can use many more machines/cores. So if ES is found to be competitive in more problems, you would expect companies would go back to network with multiple multi-core structures. Also, importance of *GPU cards would be deemphasized*, which is a whole new ballpark for everyone working on reinforcement learning now.

Also, if a certain problem can be solved by ES, RL researchers would have existential crisis because ES made minimal assumptions on problems, and it's more generic. Whereas RL methods usually have many whistles and bells. Moreover, some algorithm such as [neuro-evolution](http://www.scholarpedia.org/article/Neuroevolution) also allows the network topology to be altered. That sounds very attractive if computation is not a limiting factor.

Perhaps it's still too early to say..... OpenAI's result only say that ES can be comparable with RL in task which was dominated by RL (MuJoCo and Atari). If they later prove ES can beat RL in unsolved challenges, such as man-machine match on Starcraft, or self-driving car, DeepMind's researchers are going to adapt ideas of ES into their research.

[openai.com](https://blog.openai.com/evolution-strategies/)

---

### [The AI Misinformation Epidemic](http://approximatelycorrect.com/2017/03/28/the-ai-misinformation-epidemic/)

Here is a thought-provoking article written by [Zachary Lipton](https://www.linkedin.com/in/zacharylipton/) who is a graduate from USCD and would be an assistant professor of CMU next January. We cannot agree with him more - at [AIDL](https://www.facebook.com/groups/DeepNetGroup/), we witness misinformation and faked news spread daily - That's why we constantly curate postings. Also, there are many self-proclaimed deep learning consultants, as well as so-called influencers, who would publish for the sake of clicks and publicity. 

The truth is *no filters can be more effective that your critical mind*. You, as a reader, should be cautious and critical about sensational news when it comes to deep learning..... or perhaps on any topics.

[approximatelycorrect.com](http://approximatelycorrect.com/2017/03/28/the-ai-misinformation-epidemic/)

---

### [Deep Learning with a Pre-configured VM](https://medium.com/@ageitgey/try-deep-learning-in-python-now-with-a-fully-pre-configured-vm-1d97d4c3e9b)

There is this popular post by Adam Geitgey. He did something which is very handy for testing deep learning tools - a pre-configured VM. 

Making sure you can use different DL packages is alway tough. In python, if you hit similar problem, other than using a pre-configured VM, you can also try the following strategies: 
- Use multiple python installations such as anaconda
- virtualenv
- Docker

[medium.com](https://medium.com/@ageitgey/try-deep-learning-in-python-now-with-a-fully-pre-configured-vm-1d97d4c3e9b)

---

### The Bandwagon (using in the words of Claude Shannon, 1956)

This is an essay modified from Claude Shannon's "The Bandwagon" about machine learning. I saw it shared by [Cheng Soon Ong](https://plus.google.com/+ChengSoonOng). 

"Machine Learning has, in the last few years, become something of a scientific bandwagon. Starting as a technical tool for the computer scientist, it has received an extraordinary amount of publicity in the popular as well as the scientific press. In part, this has been due to connections with such fashionable fields computing machines, cybernetics, and automation; and in part, to the novelty of the subject matter. As a consequence, it has perhaps been ballooned to an importance beyond its actual accomplishments. Our fellow scientists in many different fields, attracted by the fanfare and by the new avenues opened to scientific analysis, are using these ideas in their own problems. Applications are being made to biology, psychology, linguistics, fundamental physics, economics, the theory of organisation, and many others. In short, machine learning is currently partaking of a somewhat heady draught of general popularity.

Although this wave of popularity is certainly pleasant and exciting for those of us working in the field, it carries at the same time an element of danger. While we feel that machine learning is indeed a valuable tool in providing fundamental insights into the nature of computing problems and will continue to grow in importance, it is certainly no panacea for the computer scientist or, a fortiori, for anyone else. Seldom do more than a few of natures' secrets give way at one time. It will be all too easy for our somewhat artificial prosperity to collapse overnight when it is realised that the use of a few exciting words like deep learning, artificial intelligence, data science, do not solve all our problems.

What can be done to inject a note of moderation in this situation? In the first place, workers in other fields should realise that the basic results of the subject are aimed in a very specific direction, a direction that is not necessarily relevant to such fields as psychology, economics, and other social sciences. Indeed, the hard core of machine learning is, essentially, a branch of mathematics and statistics, a strictly deductive system. A thorough understanding of the mathematical foundation and its computing application is surely a prerequisite to other applications. I personally believe that many of the concepts of machine learning will prove useful in these other fields -- and, indeed, some results are already quite promising -- but the establishing of such applications is not a trivial matter of translating words to a new domain, but rather the slow tedious process of hypothesis and experimental verification. If, for example, the human being acts in some situations like an ideal predictor, this is an experimental and not a mathematical fact, and as such must be tested under a wide variety of experimental situations.

Secondly, we must keep our own house in first class order. The subject of machine learning has certainly been sold, if not oversold. We should now turn our attention to the business of research and development at the highest scientific plane we can maintain. Research rather than exposition is the keynote, and our critical thresholds should be raised. Authors should submit only their best efforts, and these only after careful criticism by themselves and their colleagues. A few first rate research papers are preferable to a large number that are poorly conceived or half-finished. The latter are no credit to their writers and a waste of time to their readers. Only by maintaining a thoroughly scientific attitude can we achieve real progress in machine learning and consolidate our present position."

Shannon's original can be found [here](http://www.eoht.info/page/Shannon+bandwagon%EF%BB%BF).

Artificial Intelligence and Deep Learning Weekly

## Open Source

[*[image not recovered: original_ratio_extra_large_64ed5cb2-ad56-465d-bbb1-66d48c219fa8.png]*](https://github.com/luanfujun/deep-photo-styletransfer) 

### [Photo Style Transfer](https://github.com/luanfujun/deep-photo-styletransfer)

This is the code based on the interesting paper ["Deep Photo Style Transfer"](https://arxiv.org/pdf/1703.07511.pdf) jointly written by researchers from Cornell and Adobe. As you might know, most neural-style transfer was based on Gatys' ["Gram-matrix" method](https://arxiv.org/abs/1508.06576), but once you play with the method a bit, you would notice that getting results similar to the author is difficult. For a while, there was a mystery of how the method work, In cs231n 2016 Lecture 9, Justin Johnson comments that Gram-matrix is only one way to do such transfer, for example, it is reasonable to use any statistics which represent the picture to be optimization criterion. So one work was based on [CNNMRF](https://arxiv.org/abs/1601.04589), in which the most similar patch from the style image is using choose to match the content image. 

Despite of all this work, you can seldom transfer a style from another photo. That makes "Deep Photot Style Transfer" special. In essence, it uses two tricks:

\*[NeuralDoodle's method](https://github.com/alexjc/neural-doodle) or general semantic segmentation method (See Lecture 13 of cs231n 2016). A segmentation mask is first generated and segment class is augmented. This allows the authors to device a class-dependent metric on the statistics.

\*A photorealism regularization loss which penalizes image distortion. The idea is derived from an [image matting paper](http://www.wisdom.weizmann.ac.il/~levina/papers/Matting-Levin-Lischinski-Weiss-CVPR06.pdf) from 06. I (Arthur) believe, roughly, it calculates an affine transform to reduce the "stretch" of the input image color space.

The authors then augment the standard neural-style loss function with the photorealism loss. Since the 06 paper already has proposed an optimization function, the technical merit of the authors is to integrate such function into back propagation.

We haven't quite tried out the method. But from the examples from the paper, the results is quite stunning. The first panel from the left is the original content, the second is the style, the one at the right is transferred image. If you look at the original paper, indeed photo-style transfer gives much better results than either the gramm-matrix method or CNNMRF method. (Photo Credit: edited from the paper.)

[github.com](https://github.com/luanfujun/deep-photo-styletransfer)

## Member's Question

### Some Tips on Reading "Deep Learning" By GoodFellow et al

Q: How do you read the book [Deep Learning](http://www.deeplearningbook.org/) By Ian GoodFellow 

It depends on the chapters you are in. The first two parts are better as supplementary material to lectures/courses. For example, if you are reading deep learning and watching all videos from Karpathy's and Socher's class, you would learn much more than other students. We think the best lecture to go with is Hinton's "Neural Network".

Part 1 tries to power you through the necessary Math. If you never have at least a class of machine learning, those material are woefully inadequate. Consider to study matrix algebra or more importantly matrix differentiation first. (Abadir's [Matrix Algebra](https://www.amazon.com/Matrix-Algebra-Econometric-Exercises-Vol/dp/0521537460) is perhaps the most relevant.) Then you will make through the Math more easily. Saying so, Chapter 4's example on PCA is quite cute. So read them if you are comfortable with the math.

Part 3 is tough, and for the most part it is a reading for researchers in *unsupervised learning*, which many people believe it is the holy grail of the field. You will need to be comfortable with energy-based model. For that, we suggest you go through Lecture 11 to 15 of Hinton's deep learning first. If you don't like unsupervised learning, you could skip Part 3 for now. Reading Part 3 is more about knowing what other people are talking about in unsupervised learning.

While deep learning is a hot field, make sure you don't abandon other ideas in machine learning. e.g. we find reinforcement learning and genetic algorithm very useful (and fun). Learning theory is deep and can explain certain things we experienced in machine learning. IMO, those topics are at least as interesting as Part 3 of deep learning. (Thanks Richard Green at AIDL for his opinion.)

Artificial Intelligence and Deep Learning Weekly
