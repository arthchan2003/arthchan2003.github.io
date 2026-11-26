---
title: "What is the Difference between Deep Learning and Machine Learning?"
date: 2017-07-09
categories: ["deep learning", "deep neural network", "DNN", "Machine Learning", "Natural Language Processing"]
tags: ["deep learning", "Machine Learning"]
---

# What is the Difference between Deep Learning and Machine Learning?

*[image not recovered: question-mark-2123967_1920.jpg]*

AIDL member [Bob Akili](https://www.facebook.com/bob.akili.90?fref=ufi) asked (rephrased): 

> What is the Difference between Deep Learning and Machine Learning?

Usually I don't write a full blog message to answer member's questions. But what is "deep" is such a fundamental concept in deep learning, yet there are many well-meaning but incorrect answers floating around. So I think it is a great idea to answer the question clearly and hopefully disabuse some of the misconceptions as well. Here is a cleaned up and expanded version of my comment to the [thread](https://www.facebook.com/groups/DeepNetGroup/permalink/466714983721389/). 

# Deep Learning is Just a Subset of Machine Learning

First of all deep learning is just a subset of techniques of machine learning. You may heard from many "Deep Learning Consultants"-type: "deep learning is completely different from from Machine Learning". But then when we are talking about "deep learning" these days, we are really talking about "neural networks which has more than one layer". Since neural network is just one type of ML techniques, it doesn't make any sense to call DL as "different" from ML. It might work for marketing purpose, but the thought was clearly misleading. 

# Deep Learning is a kind of Representation Learning

So now we know that deep learning is a kind of machine learning. We still can't quite answer why it is special. So let's be more specific, deep learning is a kind of [representation learning](https://en.wikipedia.org/wiki/Feature_learning). What is representation learning? Representation learning is an opposite of another school of thought/practice: [feature engineering](https://en.wikipedia.org/wiki/Feature_engineering). In feature engineering, humans are supposed to hand-craft features to make machine works better. If you Kaggle before, this should be obvious to you, sometimes you just want to manipulate the raw inputs and create new feature to represent your data.

Yet in some domains which involve high-dimensional data such as images, speech or text, hand-crafting feature was found to be very difficult. e.g. Using HOG type of approaches to do computer vision usually takes a 4-5 years of a PhD student. So here we come back to representation learning - can computer automatically learn good features? 

# What is a "Deep" Technique?

Now we come to the part why deep learning is "deep" - usually we call a method "deep" when we are optimizing a** nested function** in the method. So for example, if you can express such functions as a graph, you would find that it has multiple layers. *The term "deep" really is describing such "nestedness".* That should explain why we typically called any artificial neural network (ANN) with more than 1 hidden layer as "deep". Or the general saying, "deep learning is just neural network which has more layers".

(Another appropriate term is "hierarchical". See footnote [4] for more detail.)

This is also the moment Karpathy in cs231n will show you the multi-layer CNN such that features are automatically learned from the simplest to more complex one. Eventually your last layer can just differentiate them using a linear classifier. As there is a "deep" structure that learn the right feature (last layer). Note the key term here is "automatic", all these Gabor-filter like feature are not hand-made. Rather, they are results from back-propagation [3]. 

# Are there Anything which is "Deep" but not a Neural Network?

Actually, there are plenty, [deep Boltzmann machine](http://proceedings.mlr.press/v5/salakhutdinov09a/salakhutdinov09a.pdf)? [deep belief network](https://en.wikipedia.org/wiki/Deep_belief_network)? [deep Gaussian process](http://proceedings.mlr.press/v31/damianou13a.pdf)? They are still discussed in unsupervised learning using neural network, but I always found that knowledge of graphical models is more important to understand them. 

# So is Deep Learning also a Marketing Term?

Yes and no. It depends on who you talk to. If you talk with ANN researchers/practitioners, they would just tell you "deep learning is just neural network which has more than 1 hidden layer". Indeed, if you think from their perspective, the term "deep learning" could just be a short-form. Yet as we just said, you can also called other methods "deep". So the adjective is not totally void of meaning. But many people would also tell you that because "deep learning" has become such a marketing term, it can now mean many different things. I will say more in next section.

Also the term "deep learning" has been there for a century. Check out Prof. Schmidhuber's [thread](https://plus.google.com/100849856540000067209/posts/7N6z251w2Wd) for more details? 

# "No Way! X is not Deep but it is also taught in Deep Learning Class, You made a Horrible Mistake!"

I said it with much authority and I know some of you guys would just jump in and argue:

"What about [word2vec](https://en.wikipedia.org/wiki/Word2vec)? It is nothing deep at all, but people still call it Deep learning!!!" "What about all wide architectures such as "[wide-deep learning](https://arxiv.org/abs/1606.07792)"?" "Arthur, You are Making a HORRIBLE MISTAKE!"

Indeed, the term "deep learning" is being abused these days. More learned people, on the other hand, are usually careful to call certain techniques "deep learning" For example, in cs221d 2015/2016 lectures, Dr. Richard Socher was quite cautious to call word2vec as "deep". His supervisor, Prof. Chris Manning, who is an authority in NLP, is known to dispute whether deep learning is always useful in NLP, simply because some recent advances in NLP really due to deep learning [1][2].

I think these cautions make sense. Part of it is that calling everything "deep learning" just blurs what really should be credited in certain technical improvement. The other part is we shouldn't see deep learning as the only type of ML we want to study. There are many ML techniques, some of them are more interesting and practical than deep learning in practice. For example, deep learning is not known to work well with small data scenario. Would I just yell at my boss and say "*Because I can't use deep learning, so I can't solve this problem*!"? No, I would just test out random forest, support vector machines, GMM and all these nifty methods I learn over the years. 

# Misleading Claim About Deep Learning (I) - "Deep Learning is about Machine Learning Methods which use a lot of Data!"

So now we come to the arena of misconceptions, I am going to discuss two claims which many people have been drumming about deep learning. But neither of them is the right answer to the question "What is the Difference between Deep and Machine Learning?

The first one you probably heard all the time, "Deep Learning is about ML methods which use a lot of data". Or people would tell you "Oh, deep learning *just* use a lot of data, right?" This sounds about right, deep learning in these days does use a lot of data. So what's wrong with the statement?

Here is the answer: while deep learning does use a lot of data, *before deep learning*, *other techniques use tons of data too!* e.g. Speech recognition before deep learning, i.e. HMM+GMM, can use up to 10k hours of speech. Same for SMT. And you can do SVM+HOG on Imagenet. And more data is always better for those techniques as well. So if you say "deep learning use more data", then you forgot the older techniques also can use more data.

What you can claim is that *"deep learning is a more effective way to utilize data".*  That's very true, because once you get into either GMM or SVM, they would have scalability issues. GMM scales badly when the amount of data is around 10k hour. SVM (with RBF-kernel in particular) is super tough/slow to use when you have ~1 million point of data. 

# Misleading Claim About Deep Learning II - "Deep Learning is About Using GPU and Having Data Center!"

This particular claim is different from the previous "Data Requirement" claim, but we can debunk it in a similar manner. The reason why it is wrong? Again *before deep learning, people have GPUs to do machine learning* *already.* For example, you can use GPU to speed up GMM. Before deep learning is hot, you need a cluster of machines to train acoustic model or language model for speech recognition. You also need tons of RAM to train a language model for SMT. So calling GPU/Data Center/RAM/ASIC/FPGA a differentiator of deep learning is just misleading.

You can say though "*Deep Learning has change the computational model from distributed network model to more a single machine-centric paradigm (which each machine has one GPU). But later approaches also tried to combine both CPU-GPU processing together".*  

# Conclusion and "What you say is Just Your Opinion! My Theory makes Equal Sense!"

Indeed, you should always treat what you read on-line with a grain of salt. Being critical is a good thing, having your own opinion is good. But you should also try to avoid *equivocate* an issue. Meaning: sometimes things have only one side, but you insist there are two equally valid answers. If you do so, you are perhaps making a logical error in your thinking. And a lot of people who made claims such as "deep learning is learning which use more data and use a lot of GPUS" are probably making such thinking errors.

Saying so, I would suggest you to read several good sources to judge my answer, they are: 
1. Chapter 1 of[Deep Learning](http://www.deeplearningbook.org/contents/intro.html).
2. Shakir's Machine Learning Blog on a [Statistical View of Deep Learning](http://blog.shakirm.com/ml-series/a-statistical-view-of-deep-learning/). In particular, part VI, "[What is Deep?](http://blog.shakirm.com/2015/06/a-statistical-view-of-deep-learning-vi-what-is-deep/)"
3. Tombone's post on [Deep Learning vs Machine Learning vs Pattern Recognition ](http://www.computervisionblog.com/2015/03/deep-learning-vs-machine-learning-vs.html)

In any case, I hope that this article helps you. I thank Bob to ask the question, [Armaghan Rumi Naik](https://www.facebook.com/rumi.naik?fref=ufi) has debunked many misconceptions in the original [thread](https://www.facebook.com/groups/DeepNetGroup/permalink/466714983721389/) - his understanding on machine learning is clearly above mine and he was able to point out mistakes from other commenters. It is worthwhile for your reading time. 

# Footnotes

[1] See "[Last Words: Computational Linguistics and Deep Learning](http://mitp.nautil.us/article/170/last-words-computational-linguistics-and-deep-learning)" [2] Generally whether DL is useful in NLP is widely disputed topic. Take a look of Yoav Goldberg's view on some recent[GAN results on language generation](https://medium.com/@yoav.goldberg/an-adversarial-review-of-adversarial-generation-of-natural-language-409ac3378bd7). AIDL Weekly #18 also gave an [expose](http://aidl.io/issues/18#start) on the issue. [3] Perhaps another useful term is "hierarchical". In the case of ConvNet the term is right on. As [Eric Heitzman](https://www.facebook.com/eric.heitzman?fref=ufi) comments at AIDL: "(deep structure) They are \*not\* necessarily recursive, but they \*are\* necessarily hierarchical since layers always form a hierarchical structure." After Eric's comment, I think both "deep" and "hierarchical" are fair terms to describe methods in "deep learning". (Of course, "hierarchical learning" is a much a poorer marketing term.) [4] In earlier draft. I use the term recursive to describe the term "deep", which as [Eric Heitzman](https://www.facebook.com/eric.heitzman?fref=ufi) at AIDL, is not entirely appropriate. "Recursive" give people a feeling that the function is self-recursive or$f(f( \ldots f(f(*))))$. but actual function are more "nested", like $f_1(f_2( \ldots f_{n-1}(f_n(*))))$. As a result, I removed the term "recursive" but just call the function "nested function". Of course, you should be aware that my description is not too mathematically rigorous neither. (I guess it is a fair wordy description though)

History: 20170709 at 6: fix some typos.

20170711: fix more typos.

20170711 at 7:05 p.m.: I got a feedback from [Eric Heitzman](https://www.facebook.com/eric.heitzman?fref=ufi) who points out that the term "recursive" can be deceiving. Thus I wrote footnote [4].

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me (Arthur) at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).
