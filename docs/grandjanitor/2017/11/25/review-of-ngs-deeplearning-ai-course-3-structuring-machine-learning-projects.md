---
title: "Review of Ng's deeplearning.ai Course 3: Structuring Machine Learning Projects"
date: 2017-11-25
categories: ["Andrew Ng", "deep learning", "Machine Learning"]
tags: ["deep learning", "Machine Learning"]
---

# Review of Ng's deeplearning.ai Course 3: Structuring Machine Learning Projects

*[image not recovered: chris-barbalis-195360.jpg]*

(Also see my review of [Course 1](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/) and [Course 2](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/).)

As you might know, deeplearning.ai courses were released in two batches. The first batch contains Course 1 to 3. And only recently (as of November 15), Course 4, "Convolution Neural Networks" was released. And Course 5 is supposedly released in late November. So Course 3, "Structuring Machine Learning Projects" was more the "final" course in the first batch. It is also a good pause of the first and second half of the course: The first half was more the foundation of deep learning, whereas the second half was more about applications of deep learning.

So here you are, learning something new in deep learning now, isn't it time to apply these new found knowledge? Course 3 says "Hold on!" It turns out before you start to do machine learning, you need to slow down and think about how to plan a task.

In fact, in practice, Course 3 is perhaps the most important course among all the courses in the specialization. The Math in Course 1 may be tougher, and Course 5 could have difficult concepts such as RNN or LSTM which are hard to grok. They are also longer than Course 3 (which only last 2 weeks). But in grand scheme of things, they are not as important as Course 3. I am going to discuss why. 

# What do you actually do as an ML Engineer?

Let me digress a bit: I know many of my readers are young college students who are looking for careers in data science or machine learning. But what do people actually do in the business of machine learning or AI? I think this is a legit question because I was very confused when I first started out.

Oh well, it really depends on how much you are on the development side or research side of your team. Terms like "Research" and "Development" can have various meaning depends on the title. But you can think "researcher" are the people who try to get a new techniques working - usually the criterion is whether it beats the status quo such as accuracy performance. "Developers" on the other hand, are people come up with a production implementation. You can think that many ML jobs are really in between the spectrum of "developers" and "researchers". e.g. I am usually known for my skill as a [architect](https://www.linkedin.com/in/arthchan2003/). That usually means I have the knowledge on both sides. My quote on my skills is usually "50% development and 50% research". There are also people who are highly specialized in either side. But I will focus on the research-side more in this article. 

# So, What do you actually do as an ML Researcher then?

Now I can see a lot of you jump up and say "OH I WANT TO BE A RESEARCHER!" Yes, because doing research is fun, right? You just need to train some models and beat the baseline and write a paper. BOOM! In fact, if you are good, you just need to ask people to do your research. Woohoo, you are happy and done, right?

Oh well, in reality, good researchers are usually fairly good coders themselves. Especially in applied field such as machine learning, my guess is out of 100 researchers in an institute, may be there is perhaps 1 person who is really a "thinking staff". i.e. They do nothing other than coming up with new theory or writing proposal. Just like you, I admire the life of a pure academician. But in our time, you usually have to be either very smart and very lucky to be one of them. (There is a tl;dr explanation here, but it is out of scope of this article.)

"Okay, okay, got it..... so can we start to have some fun now? We just need to do *some coding*, right? " Not really, the first step *before* you can work on fun stuffs such as modeling, or implement new algorithm, is to clean-up data. So say if you work on a fraudulent transaction detection, the first is to load a giant table somewhere so that you can query it and get the training data. Then you want to clean the data, and massage the data so that it can be an input of ML engine. Notice that by themselves these tasks can be non-trivial as well. 

# Course 3: Structuring Machine Learning Projects

Then there you are, after you code, you clean up your data, finally you have some time to do machine learning. Notice that your time after all these "chores" are actually quite limited. That makes *how to use your time effectively* a very important topic. And here comes why you want to take Course 3: Andrew teaches you the basics of how to assign time/resource in a deep learning task. e.g. How large are your train/validation/test sets? When should you stop your development? What is human performance? What if there are mismatches between your train set/test set? If you are stuck, should you tune your hyperparemeters more? Or should you regularize?

In a way, Course 3 is a reminiscence of "Machine Learning"'s Week 6 and Week 11, basically what you try to learn is to make good "meta-decision"e of all your projects you will work for your life time. I also think it's the *right stuffs* in your ML career.

One final note: as you might notice in my last two reviews, I usually tried to compare deeplearning.ai with other classes. But Course 3 is quite unique, so you might only find similar material on machine learning course which focus on theory. But Ng's treatment is unique: first what he gave is practical and easy to understand advice. Then his advice focused on deep learning - while we are talking about similar principle. Working on deep learning usually implies special circumstance - such as close to human performance, and you might just have low train and test set performance. Those scenarios did appear in the past - but only in cutting edge ML evaluation involved the best ML teams. So you don't normally hear about it in a course, but now Andrew tell you all. Doesn't that worth the price of $49? :) 

# Conclusion

So here you have it. This is my review of Course 3 of deeplearning.ai. Surprising even to me, I actually write more than I expect for these two-week course. Perhaps the main reason is - I really hope this course were there say 3 years ago. This would have change the course of some projects I develop.

May be it's too late for me..... but if you are early in deep learning, do recognize the importance of Course 3, or any advices you hear similar to what Course 3 taught. It will save you much time - not just on one ML task but many ML tasks you will work in your career.

Arthur Chan

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me (Arthur) at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).

---

## Comments

**Mohammad T Islam** (2017-11-26):

As usual, a great review !

I also wish I knew these concepts three/four years ago. But hey ! maybe now I can go back and polish my old papers to publish some more with better results! :)

