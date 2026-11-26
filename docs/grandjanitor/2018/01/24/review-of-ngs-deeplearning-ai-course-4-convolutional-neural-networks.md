---
title: "Review of Ng's deeplearning.ai Course 4: Convolutional Neural Networks"
date: 2018-01-24
categories: ["deep learning", "Machine Learning"]
---

# Review of Ng's deeplearning.ai Course 4: Convolutional Neural Networks

*[image not recovered: Number4.jpg]*

(You can find my reviews on previous courses here: [Course 1,](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/) [Course 2](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/) and [Course 3](/grandjanitor/2017/11/25/review-of-ngs-deeplearning-ai-course-3-structuring-machine-learning-projects/). )

Time flies, I finished Course 4 around a month ago and finally have a chance to write a full review. Course 4 is different from the first three deeplearning.ai courses, which focused on fundamental understanding of deep learning topics such as back propagation ([Course 1](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/)) , tuning hyperparameters ([Course 2](/grandjanitor/2017/10/28/review-of-ngs-deeplearning-ai-course-2-improving-deep-neural-networks/)) and decide what improvement strategy is the best ([Course 3](/grandjanitor/2017/11/25/review-of-ngs-deeplearning-ai-course-3-structuring-machine-learning-projects/)) . Course 4 is more about an important application of deep learning: computer vision.

Focusing on computer vision make designing Course 4 subjects to a distinct challenges as a course: how does Course 4 scales up with other existing computer vision class? Would it be comparable with the greats such as Stanford cs231n? For these questions, I will do a comparison between Course 4 and cs231n in this article. My goal is to answer how you would choose between the two classes in your learning process. 

# Convolutional Neural Network In the Context of Deep Learning

