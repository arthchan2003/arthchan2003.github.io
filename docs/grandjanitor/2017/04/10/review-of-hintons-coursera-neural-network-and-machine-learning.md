---
title: "A Review on Hinton's Coursera \"Neural Networks and Machine Learning\""
date: 2017-04-10
categories: ["DBN", "deep leaerning", "deep learning", "deep neural network", "energy-based models", "ESN", "Geoff Hinton", "Machine Learning", "RBM", "recurrent neural network"]
tags: ["CNN", "DBN", "deep learning", "DNN", "ESN", "Machine Learning", "RBM", "RNN"]
---

# A Review on Hinton's Coursera "Neural Networks and Machine Learning"

*[image not recovered: CajalCerebellum.jpg]*

Cajal's drawing chick cerebellum cells, from Estructura de los centros nerviosos de las aves, Madrid, 1905

For me, finishing [Hinton's deep learning class](https://www.coursera.org/learn/neural-networks), or Neural Networks and Machine Learning(NNML) is a long overdue task. As you know, the class was first launched back in 2012. I was [not so convinced by deep learning back then](/grandjanitor/2016/05/21/learning-machine-learning-some-personal-experience/). Of course, my mind changed at around 2013, but the class was archived. Not until 2 years later I decided to take [Andrew Ng's class on ML](/grandjanitor/2015/11/11/for-the-not-so-uninitiated-review-of-ngs-coursera-machine-learning-class/), and finally I was able to loop through the Hinton's class once. But only last year October when the class relaunched, I decided to take it again, i.e watch all videos the second times, finish all homework and get passing grades for the course. As you read through my journey, this class is *hard.*  So some videos I watched it 4-5 times before groking what Hinton said. Some assignments made me takes long walks to think through. Finally I made through all 20 assignments, even bought a [certificate](https://www.coursera.org/account/accomplishments/verify/7GYP3JRLCRD3) for bragging right; It's a refreshing, thought-provoking and satisfying experience.

So this piece is my review on the class, why you should take it and when. I also discuss one question which has been floating around forums from time to time: Given all these deep learning classes now, is the Hinton's class outdated? Or is it still the best beginner class? I will chime in on the issue at the end of this review. 

# The Old Format Is Tough

