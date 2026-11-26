---
title: "AIDL Weekly Issue #5 - Special Issue on Self-Driving Cars"
date: 2019-05-23
---

# AIDL Weekly Issue #5 - Special Issue on Self-Driving Cars

## Editorial

Intel/Mobileye big deal, more Waymo/Uber drama, etc. - yet another big week for self-driving cars! It's not hyperbole to say that self-driving cars represent one of largest market-size application for A.I. The jockeying for positions had been happening for a while and won't abate anytime soon. Intel largely missed the boat on mobile and is determined not to miss it on A.I. and autonomous vehicles. There's a subsystem race going on in the h/w and s/w space to solve all the myriad problems. 

At the highest level, a successful architecture would need to at least understand: 
- **Where am I (car) and where am I going?** Need maps, GPS, odometry data.
- **What's around me based on my sensors?** Need car sensors - LIDAR, camera, ultrasound, audio, infrared, etc. Need low-level intelligence / classifiers on each of those signals to identify and make sense of road signs, humans, pets, random objects on the street
- **What's around me based on external telemetry data?** Need other car-related positioning and odometry data, weather data, traffic pattern data
- **How do I make sense of what's around me, what other objects are doing and whether I'm doing the right actions?** A brain that takes internal sensor data and external telemetry data, makes sense of them and outputs an action. This is an oversimplification and is inherently a really tough challenge. There are so many corner and non-corner cases to account for. No company wants to own the first self-driving car that kills a pedestrian. How does the algorithm weigh navigation decisions in an unavoidable accident scenario where you could hit one group of pedestrians or another?
- **How do I train car to be smarter over time?** Need phone home feature to a remote human operator if car can't decide what to do, generating training data
- Etc.

This isn't meant to be exhaustive, but as you can see, the moment we start thinking about all the things a human driver does in navigation and in response to other moving blobs on the street, it becomes incredibly hard to create a driving machine replica. We suspect there will be multiple waves of innovation here over time, along the dimensions of better sensors, more types of telemetry data, better cost curve, and better brain.

Artificial Intelligence and Deep Learning Weekly

## News

### [California's Green Light to Self-Driving Cars](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/california-gives-the-green-light-to-selfdriving-cars)

