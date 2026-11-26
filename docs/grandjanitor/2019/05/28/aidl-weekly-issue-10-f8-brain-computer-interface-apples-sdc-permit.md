---
title: "AIDL Weekly Issue 10 - F8, Brain-Computer Interface, Apple's SDC Permit"
date: 2019-05-28
---

# AIDL Weekly Issue 10 - F8, Brain-Computer Interface, Apple's SDC Permit

## Editorial

### Thoughts From Your Humble Curators

The next big platform everyone will be fighting over is your mind. Check out Elon Musk's Neuralink and Facebook's brain-typing and skin-hearing. 

Last week also featured F8, which happened on April 18th and 19th. F8 gave us another week filled with some far-out news: Augmented reality? Caffe2.ai? Brain computer interface? Check, check and check. We have 4 items in this issue which cover all these cool stuffs.

We also had a very interesting live-streamed office hour with Sumit Gupta, VP of HPC, AI and Machine Learning at IBM. We went in-depth into what Sumit thinks are bottlenecks in Deep Learning today and other topics. Check out the video below.

Other than F8 and the IBM interview, we also cover: 
- Development of SDC, by Apple and Baidu,
- [Neuralink](https://techcrunch.com/2017/04/20/elon-musks-neuralink-wants-to-turn-cloud-based-ai-into-an-extension-of-our-brains/) and its criticism.

As always, if you like our newsletter, subscribe and forward it to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## News

### [Facebook AI in Augmented Reality](https://www.wired.com/2017/04/facebooks-augmented-reality-engine-brings-ai-right-phone/)

FB is turning to the humble camera as the next platform. FB envisions AR to be universal from simple Snapchat style of face filter to "why buy a physical TV when you can buy a $1 app that *is* a TV projected in AR?". This path would require lots of visual detection, object recognition and SLAM-type techniques for virtual agents to check their own location and update mapping. As Mark Zuckerberg stressed that AR is Facebook's 2nd Act, AI will also be more the DNA within Facebook. 

[wired.com](https://www.wired.com/2017/04/facebooks-augmented-reality-engine-brings-ai-right-phone/)

---

### [Neuroscientists weigh in on Neurolink](http://spectrum.ieee.org/the-human-os/biomedical/devices/5-neuroscience-experts-weigh-in-on-elon-musks-mysterious-neural-lace-company)

By now, we all learn about [Neuralink](http://www.theverge.com/2017/3/27/15077864/elon-musk-neuralink-brain-computer-interface-ai-cyborgs) which is a new company by Elon Musk on creating new [brain-computer interface (BCI)](https://en.wikipedia.org/wiki/Brain%E2%80%93computer_interface). If it is the first time you heard about BCI, it is more mature than you thought. For example, [one treatment of Parkinson's disease](http://www.parkinson.org/understanding-parkinsons/treatment/surgery-treatment-options/Deep-Brain-Stimulation) is to surgically insert wire into thalamus of the brain and emulate a normal brain stimulus within the region. So far, there are around 150k Parkinson's patients received such treatment. Of course, there are also know cases [where a mind-reading device could be implanted](https://www.technologyreview.com/s/603512/reached-via-a-mind-reading-device-deeply-paralyzed-patients-say-they-want-to-live/) to stroke's patients, which allow them to communicate with the outside world. 

On the other hand, any invasive procedures such as surgery can easily cause issues like infections. So usually any BCI technique is used a last resort. And new inventions are usually heavily regulated.

Musk seems to have a different approach. In the past, one method he mentioned in various conferences/interview (see this [tweet](https://twitter.com/elonmusk/status/824182237352562688?ref_src=twsrc%5Etfw&ref_url=http%3A%2F%2Fwww.theverge.com%2F2017%2F3%2F27%2F15077864%2Felon-musk-neuralink-brain-computer-interface-ai-cyborgs)) is [neural lace](https://techcrunch.com/2017/02/13/elon-musk-reiterates-the-need-for-brain-computer-interfaces-in-the-age-of-ai/). Neural lace is more a sci-fi term, it could mean an extremely thin mesh that can be inserted from needle hole.

How feasible is the plan? Spectrum found 5 experts on the field to discuss the matter. If you check out the links, there are academics who are working on ideas similar to Musk, there are also entrepreneur who has counter opinions, especially the potential medical issues of using neural lace.

[Edit at 20170421, 3:00 p.m. Fixed a typo.]

[ieee.org](http://spectrum.ieee.org/the-human-os/biomedical/devices/5-neuroscience-experts-weigh-in-on-elon-musks-mysterious-neural-lace-company)

---

### [Facebook Brain Computer Interface : Brain-Typing and Skin-Hearing](https://techcrunch.com/2017/04/19/facebook-brain-interface/)

How real is Facebook's [Brain-Computer Interface](https://en.wikipedia.org/wiki/Brain%E2%80%93computer_interface) (BCI)? Here are several thoughts: 
- As we mentioned in the Neuralink piece. BCI is already being used in practice and has many genuine applications: brain stimulus of [Parkinson's patients](http://www.parkinson.org/understanding-parkinsons/treatment/surgery-treatment-options/Deep-Brain-Stimulation), reading minds from [patents with massive stroke](https://www.technologyreview.com/s/603512/reached-via-a-mind-reading-device-deeply-paralyzed-patients-say-they-want-to-live/).
- But what about ideas such as brain-typing or skin-reading? Those are more speculative technologies. For example, brain-typing is usually called ["imagined speech recognition"](https://en.wikipedia.org/wiki/Imagined_speech) in literature. Due to the highly noisy nature of [electroencephalogram](https://en.wikipedia.org/wiki/Electroencephalography) (EEG) signal, it is very tough to have a good working system. So many existing researches actually used [Electrocorticogram](https://en.wikipedia.org/wiki/Electrocorticography)(ECog), which is an invasive procedure. As we discussed in the Neuralink piece, invasive procedure would likely cause complications. In the case of Ecog, around 10% of chance that the procedure would results in [minor complications](https://www.ncbi.nlm.nih.gov/pubmed/26921853). We are also far from complete mind reading - for example most applications are confined to recognize limited vocabularies.
- Facebook's massive imaging software seems to be a way to resolve this issue. According to their [hiring page](https://www.facebook.com/careers/jobs/a0I1200000JXr3eEAD/), the new technique would base on "optical, RF, ultrasound, or other entirely non-invasive approaches". The issue perhaps is how to do such procedure real-time.
- Skin-reading on the other hand requires new interface such as acoustic actuators on your skin, that probably requires advanced signal processing techniques such as beam-forming.

So far, we can conclude that these efforts are more speculative and research in nature. I think both Facebook/Techcrunch seem to report as it is. Facebook stress that they are hiring neuroimaging engineers as well as start to a complete 2 year projects. So none of these details make me think Facebook is hyping it. 

You can contrast Facebook research to Neuralink from Musk, which is a lot more speculative, because it requires a non-invasive procedure to insert interface to the brain.

[techcrunch.com](https://techcrunch.com/2017/04/19/facebook-brain-interface/)

---

### [Apple's Official Permit of Testing Self-Driving Car](http://www.businessinsider.com/apple-officially-testing-self-driving-cars-california-dmv-confirms-2017-4?op=1)

It's an open secret that Apple is working on a self-driving car. After a well publicized cut-back [last October](http://www.businessinsider.com/apple-officially-testing-self-driving-cars-california-dmv-confirms-2017-4?op=1), Apple is in the game again. 

What should we expect from Apple SDC? 
- While Google is getting more limelight in its deep learning technology, Apple is unlikely to be too behind. With a recent move of [revamping its research effort](https://www.bloomberg.com/news/articles/2016-12-06/apple-to-start-publishing-ai-research-to-hasten-deep-learning), we expect Apple has similar man-power as Google in deep learning.
- Perhaps the issues is data. Google (Waymo) has invested a decade of research to collect road data. Remember several Apple's public PR disaster such as Map stemmed from insufficient amount of data.
- Perhaps what we expect most is the design. Would it follow Johnathan Ive's series of iProducts?

Interesting enough, we just learned this is also the week - Google is [hiring lobbyist](http://thehill.com/business-a-lobbying/328858-google-taps-new-lobbyist-for-self-driving-cars) to push SDC through the administration. Of course, we learn that Baidu just announced [project Apollo](http://www.marketwired.com/press-release/baidu-announces-project-apollo-opening-up-its-autonomous-driving-platform-nasdaq-bidu-2210437.htm), which is the umbrella project of all Baidu hardware and software solutions for SDC. With 30+ players in the field, we will see who win the crown of SDC.

[businessinsider.com](http://www.businessinsider.com/apple-officially-testing-self-driving-cars-california-dmv-confirms-2017-4?op=1)

---

### [Baidu's Project Apollo](http://www.marketwired.com/press-release/baidu-announces-project-apollo-opening-up-its-autonomous-driving-platform-nasdaq-bidu-2210437.htm)

Yet another company disclosed their plan on SDC. Codenamed Apollo, Baidu's effort seems extensive: it includes open sourcing hardware and software solutions. On the software stack, Baidu promised to open code and capabilities in obstacle perception, trajectory planning, vehicle control, vehicle operating systems. 

While Baidu received a permit from California last September, it's reasonable to believe that its core market is China. We believe it is more challenging. China leads the on-road car [accidents and causalities](http://www.worldatlas.com/articles/car-accidents-and-traffic-jams-in-china.html), mostly because it has a strained highway infrastructure. Would SDC be operable in such challenging road-condition? It's still left to find out. But for now, California might be a better test bed for Baidu.

[marketwired.com](http://www.marketwired.com/press-release/baidu-announces-project-apollo-opening-up-its-autonomous-driving-platform-nasdaq-bidu-2210437.htm)

## Blog Posts

### [Kaggle's CTO advice on studying ML. ](http://blog.kaggle.com/2017/04/17/the-best-sources-to-study-machine-learning-and-ai-with-ben-hamner-kaggle-cto/)

Kaggle's CTO, Ben Hamner, shares his view on how to study machine learning. His view echo with ours - you need a lot of practice in getting your ML skill sharpen in practice. 

I think in real-life, having good mathematical and theoretical foundation of machine learning is also important. On that realm, perhaps a reference book such as [PRML](https://www.amazon.com/Pattern-Recognition-Learning-Information-Statistics/dp/0387310738) would be helpful.

[kaggle.com](http://blog.kaggle.com/2017/04/17/the-best-sources-to-study-machine-learning-and-ai-with-ben-hamner-kaggle-cto/)

---

### [Reinforcement Learning vs Evolutionary Strategies](https://medium.com/@awjuliani/reinforcement-learning-or-evolutionary-strategies-nature-has-a-solution-both-8bc80db539b3)

Arthur Juliani was a developer of Unity3d and currently a researcher in deep learning and cognitive neuroscience. In this interesting article, he argues that reinforcement learning (RL) and evolution strategy (ES) could be methods which coexists with each other. His point of view is purely based on animal's inter/intra-life learning. Which the former is more close the evolution and the latter is close to reinforcement learning, or Juliani refers as the "gradient-based methods". 

I (Arthur Chan) spread this article around. One criticism I heard from member [Stuart Gray](https://www.facebook.com/StuartGray), he found that Juliani seems to mix up current day genetic algorithm/evolutionary method with biological evolution. As you know ES-type of method these days are mostly about optimization in the agent life-time. So perhaps it can also be seen as intra-life learning?

I think Stuart has a point. I got to agree though the article is interesting enough, because there might room for model which is first-trained by one strategy, and then retrained by others. Perhaps one potential thought is to first train a neural network, then evolve it using [neuroevolution type of method](https://en.wikipedia.org/wiki/Neuroevolution).

In any case, I found Juliani an interesting author to follow. So go ahead to check out his article.

[medium.com](https://medium.com/@awjuliani/reinforcement-learning-or-evolutionary-strategies-nature-has-a-solution-both-8bc80db539b3)

## Open Source

### [Caffe2.ai](http://caffe2.ai/blog/2017/04/18/caffe2-open-source-announcement.html)

During F8, Facebook [launched a new deep learning framework caffe2](https://venturebeat.com/2017/04/18/facebook-open-sources-caffe2-a-new-deep-learning-framework/), so what's the deal? 

From the documentation so far, caffe2 is more a refactored version of caffe1 with backward compatibility. My first impression of the toolkit is simialr to [Denny Britz's](https://twitter.com/dennybritz/status/854440840151744512): 

> I see reasons for using PyTorch over TF in certain research but I have a hard time seeing how to justify Caffe2 over TF for production.

which is quite true. I don't see a strong reason why one has to use Caffe2 instead of TF in server environment. But then Facebook positions the framework as more mobile-friendly. For example, in [its blog message](http://caffe2.ai/blog/2017/04/18/caffe2-open-source-announcement.html), Facebook indicated that she has been working with several big companies including Qualcomm and Intel to facilitate caffe2's mobile deployment.

As the package is still new, it's hard for us to speculate all details of the packages. Let's look for more developer reports in the near future, in particular we should watch out any speed/memory/model compression performance of caffe2.

[caffe2.ai](http://caffe2.ai/blog/2017/04/18/caffe2-open-source-announcement.html)

## Jobs

### [Computer Vision Engineer at Dishcraft Robotics](http://www.dishcraft.com/jobs/)

Bay Area-based startup Dishcraft looking for a machine learning engineer. Well-funded by tier-1 brand-name investors (led by First Round Capital) and are doing extremely well. For the right candidate, willing to relocate the person. Looking for basic traditional ML (SVM and boosting). Kaggle experience is a plus, Deep Learning for 2D images and 3D volumetric data (CNN focused), Tensorflow + Keras. Desirable computer vision skills: point cloud processing, signal and image processing, computational photography (familiarity with multi-view geometry and stereo vision, and color processing) 

[dishcraft.com](http://www.dishcraft.com/jobs/)

## [Have a Deep Learning related position you need to fill?](http://aidl.io/sponsorship/index.html)

## Video

### [F8: Keynote by Mark Zuckerberg and More](https://www.youtube.com/watch?v=YtUye84PuFY)

We talk a lot of F8 this week. There you have it, everything you love from Facebook is here. All the AI stuffs, plus more. Enjoy! 

[youtube.com](https://www.youtube.com/watch?v=YtUye84PuFY)

---

### [AIDL Office Hour Episode 7 With Sumit Gupta](https://www.youtube.com/watch?v=U9pyTMDspWg)

We had an awesome video "office hour" session with Sumit Gupta, VP of HPC, AI and Machine Learning at IBM. Sumit was very generous with his time and he shared what IBM is doing on the AI front with PowerAI, insights on where the bottlenecks on AI are today and how, as a beginner/intermediate practitioner, you should think about your career. 

Also, here are the links to what IBM is doing with PowerAI and the Galvanize-IBM hackathon in Bay Area: 
- [PowerAI overview](https://www.ibm.biz/powerai)
- [Galvanize-IBM Cognitive Builder Faire](http://www.galvanize.com/event/cognitive-builder-faire-san-francisco-4-21-4-23/) in SF this weekend

Thanks Sumit!

[youtube.com](https://www.youtube.com/watch?v=U9pyTMDspWg)