I admire people who could finish this class in the Coursera's old format. NNML is well-known to be much harder than [Andrew Ng's Machine Learning](https://www.coursera.org/learn/machine-learning) as multiple reviews said ([here](https://www.quora.com/What-are-your-reviews-on-Geoffrey-Hintons-coursera-course-on-neural-networks), [here](http://ketnowledge.blogspot.com/2013/03/reviews-of-some-coursers-courses-that-i.html)). Many of my friends who have PhD cannot quite follow what Hinton said in the last half of the class.

No wonder: at the time when Kapathay [reviewed it in 2013](https://plus.google.com/+AndrejKarpathy/posts/4FtyNBN5A38), he noted that there was an influx of non-MLers were working on the course. For new-comers, it must be mesmerizing for them to understand topics such as energy-based models, which many people have hard time to follow. Or what about deep belief network (DBN)? Which people these days still mix up with deep neural network (DNN). And quite frankly I still don't grok some of the proofs in lecture 15 after going through the course because deep belief networks are difficult material.

The old format only allows 3 trials in quiz, with tight deadlines, and you only have one chance to finish the course. One homework requires deriving the matrix form of backprop from scratch. All of these make the class unsuitable for busy individuals (like me). But more for second to third year graduate students, or even experienced practitioners who have plenty of time (but, who do?). 

# The New Format Is Easier, but Still Challenging

I took the class last year October, when Coursera had changed most classes to the new format, which allows students to re-take. [1] It strips out some difficulty of the task, but it's more suitable for busy people. That doesn't mean you can go easy on the class : for the most part, you would need to review the lectures, work out the Math, draft pseudocode etc. The homework requires you to derive backprop is still there. The upside: you can still have all the fun of deep learning. :) The downside: you shouldn't expect going through the class without spending 10-15 hours/week. 

# Why the Class is Challenging - I: The Math

Unlike Ng's and [cs231n](http://cs231n.stanford.edu/), NNML is not too easy for beginners without background in calculus. The Math is still not too difficult, mostly differentiation with chain rule, intuition on what Hessian is, and more importantly, vector differentiation - but if you never learn it - the class would be over your head. Take at least Calculus I and II before you join, and know some basic equations from the [Matrix Cookbook](http://www2.imm.dtu.dk/pubdb/views/edoc_download.php/3274/pdf/imm3274.pdf). 

# Why the Class is Challenging - II: Energy-based Models

Another reason why the class is difficult is that last half of the class was all based on so-called energy-based models. i.e. Models such as Hopfield network (HopfieldNet), Boltzmann machine (BM) and restricted Boltzmann machine (RBM). Even if you are used to the math of supervised learning method such as linear regression, logistic regression or even backprop, Math of RBM can still throw you off. No wonder: many of these models have their physical origin such as [Ising model](https://en.wikipedia.org/wiki/Ising_model). Deep learning research also frequently use ideas from Bayesian networks such as [explaining away](http://stats.stackexchange.com/questions/54849/why-does-explaining-away-make-intuitive-sense). If you have no basic background on either physics or Bayesian networks, you would feel quite confused.

In my case, I spent quite some time to Google and read through relevant literature, that power me through some of the quizzes, but I don't pretend I understand those topics because they can be deep and unintuitive. 

# Why the Class is Challenging - III: Recurrent Neural Network

If you learn RNN these days, probably from [Socher's cs224d](http://cs224d.stanford.edu/) or by reading Mikolov's thesis. [LSTM](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) would easily be your only thought on how to resolve exploding/vanishing gradients in RNN. Of course, there are other ways: [echo state network](http://www.scholarpedia.org/article/Echo_state_network) (ESN) and Hessian-free methods. They are seldom talked about these days. Again, their formulation is quite different from your standard methods such as backprop and gradient-descent. But learning them give you breadth, and make you think if the status quote is the right thing to do. 

# But is it Good?

You bet! Let me quantify the statement in next section. 

# Why is it good?

Suppose you just want to *use* some of the fancier tools in ML/DL, I guess you can just go through Andrew Ng's class, test out bunches of implementations, then claim yourself an expert - That's what many people do these days. In fact, Ng's Coursera class is designed to give you a taste of ML, and indeed, you should be able to wield many ML tools after the course.

That's said, you should realize your understanding of ML/DL is still .... rather shallow. May be you are thinking of "Oh, I have a bunch of data, let's throw them into Algorithm X!". "Oh, we just want to use XGBoost, right! It always give you the best results!" You should realize *performance number isn't everything*. It's important to understand what's going on with your model. You easily make costly short-sighted and ill-informed decision when you lack of understanding. It happens to many of my peers, to me, and sadly even to some of my mentors.

Don't make the mistake! Always seek for better understanding! Try to [grok](https://en.wikipedia.org/wiki/Grok). If you only do Ng's neural network assignment, by now you would still wonder how it can be applied to other tasks. Go for Hinton's class, feel perplexed by the Prof said, and iterate. Then you would *start* to build up a better understanding of deep learning.

Another more technical note: if you want to learn deep unsupervised learning, I think this should be the first course as well. Prof. Hinton teaches you the intuition of many of these machines, you will also have chance to implement them. For models such as Hopfield net and RBM, it's quite doable if you know basic octave programming. 

# So it's good, but is it outdated?

Learners these days are perhaps luckier, they have plenty of choices to learn deep topic such as deep learning. Just check out my own "[Top 5-List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)". cs231n, cs224d and even Silver's class are great contenders to be the second class.

But I still recommend NNML. There are four reasons: 
1. It is deeper and tougher than other classes. As I explained before, NNML is tough, not exactly mathematically (Socher's, Silver's Maths are also non-trivial), but conceptually. e.g. energy-based model and different ways to train RNN are some of the examples.
2. Many concepts in ML/DL can be seen in different ways. For example, bias/variance is a trade-off for frequentist, but it's seen as "frequentist illusion" for Bayesian. Same thing can be said about concepts such as backprop, gradient descent. Once you think about them, they are tough concepts. So one reason to take a class, is not to just teach you a concept, but to allow you to look at things from different perspective. In that sense, NNML perfectly fit into the bucket. I found myself thinking about Hinton's statement during many long promenades.
3. Hinton's perspective - Prof Hinton has been mostly on the losing side of ML during last 30 years. But then he persisted, from his lectures, you would get a feeling of how/why he starts a certain line of research, and perhaps ultimately how you would research something yourself in the future.
4. Prof. Hinton's delivery is humorous. Check out his view in Lecture 10 about why physicists worked on neural network in early 80s. (Note: he was a physicist before working on neural networks.)

# Conclusion and What's Next?

All-in-all, Prof. Hinton's "Neural Network and Machine Learning" is a must-take class. All of us, beginners and experts include, will be benefited from the professor's perspective, breadth of the subject.

I do recommend you to first take the Ng's class if you are absolute beginners, and perhaps some Calculus I or II, plus some Linear Algebra, Probability and Statistics, it would make the class more enjoyable (and perhaps doable) for you. In my view, both Kapathy's and Socher's class are perhaps easier second class than Hinton's class.

If you finish this class, make sure you check out other fundamental classes. Check out my post "[Learning Deep Learning - My Top 5 List](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)", you would have plenty of ideas for what's next. A special mention here perhaps is Daphne Koller's [Probabilistic Graphical Model](https://www.coursera.org/learn/probabilistic-graphical-models), which I found equally challenging, and perhaps it will give you some insights on very deep topics such as Deep Belief Network as well.

Another suggestion for you: may be you can take the class again. That's what I plan to do about half a year later - as I mentioned, I don't understand every single nuance in the class. But I think understanding would come up at my 6th to 7th times going through the material.

Arthur Chan

[1] To me, this makes a lot of sense for both the course's preparer and the students, because students can take more time to really go through the homework, and the course's preparer can monetize their class for infinite period of time.

History:

(20170410) First writing (20170411) Fixed typos. Smooth up writings. (20170412) Fixed typos (20170414) Fixed typos.

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me (Arthur) at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).

---

## Comments

**Andreas** (2017-11-25):

"Many of my friends who have PhD cannot quite follow what Hinton said in the last half of the class." Thanks for that sentence! I was really not sure if I was just too dumb to follow. These energy based models are highly interesting to me but still I struggle to understand them and some other his material. Good to hear that other, supposedly smarter guys have similar problems.

> **grandjanitor** (2017-11-25):
>
> Indeed. You should also understand that energy-based model was much less known than discriminative models. So unless you have a background in graphical model or statistical thermodynamics. The Math would look foreign to you. That's probably the true reason why my PhD friends are more confused than they should.

**Rafael** (2018-03-29):

Oh, I was reading this after searching about this course on google and it was a very good read. I was surprised to see "Arthur Chan" at the end, since you are the legendary admin on the facebook deep learning group.

Anyway, I'm still in lecture 7. The ones before it weren't so difficult. I found the assignments were on the easy side too since I didn't really need to write anything, just pick the right choice.

But now lecture 7 is quite hard, and you said it will only get harder. It's weird because I do understand markov models somehow so I thought it wouldn't be so hard, but it doesn't look like Geoffrey explained what is a RNN. I'm not sure if I need to go to the course knowing that, but I guess I will need to watch some other lectures (luckily you have some courses on your top five that I can probably learn more about those).

