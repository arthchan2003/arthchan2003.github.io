---
title: "AIDL Weekly Issue #72 - Google Dopamine"
date: 2019-07-25
---

# AIDL Weekly Issue #72 - Google Dopamine

Artificial Intelligence and Deep Learning Weekly - Issue 72

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 72 *September 3rd 2018* ](http://aidl.io/issues/72/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

We include links of several blogs post this week. That includes: 
- Google's new reinforcement learning framework - Dopamine,
- The very cool tutorial from Adrian Rosebrock on neural style transfer.

As always, if you find this newsletter useful, feel free to share it with your friends/colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 171,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [Neural Style Transfer Tutorial by Adrian Rosebrock. ](https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/)

We post yet another tutorial by Adrian this time. Why are Adrian's posts so appealing to us? Well, not only his tutorial covers the basic theory of a deep learning topic. He also include detail commentary on how his own code works. So you can always repeat what he did.

Now one more thing about his neural style transfer tutorial - it works real-time. As far as we know, you can probably optimize some existing tutorial code to achieve real-time information. But Adrian's is probably the one tutorial we know which already works at real-time.

Anyway, this sounds good to us. And please check it out.

[pyimagesearch.com](https://www.pyimagesearch.com/2018/08/27/neural-style-transfer-with-opencv/)

---

### [Dexterous Manipulation with Reinforcement Learning: Efficient, General, and Low-Cost](https://bair.berkeley.edu/blog/2018/08/31/dexterous-manip/)

Here is a post from Berkeley BAIR, on how one can use low-cost hardware and reinforcement learning to learn complex manipulation for robotic hands.

[berkeley.edu](https://bair.berkeley.edu/blog/2018/08/31/dexterous-manip/)

---

### [Cython for high and low](https://smerity.com/articles/2018/cython_for_high_and_low.html)

We found this half-a-year-old gem from Stephen Merity's blog. In the surface, it doesn't look like it has anything to do with AI/DL, but then deep learning just happens to be one application you always want to write in hybrid python/C to optimize performance.

So check out Merity's message, you will learn a lot on how it is done in practice.

[smerity.com](https://smerity.com/articles/2018/cython_for_high_and_low.html)

---

### [Google Dopamine](https://ai.googleblog.com/2018/08/introducing-new-framework-for-flexible.html?m=1)

RL, unlike deep learning, has fewer standard frameworks to initiate beginners. We have the openAI gym in the past, but the valuable site is now unmaintained. And there are a lot of small hacks you need to do to get some sample code working.

So Google's [Dopamine](https://github.com/google/dopamine) is going to change the landscape, it is an experimental framework which you can easily repeat certain method.

Currently, the framework's focus is mainly Atari 2600 games, and it already implements several state-of-the-art algorithms.

[googleblog.com](https://ai.googleblog.com/2018/08/introducing-new-framework-for-flexible.html?m=1)

---

### [Tutorial on Genetic Algorithm](https://medium.com/sigmoid/https-medium-com-rishabh-anand-on-the-origin-of-genetic-algorithms-fc927d2e11e0)

Here is a nice tutorial on genetic algorithm. In our time of deep learning, it's refreshing to see discussion on GA, which is actually quite competitive when compare to reinforcement learning. Kudo to the author Rishabh Anand!

[medium.com](https://medium.com/sigmoid/https-medium-com-rishabh-anand-on-the-origin-of-genetic-algorithms-fc927d2e11e0)

## Video

### [Crash Course of Deep Learning by Andrew Glassner](https://www.youtube.com/watch?v=r0Ogt-q956I)

Here is a course by [Andrew Glassner](https://en.wikipedia.org/wiki/Andrew_Glassner) on deep learning. The content for this course is interesting - other than the standard deep learning curriculum such as BackProp, convnet etc, Glassner also tried to bring insight on how deep learning can be used in computer graphics. He is more known to be an expert of the field so we are not too surprised.

[youtube.com](https://www.youtube.com/watch?v=r0Ogt-q956I)

## Member's Question

### [How does a CUDA program feels like?](https://devblogs.nvidia.com/easy-introduction-cuda-c-and-c/)

Q: As subject.

A: It really depends. In particular, in depends on how you structure your program. So here's an example based on C. But you can imagine similar thinking can work for Fortran as well.

Suppose you have a C-function which multiplies each element of an array by a scalar c, it is the type of function which can be easily parallelized. And doing it is easy, you just have to use a construct call CUDA kernel. I will leave it to look up some simple example on-line and try it out yourself. Generally, you can think CUDA is just a language extension of C. And they look quite similar.

So to your question, suppose you write the program in pure C, then the whole thing would just run on your CPU. But if you use the CUDA version, then the CUDA kernel would be executed on the GPU card. That in parallel programming, it's usually called heterogeneous programming. Because you are using two different devices (CPU and GPU) at the same time.

That's what we mean by "how you structure the program". It is up to the programmer to decide if a certain part of the program should be written in CUDA. If you want to get a better feeling, those are usually the part which you can expressed it as a simple for loop. We say usually, because some complex algorithms, such as FFT or graph algorithms, can be parallelized too. In fact, to decide whether certain program can be parallelized and can be scaled, is an important question in parallel programming in general.

If what we confuses you, we suggest you just go to copy few example and try to compile them with a machine which a GPU and CUDA are installed properly. Also check out the blog link we shared?

[nvidia.com](https://devblogs.nvidia.com/easy-introduction-cuda-c-and-c/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 171,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
