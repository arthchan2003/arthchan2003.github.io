---
title: "Learning Deep Learning - My Top-Five List"
date: 2016-08-15
categories: ["deep learning", "Machine Learning", "reinforcement learning"]
---

# Learning Deep Learning - My Top-Five List

Many people have been nagging me to write a beginner guide on deep learning. Geez, that's a difficult task - there are so many tutorials, books, lectures to start with, and the best way to start highly depends on your background, knowledge and skill sets. So it's very hard to give a simple guideline.

In this post, I will do something less ambitious: I gather what I think is the top-5 most important resources which let you to start to learn deep learning. Check out the "Philosophy" section on why this list is different from other lists you saw. 

## Philosophy

There are many lists of resources of deep learning. To name a few, the "[Awesome](https://github.com/ChristosChristofidis/awesome-deep-learning)" list, the [Reddit machine learning FAQ](https://www.reddit.com/r/MachineLearning/wiki/index). I think they are quality resources, and it's fair to ask why I started "Top-Five" a year ago.

Unlike all the deep learning resource list you saw, "Top-Five" is not meant to be an exhaustive list. Rather it assumes you have only limited amount of time to study and gather resources while learning deep learning. For example, suppose you like to learn through on-line classes. Each machine/deep learning class would likely take you 3 months to finish. It will take you a year to finish all the classes. As a result, *having a priority* *is good.* For instance, without any guidance, reading Goodfellow's *Deep Learning* would confuse you. A book such as Bishop's *P**attern Recognition and Machine Learning* (PRML) would likely be a better "introductory book".

Another difference between Top-Five list and other resource list is that the resource* are curated*. Unless specified, I have either finished the material myself. So for classes I have at least audit the whole lecture once. For books I probably browse it once. In a way, this is more an "Arthur's list", rather than some disorganized links. You also see a short commentary why (IMO) they are useful. 

## Which Top-Five?

As the number of sections in my list grow, it's fair to ask what resources should you spend time on first. That's a tough question because humans differ in their preference of learning. My suggestion is start from the following, 
1. Taking classes - by far I think it is the most effective way to learn. Listening+doing homework usually teach you a lot.
2. Book Reading - this is important because usually lectures only summarize a subject. Only when you read through a certain subject, you start to get deeper understanding.
3. Playing with Frameworks - This allows you to actually create some deep learning applications, and turn some your knowledge in real-life
4. Blog Reading - this is useful but you better know which blogs to read (Look at the section "Blogs You Want To Read"). In general, there are just too many blog writers these days, and they might only have murky understanding of the topic. Reading those would only make you feel more confused.
5. Joining Forums and ask questions - this is where you can dish out some of your ideas and ask for comments. Once again, the quality of the forum matters. So take a look of the section "Facebook Forums".

## Lectures/Courses

##### Basic Deep Learning (Also check out "[The Basic-Five](/grandjanitor/2017/05/13/learning-deep-learning-the-basic-five-five-beginner-course-on-deep-learning/)")

This are more the must-take courses if you want to learn the basic jargons of deep learning. Ng's, Karparthy's and Socher's class teach you basic concepts but they have a theme of building applications. Silver's class link deep learning concepts with reinforcement learning. So after these 4 classes, you should be able to talk deep learning well and work with some basic applications. 
1. [Andrew Ng's Coursera Machine Learning class](https://www.coursera.org/learn/machine-learning) 
        - You need to walk before you run. Ng's class is the best beginner class on machine learning in my opinion. Check out this page for [my review.](/grandjanitor/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/)
2. [Andrew Ng's deeplearning.ai Specialization](https://www.coursera.org/learn/neural-networks-deep-learning) 
        - In my view, the best transition class from Ng's Machine Learning class to more difficult classes such as cs231n and cs224n. See my full reviews of[Course 1](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/) and [Course 2](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/). Also Check our my [quick impressions at here](/grandjanitor/2017/08/09/quick-impression-on-deeplearning-ai/) and review of one of the ["Heros of Deep Learning" with Prof. Geoffrey Hinton](/grandjanitor/2017/08/13/quick-impression-on-deeplearning-ai-heroes-of-deep-learning-geoffrey-hinton/).
3. [Fei-Fei Li and Andrew Karpathy's Computer Vision class](http://cs231n.stanford.edu/) (Stanford cs231n 2015/2016) 
        - I listen through the lectures once. Many people just call this a Karpathy's class, but it is also co-taught by another experienced graduate student, Justin Johnson. For the most part this is the class for learning CNN, it also brings you to the latest technology of more difficult topics such as image localization, detection and segmentation.
4. [Richard Socher's Deep Learning and Natural Language Processing](http://cs224d.stanford.edu/) (Standard cs224d) 
        - I listen to the whole lecture once, the first few lectures were very useful for me when I tried to understand RNN and LSTM. This might also be the best set of lecture to learn Socher's recursive neural network. Compare to Karpathy's class, Socher's place more emphasis on mathematical derivation. So if you are not familiar with matrix differentiation, this would be a good class to start with and get your hands wet.
5. [David Silver's Reinforcement Learning](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html) 
        - This is a great class taught by the main programmer of [AlphaGo](http://www.nature.com/nature/journal/v529/n7587/full/nature16961.html). It starts from the basic of reinforcement learning such as DP-based method, then proceeds to more difficult topic such as Monte-Carlo and TD method, as well as function approximation and policy gradient. It takes quite a bit of understanding even if you already background of supervised learning. As RL is being used more and more applications, this class should be a must-take for all of you.

You should also consider: 
- [Fast.ai](http://www.fast.ai/)'s Deep Learning for Coders 
        - a class which has generally good review. I would suggest you read [Arvind Nagaraj's post](https://medium.com/towards-data-science/thoughts-after-taking-the-deeplearning-ai-courses-8568f132153) which compare deeplearning.ai and fast.ai.
- [Theories of Deep Learning](https://www.researchgate.net/project/Theories-of-Deep-Learning) 
        - Or Stanford Stat 385, which is one of the theory class of deep learning.
- [Hugo Larochelle's Neural Network class](http://info.usherbrooke.ca/hlarochelle/neural_networks/content.html) 
        - by another star-level innovator of the field. I only heard Larochelle's lecture in a deep learning class, but he is succinct and to the point than many.
- [MIT Self Driving 6.S094](http://selfdrivingcars.mit.edu/) 
        - See the description in the session of Reinforcement Learning.
- [Nando de Freita's class on Machine/Deep Learning](https://www.cs.ox.ac.uk/people/nando.defreitas/machinelearning/) 
        - I don't have a chance to go through this one, but it is both for beginner and more advanced learners. It covers topics such as reinforcement learning and siamese network. I also think this is the class if you want to use Torch as your deep learning language.

##### Intermediate Deep/Machine Learning

The intermediate courses are meant to be the more difficult sets of classes. They are much more difficult to finish - Math is necessary. There are also many confusing concepts even if you already have Master. 
1. [Hinton's Neural Network Machine Learning](https://www.coursera.org/learn/neural-networks) 
        - While the topics are advanced, Prof. Hinton's class is probably the one which can teach you the most on the philosophical difference between deep learning and general machine learning. The first time I audit the class in 2016 October, his explanation on models based on statistical mechanical model blew my mind. I finished the course around 2017 April, which results in a popular [review post](/grandjanitor/2017/04/10/review-of-hintons-coursera-neural-network-and-machine-learning/). Unfortunately, due to the difficulty of the class, it was ranked lower in this list. (It was ranked 2nd, then 4th on the Basic Five, but I found that it requires deeper understanding than the Karparthy's, Socher's and Silver's. Later on when deeplearning.ai comes up, I shift Prof Hinton's course to one of the Intermediate classes. )
2. [Daphne Koller's Probabilistic Graphical Model](https://www.coursera.org/learn/probabilistic-graphical-models) 
        - if you want to understand tougher concepts in models such as DBN, you want to have some background in Bayesian network as well. If that's the route you like, Koller's class is for you. But this class, just like Hinton's NNML, is notoriously difficult and not for faint of heart - you will be challenged on probability concepts (Course 1), graph theory and algorithm (Course ) and parameter estimation (Course 3).

##### Reinforcement Learning

Reinforcement learning has deep history by itself and you can think it has the heritage from both computer science and electrical engineering.

My understanding of RL is fairly shallow so I can only tell you which are the easier class to take, but all of these classes are more advanced. Georgia Tech CS8803 should probably be your first. Silvers' is fun, and it's based on Sutton's book, but be ready to read the book in order to finish some of the exercises. 
1. [Udacity's Reinforcement Learning ](https://www.udacity.com/course/reinforcement-learning--ud600) 
        - This is a class which is jointly published by Georgia Tech and you can take it as an advanced course CS8803. I took Silver's class first, but I found the material this class provides a non-deep learning take and quite refreshing if you start out at reinforcement learning.
2. [David Silver's Reinforcement Learning](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching.html) 
        - See description in the "Introductory Deep Learning" section.
3. [MIT Self Driving 6.S094](http://selfdrivingcars.mit.edu/) 
        - A specialized class in self-driving. The course is mostly computer vision, but there is one super-entertaining exercise on self driving, which mostly likely you want to use RL to solve the problem. (Here is some [quick impression ](/grandjanitor/2017/05/12/some-quick-impression-on-mit-dl4sdc-class-by-lex-friedman/)about the class.)

You should also consider: 
- [Berkeley's Deep Reinforcement Learning](http://rll.berkeley.edu/deeprlcourse/#lecture-videos) Potentially a third class about deep reinforcement learning (after Silver's and Schulmann's).

##### I heard good things about them......

- [Oxford Deep NLP 2017 ](https://github.com/oxford-cs-deepnlp-2017/lectures) 
        - This is perhaps the second class of deep learning on NLP. I found the material interesting because it covers material which wasn't covered by the Socher's class. I haven't takem it yet. So I will comment later.
- [Statistical Computing by Nicholas Zabara ](https://www.zabaras.com/statisticalcomputing) 
        - looks super interesting and most material are actually ML-based.
- [CMU CS11-747 Neural Networks and NLP](https://www.youtube.com/user/neubig/playlists) 
        - A great sets of lecture by Graham Neubig. Neubig has written few useful tutorial on DL in NLP. So I add his as more promising candidate here as well.
- [NYU Deep Learning class at 2014](http://cilvr.cs.nyu.edu/doku.php?id=deeplearning:slides:start#week_1) 
        - Prof. Yann LeCun. To me this is an important class, with similar importance as Prof. Hinton's class. Mostly because Prof. LeCun is one of the earliest experimenters on BackProp and SGD. Unfortunately these NYU's lecture was removed. But do check out the slides though.
- Also from Prof. Yann LeCun, [Deep Learning inaugural lectures](https://www.college-de-france.fr/site/en-yann-lecun/course-2015-2016.htm).
- Berkely's Seminar on Deep Learning: by Prof. **** [Ruslan Salakhutdinov](http://www.cs.cmu.edu/~rsalakhu/), an early researcher on unsupervised learning.
- [University of Amsterdam Deep Learning](http://uvadlc.github.io/) 
        - If you have already audit cs231n and cs224d, perhaps the material here is not too new, but I found it useful to have a second source when I look at some of the material. I also like the presentation of back-propagation, which is more mathematical than most beginner class.
- [Special Topics in Deep Learning](https://berkeley-deep-learning.github.io/cs294-131-s17/) 
        - I found it great resource if you want to drill on more exoteric topics in deep learning.
- [Deep Learning for Speech and Language](https://telecombcn-dl.github.io/2017-dlsl/) 
        - of my own curiosity on speech recognition. This course is perhaps is the only one I can find on DL on ASR. If you happen to stumble this paragraph, I'd say most software you find on-line are not really too applicable in real-life. The only exceptions are discussed in [this very old article of mine](/grandjanitor/2013/11/17/learning-asr-through-coding/).

##### For reference

- [Virginia Tech Deep Learning at 2015](https://computing.ece.vt.edu/~f15ece6504/)
- [University of Waterloo by Prof Ali Ghodsi](https://uwaterloo.ca/data-analytics/)
- [MIT 6.S191 Introduction to Deep Learning](http://introtodeeplearning.com/index.html)
- [Deep RL and Control from CMU ](https://katefvision.github.io/)
- [Udacity Deep Learning](https://classroom.udacity.com/courses/ud730) and Deep Learning NanoDegree.

##### Great Preliminaries

- [Linear Algebra By Prof. Gilbert Strang](https://ocw.mit.edu/courses/mathematics/18-06sc-linear-algebra-fall-2011/)
- [Probabilistic System and Applied Probability By Prof. John Tsitsiklis](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-041sc-probabilistic-systems-analysis-and-applied-probability-fall-2013/index.htm)

##### More on Basic Machine Learning (Unsorted)

- ColumbiaX: [CSMM.102x](https://www.edx.org/course/machine-learning-columbiax-csmm-102x-1)
- [ESL](http://www.dataschool.io/15-hours-of-expert-machine-learning-videos/)
- [Caltech Machine Learning](https://work.caltech.edu/telecourse.html).
- [Andrew Ng's Machine Learning 2008](https://www.youtube.com/playlist?list=PLA89DCFA6ADACE599)
- [Tony Mitchell's Machine Learning 2011](http://www.cs.cmu.edu/~tom/10701_sp11/lectures.shtml)
- [Nando De Freita's Machine Learning 2012](https://www.youtube.com/playlist?list=PLE6Wd9FR--Ecf_5nCbnSQMHqORpiChfJf)

##### More AI than Machine Learning (Unsorted)

- [Berkley CS 188](http://ai.berkeley.edu/lecture_videos.html)
- [Stanford cs221](http://web.stanford.edu/class/cs221/)
- [edX AI](https://www.edx.org/course/artificial-intelligence-ai-columbiax-csmm-101x-0)
- [MIT AI Courseware - lectures by Patrick Winston](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-034-artificial-intelligence-fall-2010/)
- [Prof. Marvin Minsky's The Society of Minds ](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-868j-the-society-of-mind-fall-2011/)

##### More about the Brain:

I don't have much, but you can take a look of my another list on [Neuroscience MOOCs](/grandjanitor/2017/04/10/list-of-neuroscience-mooc/). 

## Books

I wrote quite a bit on the [Recommended Books Page](/grandjanitor/2017/10/09/repost-recommended-books-in-machine-learningdeep-learning/). In a nutshell, I found that classics such as PRML and Duda and Hart are still must-reads in the world of deep learning. But if you still want a list, alright then...... 
1. [Michael Nielson's Deep Learning Book](http://neuralnetworksanddeeplearning.com/): or NNDL, highly recommended by many. This book is very suitable for beginners who want to understand the basic insights of simple feed forward networks and their setups. Unlike most text books, it doesn't quite go through the Math until it gives you some intuition. While I only went through recently, I highly recommend all of you to read it. Also see [my read on the book](/grandjanitor/2016/10/02/reading-michael-nielsons-neural-networks-and-deep-learning/).
2. PRML : I love PRML! Do go to read my [Recommended Books Page](/grandjanitor/2017/10/09/repost-recommended-books-in-machine-learningdeep-learning/) to find out why.
3. Duda and Hart: I don't like it as much as PRML, but it's my first machine learning Bible. Again, go to my [Recommended Books Page](/grandjanitor/2017/10/09/repost-recommended-books-in-machine-learningdeep-learning/) to find out why.
4. T[he Deep Learning Book](http://www.deeplearningbook.org/) by Ian Goodfellow, Yoshua Bengio and Aaron Courville: This is *the* book for deep learning, but it's hardly for beginner. I recently browse through the book. Here is [some quick impression](/grandjanitor/2017/03/10/some-quick-impression-of-browsing-deep-learning/).
5. [Natural Language Understanding with Distributed Representation](http://arxiv.org/abs/1511.07916) by Kyung Hyun Cho. This is mainly for NLP people, but it's important to note how different that NLP is seen from a deep learning point of view.

Others: Check out my [Recommended Books Page](/grandjanitor/2017/10/09/repost-recommended-books-in-machine-learningdeep-learning/). For beginner, I found Mitchell's and Domingo's books are quite interesting. 

## Frameworks

1. [Tensorflow](https://www.tensorflow.org/) : most popular, and could be daunting to install, also check out [TFLearn](http://tflearn.org/). [Keras](https://keras.io/) became the de-facto high-level layer lately.
2. [Torch](http://torch.ch/) : very easy to use even if you don't know Lua. It also leads you to great tutorials. Also check out [PyTorch](https://github.com/pytorch/pytorch).
3. [Theano](http://deeplearning.net/software/theano/) : grandfather of deep learning frameworks, also check out [Lasagne](http://github.com/Lasagne/Lasagne).
4. [Caffe](http://caffe.berkeleyvision.org/) : probably the fastest among the generic frameworks. It takes you a while to understand the setup/syntax.
5. [Neon](https://github.com/NervanaSystems/neon) : the very speedy neon, it's optimized on modern cards. I don't have a benchmarking between caffe and neon yet, but its MNIST training feels very fast.

Others: 
- [deeplearning4j](https://deeplearning4j.org/): obviously in java, but I heard there are great support on enterprise machine learning.

## Tutorials

1. [Theano Tutorial](http://deeplearning.net/tutorial/): a great sets of tutorials and you can run it from CPU.
2. [Tensorflow Tutorial](https://www.tensorflow.org/versions/r0.10/tutorials/image_recognition/index.html) : a very comprehensive sets of tutorial. I don't like it as much as Theano's because some tasks require compilation, which could be fairly painful.
3. [char-rnn](http://karpathy.github.io/2015/05/21/rnn-effectiveness/): not exactly a tutorial but if you want to have *fun* with deep learning. You should train at least one char-rnn. Note that word-based version is available. The package is also optimized now as torch-rnn. I think char-rnn is also a great starting code for intermediate learners to learn Torch.
4. Misc: generally running the examples of a package can teach you a lot. Let's say this is one item.

Others: I also found [Learning Guide from YeravaNN's lab](http://yerevann.com/a-guide-to-deep-learning/) to be fairly impressive. There is ranked resource list on several different topics, which is similar to the spirit of my list. 

## Mailing Lists

1. [(Shameless Plug) AIDL Weekly](http://aidl.io/) Curated by me and [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129), AIDL weekly is a tied-in newsletter of the [AIDL Facebook group](https://www.facebook.com/groups/DeepNetGroup/). We provide in-depth analysis of weekly events of AI and deep learning.
2. [Mapping Babel](https://jack-clark.net/2017/03/06/import-ai-issue-31-evolution-meets-deep-learning-busting-ai-hype-and-the-automatic-analysis-of-cities/) Curated by Jack Clark. I found it entertaining and well-curated. Clark is more in the journalism space and I found his commentary thoughtful.
3. [Data Machina](https://tinyletter.com/datamachina) This is a link only letter. The links are quite quality.

Of course, there are more newsletter than these three. But I don't normally recommend them. One reason is many "curators" don't always read the original sources before they share the links, which sometimes inadvertently spread faked news to the public. In Issue [\#4 of AIDL Weekly](http://aidl.io/issues/4#start), I described one of such incidences. So you are warned! 

## Facebook Forums

That's another category I am going to plug shamelessly. It has to do with most Facebook forums have too much noise and administrator pay too little attention to the group. 
1. (Shameless Plug) [AIDL](https://www.facebook.com/groups/DeepNetGroup/) This is a forum curated by me and [Waikit](https://www.linkedin.com/in/waikit-lau-89129). We like our forum because we actively curate it, delete spam and facilitate discussion within the group. As a result it become one of the most active group. It has 10k+ members. As of this writing, we have a tied-in mailing list as well as a weekly show.
2. [Deep Learning](https://www.facebook.com/groups/DeepLearnng/) Deep Learning has comparable size as AIDL, but less active, perhaps because the administrators use Korean. I still find some of the links interesting and use the group a lot before administering AIDL.
3. [Deep Learning/AI](https://www.facebook.com/groups/1738168866424224/) Curated by [Sid Dharth](https://www.facebook.com/sid027) and [Ish Girwan](https://www.facebook.com/ish.girwan?fref=pb_other). DLAI follows very similar philosophy and Sid control posting tightly. I think his group will be one of the up-and-coming group next year.
4. [Strong Artificial Intelligence ](https://www.facebook.com/groups/strongartificialintelligence/) This is less about deep learning, but more on AI. It is perhaps the biggest FB group on AI, its membership stabilized but posting is solid and there are still some life in discussion. I like the more philosophical ends of the posts which AIDL usually refrained from.

## Non-trivial Mathematics You should Know

Due to popular demand, this section is what I would say a bit on the most relevant Math which you need to know. Everyone knows that Math is useful, and yes, stuffs like Calculus, Linear Algebra, Probability and Statistics are super useful too. But then I think they are too general, so I will name several specific topics which turns out to be very useful, but not very well taught in school. 
1. Bayes' Theorem: Bayes' theorem is important not only as a simple rule which you will use it all the time. The high school version usually just ask you to reverse the end of probabilities. But once it is apply in reasoning, you will need to be very clear how to interpret terms such as likelihood and priors. It's also very important what the term Bayesian really means, and why people see it as better than frequentist. All these thinking if you don't know Bayes' rules, you are going to get very confused.
2. Properties of Multi-variate Gaussian Distribution: The one-dimensional Gaussian distribution is an interesting mathematical quantity. If you try to integrate it, it will be one of the integrals you quickly you can't integrate it in trivial way. That's the point you want to learn the [probability integral](/grandjanitor/2016/01/04/the-probability-integral-2/) and how it was integrated. Of course, once you need to work on multi-variate Gaussian, then you will need to learn further properties such as diagonalizing the covariance matrix and all the jazz. Those are non-trivial Math. But if you master them, it will helps you work through more difficult problems in PRML.
3. Matrix differentiation : You can differentiate all right, but once it comes to vector/matrix, even the notation seems to be different from your college Calculus. No doubt, matrix differentiation is seldom taught in school. So always refer to useful guide such as [Matrix Cook Book](https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf), then you will be less confused. ([Matrix reference manual](http://www.ee.ic.ac.uk/hp/staff/dmb/matrix/intro.html) is also good. )
4. Calculus of Variation: If you want to find the best value which optimize a function you use Calculus, if you want to find the best function/path which optimize a functional, you use Calculus of Variation. For the most part, [Euler-Langrange equation](https://en.wikipedia.org/wiki/Calculus_of_variations#Euler.E2.80.93Lagrange_equation) is what you need.
5. Information theory: information theory is widely used in machine learning. More importantly the reasoning and thinking can be found everywhere. e.g. Why do you want to optimize cross-entropy, instead of square error? Not only[square error over-penalize incorrect outputs](https://jamesmccaffrey.wordpress.com/2013/11/05/why-you-should-use-cross-entropy-error-instead-of-classification-error-or-mean-squared-error-for-neural-network-classifier-training/). You can also think of cross-entropy is learning from the *surprise* of a mistake.

# Blogs You Should Read

1. [Chris Olah's Blog](http://colah.github.io/) Olah has great capability to express very difficult mathematical concepts to lay audience. I greatly benefit from his articles on LSTM and computational graph. He also makes me understand learning topology is fun and profitable.
2. [Andrew Karparthy's Blog ](http://karpathy.github.io/) If you hadn't read "[The Unreasonable Effectiveness of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/)", you should. Karparthy's articles show both great enthusiasm on the topic and very good grasp on the principle. I also like his article on reinforcement learning.
3. [WildML](http://www.wildml.com/about/) Written by Danny Britz, he is perhaps less well-known than either Olah or Karparthy, but he enunciate many topics well. For example, I enjoy his explanation on GRU/LSTM a lot.
4. [Tombone's Computer Vision Blog](http://www.computervisionblog.com/) Written by Tomasz Malisiewicz. This is the first few blogs I read about computer vision, Malisiewicz has great insight on machine learning algorithms and computer vision. Many of his articles give insightful comments on relationship between ML techniques.
5. [The Spectactor ](http://blog.shakirm.com/)written by Shakir Mohamad. This is my goto page on mathematical statistics as well as theoretial basis of deep learning techniques. Check out his thought on what make a ML technique deep, as well as his tricks in machine learning.

That's it for now. Check out this page and I might update with more contents. Arthur

This post is first published at [http://thegrandjanitor.com/2016/08/15/learning-deep-learning-my-top-five-resource/](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/).

You might also like [Learning Machine Learning, Some Personal Experience](/grandjanitor/2016/05/21/learning-machine-learning-some-personal-experience/).

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).

(20160817): I change the title couple of times, because this is more like a top-5 list of a list. So I retitled the post as "top-five resource", "top-five", now I settled to use "top-five list", which is a misnomer but close enough.

(20160817): Fixed couple of typos/wording issues.

(20160824): Add a section on important Math to learn.

(20160826): Fixed Typos, etc.

(20160904): Fixed Typos

(20161002): Changed the section on books to link to my article on NNDL. Added a section on must-follow blogs.

(20170128): As I go deep on Socher's lectures, I boost up his class ranking to number 3. I also made Karparthay's lecture into rank number 2. I think Silver's class is important but the material is too advanced, and perhaps less of importance for deep learning learners. (It is more about reinforcement learning when you look at it closely.) Hinton's class is absolutely crucial but it requires more mathematical understanding than Karparthay's class. Thus the ranking.

I also 2 more classes (NYU, MIT) to check out and 2 more as references (VTech and UA).

(20161207): Added descriptions of Li, Karparthy and Johnson's class, Added description of Silver's class.

(20170310): Add "Philosophy", "Top-Five of Top-Five", "Top-Five Mailing List", "Top-Five Forums". Adjusted description on Socher's class, linked a quick impression on GoodFellow's "Deep Learning".

(20170312): Add Oxford NLP class, Berkeley's Deep RL into the mix.

(20170319): Add the Udacity's course into the mix. I think next version I might have a separate section on reinforcement learning.

(20170326): I did another rewrite last two weeks mainly because there are many new lectures released during Spring 2017. Here is a summary: 

- I separate all "Courses/Lectures" session to two tracks: "Basic Deep Learning" and "Reinforcement Learning". It's more a decluttering of links. I also believe reinforcement learning should be separate track because it requires more specialized algorithms.
- On the "Basic Deep Learning" track, ranking has change. It was Ng's, cs231n, cs224d, Hinton's, Silver's, now it becomes Ng's, cs231n, cs224d, Silvers's, Hinton's. As I go deep into Hinton's class, I found that it has more difficult concepts. Both Silver's and Hinton's class are more difficult than the first 3 IMO.
- I also gives some basic description on the U. of Amsterdam's class. I don't know much about it yet, but it's refreshing because it gives different presentation from the "Basic 5" I recommend.

(20170412): I finished Hinton's NNML, added Berkley CS294-131 into the mix.

(20170620): Links up "Top-5" List with "Basic 5". Added a list of AI, added link to my MOOC list.

(20170816): Added deeplearning.ai into Basic 5. It becomes the new official recommendation to AIDL newcomers.

(20171126): Added several ML classes. Added Stats 385 into the considered list.

Appendix: Links to process: http://ai.berkeley.edu/lecture_videos.html

---

## Comments

**grandjanitor** (2017-09-20):

Hey Khayrat,

I genuinely hope that my articles help you. The strength of the top-5 list I'd say is that its suggested course sequence of learning is quite reasonable for anyone who has college-level calculus. And I'd assume with persistence, you can go quite far just by taking classes.

In any case, I hope you have good luck.

Thanks, Arthur

**Khayrat Glende** (2017-09-18):

Hi Arthur, thank you for sharing your insights. I'm a beginner to ML and fulltime developer with basic math. I've just finished Andrew Ng's ML-course for the second time with an interruption of 3 years where I tried to learn the math, but sadly get confused with where to start and what to learn in which order and made little progress. Also I could follow the explanations in the Andrew's course quit easily, I felt I need more insight. Now is my second attempt to ML and I plan to learn the needed math along the way. Now I was looking for how to proceed . I was thinking about Yaser Abu-Mostafi's course at edx and then turn to the new deeplearning.ia from Andrew. But after reading your advise I think the best way to proceed as you suggested. Best Regards, Khayrat

**Anilkumar ES** (2017-08-18):

Really Very useful information. Thanks a lot! But I am not able to subscribe for new letter. Could you please check it once.

Thank you Anil

> **grandjanitor** (2017-08-18):
>
> Yeah.. My own blog's newsletter subscription is kind of broken. So I might want to remove the options.
>
> I would suggest you to subscribe[AIDL Weekly](http://www.aidl.io), which is also written by me. Thanks!

**grandjanitor** (2017-08-17):

Sure. I will take a look. Thanks!

**TanDo** (2017-08-17):

Awesome reviews and suggestion. Thank you for your article. But I can not subscribe to your blog. Could you please check it ?

**grandjanitor** (2016-08-26):

People adapt NN differently in different applications. e.g. ReLU is usually used in CNN but seldom used in RNN. That's because the ReLU, together with the multiplicative nature of errors could easily blow up the training. On architecture, you may also find that the optimal architecture is application-based and is driven by experiments heavily.

Saying so it doesn't mean you can't use RNN on image recognition , nor you can't use CNN on NLP. It just requires very special care of how you model.

**grandjanitor** (2017-04-12):

You are welcome, chetan. Hope this is useful for you.

**chetan** (2017-04-12):

Thanks for sharing this detailed information about Deep Learning. I am pretty thankful to have you in my network over Fb and thanks again for helping people with your knowledge around the globe.

**johan** (2016-08-26):

this is so awesome resource. thank you for sharing this. i have also just begun my masters (post-grad) research in machine learning (neural networks). i have background of bachelors in electrical engineering.

i have a question of 'how to' nature for research. should the optimization in the neural network algorithm be application specific or should it be general? so for-example, should the application dictate which function of the algorithm be optimized to achieve better results or should one optimize the algorithm in general and then compare it for any application?

**unkle** (2016-08-16):

You should check out https://www.kadenze.com/courses/creative-applications-of-deep-learning-with-tensorflow/info for some really impressive videos and the related course github: https://github.com/pkmital/CADL/ - with complete lecture transcripts in python notebooks.