The California State is giving loosening regulations on self-driving cars. This makes vehicles with automated [level 4 or 5](http://www.techrepublic.com/article/autonomous-driving-levels-0-to-5-understanding-the-differences/) be more easily tested. Vehicles such as Uber's self-driving taxi would also be allowed to pick up customers, but not for a fee. California's move is bold as many other cities in the world, such as Singapore, Boston, Pittsburgh, competes to be the leading city of driverless car. Free pick-up has been implemented [in Pittsburgh back September last year](https://newsroom.uber.com/pittsburgh-self-driving-uber/). 

[ieee.org](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/california-gives-the-green-light-to-selfdriving-cars)

---

### [Intel buys Mobileye for $15B](https://www.technologyreview.com/s/603853/machine-learning-and-data-are-fueling-a-new-kind-of-car/)

Intel acquisition of Mobileye deserves some attention: the price is expensive. [Intel is paying 60 times of Mobileye's earning](http://www.reuters.com/article/us-intel-mobileye-idUSKBN16K0ZP). Many people believe that it is [overpriced](https://www.fool.com/investing/2017/03/13/intel-is-paying-an-awful-lot-for-mobileye.aspx). So the question is : is it worthwhile? 

From the A.I. perspective, it does make sense. Intel's rival Nvidia released [Jetson TX2](http://www.nvidia.com/object/embedded-systems-dev-kits-modules.html), and is positioning to get into autonomous vehicles via tier-1 auto suppliers like Bosch. Intel missed the mobile wave and they are determined not to miss this wave.

Mobileye's Autopilot was one of the most prominent systems used in many self-driving system, lauded as the [first deep-learning-based system for vehicle detection](http://wccftech.com/tesla-autopilot-story-in-depth-technology/4/). Mobileye is a major supplier for many self-driving companies, which used to include Tesla, but Tesla dropped the relationship [after a fatal accident](https://www.technologyreview.com/s/603853/machine-learning-and-data-are-fueling-a-new-kind-of-car/). Currently Mobileye is investing reinforcement learning to improve their system. They also have a simulated system to assist such learning.

If you compare Mobileye with Drive.ai (also featured in this issue), perhaps the deep learning technology is less sexy. Drive.ai uses an end-to-end training strategy which usually results in bigger gain. But then Mobileye has been around, its existing customer base is more massive.

It's reasonable to think that acquisition of Mobileye, similar to [Nervanna's](https://www.nervanasys.com/intel-nervana/), would assist Intel's progress of creating specialized hardware chip on deep learning, and more important, the development platform for adopters.

[technologyreview.com](https://www.technologyreview.com/s/603853/machine-learning-and-data-are-fueling-a-new-kind-of-car/)

---

### [Deep Learning and Drive.ai](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/how-driveai-is-mastering-autonomous-driving-with-deep-learning)

For a new company in the self-driving space, Drive.ai stands out among the crowd, and made headlines multiple times. For example, we saw [a video back in February](http://observer.com/2017/02/this-startups-new-self-driving-car-video-is-way-more-impressive-than-teslas/) that Drive can take care of a driving on rainy night, and very difficult driving condition such as malfunction red-light And we learn from several articles (such as [this one](https://techcrunch.com/2016/08/30/drive-ai-uses-deep-learning-to-teach-self-driving-cars-and-to-give-them-a-voice/) and the IEEE piece), that Drive attempts to train their network end-to-end. So we can imagine it is a sort of all-in-one architecture that include object-detection, and their approach would come up with both driving decision and if it is safe one or not. 

The IEEE piece tells one more interesting technical strength: which is how it can obtain data. It uses a small band of annotators, but most of them are used to train new scenarios. Whereas the deep-learning-based system is used to automate validate the data itself.

The test the author went through was based on automated level Level 2, which assumes human is on the driving seat. With California's state law loosen, we might see more Drive to showcase their close to Level-4 automated driving in the future.

[ieee.org](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/how-driveai-is-mastering-autonomous-driving-with-deep-learning)

---

### [Update on Waymo's Lawsuit](http://www.theverge.com/2017/3/10/14884666/alphabet-waymo-google-uber-lawsuit-testimony-block)

Woo. Waymo is ramping up its legal actions on Uber! This time it is filing for an injunction of the whole Uber's self-driving car operation (!). Enough said. As blogger [Daniel Compton](https://danielcompton.net/about) analyzed, it may be provable that Levandowski and Uber collaborated on the data theft before Levandowski even left Google 

[theverge.com](http://www.theverge.com/2017/3/10/14884666/alphabet-waymo-google-uber-lawsuit-testimony-block)

## Blog Posts

### [ICLR 2017 vs arxiv-sanity](https://medium.com/@karpathy/iclr-2017-vs-arxiv-sanity-d1488ac5c131#.vf91uwqo6)

Here is an interesting analysis by [Andrej Karpathy](http://cs.stanford.edu/people/karpathy/), on ICLR 2017 papers. What's the difference between peer review results and from arxiv-sanity? Spoiler alert: many papers loved by arxiv-sanity are rejected. So check out Karpathy's article and see why. 

[medium.com](https://medium.com/@karpathy/iclr-2017-vs-arxiv-sanity-d1488ac5c131#.vf91uwqo6)

---

### [An analysis of Uber's Worst Case Scenario](https://danielcompton.net/2017/03/14/uber-bombshell)

This is a piece written by Blogger Daniel Compton. In our view, perhaps it gives the best speculation on how the Waymo-Uber lawsuit would turn out. It ain't pretty. 

[danielcompton.net](https://danielcompton.net/2017/03/14/uber-bombshell)

---

### [Updates on "Learning Deep Learning - My Top Five List"](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)

At [AIDL](https://www.facebook.com/groups/DeepNetGroup/), we usually point any beginner resource question to Q4 which answers the question " How do you compare different resources on machine learning/deep learning?" and it links to one of my (Arthur's) blog post "Learning Deep Learning - My Top-Five List". 

Recently I gave the post a quarterly update, a summary: - Add a "Philosophy" section - Add a "Top-Five of Top-Five" section for people who don't know how to start. - Update my impression about Socher's class - as I finish the course half-way as well as looping through Hinton's class second time. No ranking changes. - Also add Oxford Deep Learning and several other classes in the Lectures/Courses section - Link Ian GoodFellow's "Deep Learning" with some of my quick impressions of the book - as I browse through the whole book once. (Also in this Issue.) - Add "Top-Five" for mailing list. You favorite mailing list "AIDL Weekly" is #1! :)

[thegrandjanitor.com](/grandjanitor/2016/08/15/learning-deep-learning-my-top-five-resource/)

---

### [Applying ML on March madness.](https://adeshpande3.github.io/adeshpande3.github.io/Applying-Machine-Learning-to-March-Madness)

One of our favorite writers, [Adit Despande](https://www.facebook.com/adit.deshpande.5?fref=pb_other) wrote an interesting piece on how to use machine learning to predict March Madness' result using data from last 25 years. 

[github.io](https://adeshpande3.github.io/adeshpande3.github.io/Applying-Machine-Learning-to-March-Madness)

## Open Source

### [YerevaNN Lab's "A Guide to Deep Learning"](http://yerevann.com/a-guide-to-deep-learning/)

We stumbled on this tremendous resources, a courtesy from YerevaNN Lab from Armenia. For beginners of deep learning, this guide is absolutely a treasure trove - it has a ranked resource list, separated by topics and gives very clear guidance what topic should be learned. It will give you a good sense on what topic in deep learning is a must-learn and how difficulty the topic is. 

[yerevann.com](http://yerevann.com/a-guide-to-deep-learning/)

---

### [tf-Seq2seq](https://github.com/google/seq2seq?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=revue)

[Denny Britz](https://github.com/dennybritz) released a general purpose seq2seq engine, tf-seq2seq. He mentioned that this engine, unlike [GNMT](https://research.googleblog.com/2016/09/a-neural-network-for-machine.html) is meant to be general purpose, so he doesn't guarantee tf-seq2seq would replicate Google's results. But the engine does look promising enough, it encompasses several functionalities including Machine Translation, Text Summarization, Conversational Modeling, Image Captioning. While these applications are based on the same theory, you usually need to do some plumbing to train well if you only have a translation engine. 

[github.com](https://github.com/google/seq2seq?utm_campaign=Revue%20newsletter&utm_medium=Newsletter&utm_source=revue)

## Video

### [AIDL Office Hour session with Han Shu, of Airbnb data science team](https://www.youtube.com/watch?v=Qqtc9_05yLc)

Han Shu, who leads a couple of data science teams at Airbnb, graciously took time out to talk with us about how Airbnb implements ML into the platform and how they think about it. They think as much as about org design as the code itself. 

Several interesting tidbits: 
- Both of us (Arthur and Waikit) were interested in Airbnb's design of scalable experimentation. Engineers can easily change their engine and quickly perform A/B tests. Results populate automately in their in-house built data platform
- Han gave an insider's view on how deep learning changed automatic speech recognition (ASR). He has been very experienced in ASR - PhD from [MIT SLS group](https://groups.csail.mit.edu/sls/research/) and one of the co-founders of [Vlingo](http://www.vlingo.com/) (later acquired by Nuance).

[youtube.com](https://www.youtube.com/watch?v=Qqtc9_05yLc)