Convolutional neural networks (CNN) has a very special place in deep learning. For the most part, you can think of it as interesting special case of a vanilla feed-forward network with parameters tied. Computationally, you can parallelize it much better than technique such as recurrent neural networks. Of course, it is prominent in image classification (since [LeNet-5](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf)). But then it is also frequently used in sequence modeling such as speech recognition and text classification (check out [cs224n](http://web.stanford.edu/class/cs224n/) for details). I guess, more importantly, since image classification is also used a template of development in many other newer application. It makes learning CNN sort of mandatory for students of deep learning. 

# Learning Deep-Learning-based Computer Vision before deeplearning.ai

Interesting enough, there is a rather standard option to learning deep learning-based computer vision on-line. Yes! You guess it right! It is [cs231n ](http://cs231n.stanford.edu/)which used to be taught by then Stanford PhD candidates, [Andrej Karpathy](https://cs.stanford.edu/people/karpathy/) in 2015/16. [1] To recap, cs231n is not only a good class for computer vision, it is also a good class for learning basics of deep learning. Also as now famous Dr. Karpathy [said](https://medium.com/@karpathy/yes-you-should-understand-backprop-e2f06eab496b), it has probably one of the best explanation of back-propagation. My only criticism for the class (as I mentioned in [earlier reviews](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/)) is that as a first class, it is too focused on image recognition. But as a first class of deep-learning-based computer vision, I think it was the best. 

# Course 4: Convolutional Neural Networks Briefly

Would Course 4 changes my opinion about cs231n then? I guess we should look at it in perspective. Comparing Course 4 with cs231n is comparing orange and apple. Course 4 is a month-long class which is suitable for absolute beginners. If you look into it course 4 basically is a quick introductory class. Week 1 focuses on what CNN is, Week 2 and 3 talks about 2 prominent applications: image classification, image detection. Whereas Week 4 are about fun stuffs such as face verification and image transfer.

Many people I know finish the class within 3 days when the class started. Whereas cs231n is a semester-long course which contain ~18 hours of video to watch with more substantial (and difficult) homework problems. It is more suitable for people who already have at least one or two machine learning full courses at their belt.

So my take is that Course 4 can be a good first class of deep-learning-based computer vision, *but it is not a replacement of cs231n*. So if you only took Course 4, you will find that there are still a lot in computer vision you don't grok. My advice is *you should then audit cs231n afterward*, or else your understanding would still have holes. 

# What if I already took cs231n? Would Course 4 still helps me?

Absolutely. While Course 4 is much shorter - remember that a lot of deep learning concepts are obscure. It doesn't hurt to learn the same thing in different ways. And Course 4 offer different perspectives on several topics: 
- For starter, Course 4, just like all other deeplearning.ai has homework which require code verification at every step. As I argued in [an earlier review](/grandjanitor/2017/10/14/review-of-ngs-deeplearning-ai-course-1-neural-networks-and-deep-learning/), that's a huge plus for learning.
- Then there is the treatment of individual topics, I found that Ng's treatment on image detection is refreshing - the more conventional view (which cs231n took) was to start from RCNN and its two faster variants, then bring up YOLO. But Andrew just decide to go with YOLO instead. Notice that neither of the classes had gave detail description of the algorithm. (Reading the paper is probably the best.) But YOLO is indeed more practical than RCNN variants.
- On Week 4 about applications, such as face verification and Siamese networks are actually new to me. Andrew also give a very nice explanation on why image transfer really works.
- As always, even a new note for old topics matter. E.g. This is the first time I am aware the convolution in deep learning is different from convolution in signal processing. (See Week 1). I also found that Andrew's note on various image classification papers are gems. Even if you you read those paper, I do suggest you to listen to him again.

# Weakness(es)

Since I admin an[unofficial forum](https://www.facebook.com/groups/DeepLearningAISpecialization/?ref=bookmarks) for the course, I learn that there are fairly obvious problems with the courses. For example, back in December when I took the course, there is one homework you need to submit an algorithm which wouldn't match the notebook. Also, there was also a period of time where submission was very slow, which I need to fix the file downloading to straighten it up. I do think those are frustrating issue. Hopefully, by the time when you read this article, the staff has already fixed the issues. [2]

To be fair, even the great NNML by Hinton has glitches here and there in their homeworks. So I am not entirely surprised glitches happen in deeplearning.ai. Of course, I would still highly recommend the class. 

# Conclusion

There you have it - I reviewed Course 4 of deeplearning.ai. Unlike earlier parts of the courses, Course 4 has a very obvious competitor: cs231n. And I don't quite put Course 4 as the one course you can take and master computer vision.  My belief is you need to go through both Course4 and cs23n to have reasonable understanding. 

But as a first class of DL-based computer vision. I still think Course 4 has tremendous value. So once again I highly recommend yo all to take the class.

As a final note, I was able to catch up reviews for all classes in deeplearning.ai. Now all eyes on Course 5 and currently (as of Jan 23), it is set to launch at Jan 31. Before that, do check out ourforum AIDL and Coursera deeplearning.ai for more discussion!

Arthur Chan

First published at http://thegrandjanitor.com/2018/01/24/review-of-ngs-deeplearning-ai-course-4-convolutional-neural-networks/

If you like this message, subscribe the Grand Janitor Blog's RSS feed. You can also find me (Arthur) at [twitter](https://twitter.com/arthchan2003), [LinkedIn](https://www.linkedin.com/in/arthchan2003), [Plus](https://plus.google.com/), [Clarity.fm](https://clarity.fm/arthurchan). Together with [Waikit Lau](https://www.linkedin.com/in/waikit-lau-89129?authType=OPENLINK&authToken=ECvg&locale=en_US&srchid=32591551472085290618&srchindex=1&srchtotal=1&trk=vsrp_people_res_name&trkInfo=VSRPsearchId%3A32591551472085290618%2CVSRPtargetId%3A58285%2CVSRPcmpt%3Aprimary%2CVSRPnm%3Atrue%2CauthType%3AOPENLINK), I maintain the [Deep Learning Facebook forum](https://www.facebook.com/groups/DeepNetGroup/). Also check out my awesome employer: [Voci](https://www.linkedin.com/company/9382025?trk=tyah&trkInfo=clickedVertical%3Acompany%2CclickedEntityId%3A9382025%2Cidx%3A2-1-2%2CtarId%3A1472085172997%2Ctas%3Avoci).

Footnotes:

[1] Funny enough, while I went through all cs231n 2016 videos a while ago, I never wrote a review about the course.

[2] As a side note, I think it has to do with Andrew and the staffs are probably rushing to create the class. That's why I was actually relieved when I learn that Course 5 will be released in January. Hopefully this gives more time for the staffs to perfect the class.
