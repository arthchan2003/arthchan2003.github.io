---
title: "Speech Recognition vs SETI"
date: 2012-12-27
categories: ["cmusphinx", "HTK", "Julius", "Speech Recognition", "voxforge"]
---

# Speech Recognition vs SETI

If you track news of CMUSphinx, you may notice that the Sourceforge guys start to distribute data through BitTorrent ([link](http://cmusphinx.sourceforge.net/2012/12/help-to-distribute-cmusphinx-data-through-bittorrent/)). 

That's a great move. One of the issues in ASR is the lack of machine power in training. To make a blunt example, it's possible to squeeze extra performance by searching for the best training parameters. Not to say a lot of modern training techniques take some time to run. 

I do recommend all of your help the effort. Again, me not involved at all, just feel that it is a great cause.

Of course, things in ASR are never easy so I want to give two subtle points about the whole distributed approach of training.

### Improvement over the years?

First question you may ask, now does that mean, ASR can be like project such as SETI, which would automatically improve over the years? Not yet, ASR still has its unique challenge.

The major part I would see is how we can incrementally increase phonetically-balanced transcribed audio. Note that it is not just audio, but transcribed audio. Meaning: someone needs to go to listen to the audio, spending 5-10 times real time to write down what the audio really say word-by-word. All these transcriptions need to clean up and in a certain format. 

This is what Voxforge tries to achieve and it's not a small undertaking. Of course, comparing to the speed of the industry development, the progress is still too slow. The last time I heard, Google was training their acoustic model with 38000 hours of data. A WSJ corpus is a toy task compared to it.

Now, thinking in this way, let's say if we want to build the best recognizer through open source, what is the bottleneck? I bet the answer doesn't lie on machine power, whether we have enough transcribed data would be the key. So that's something to ponder about.

(Added Dec 27, 2012, on the part of initial amount of data, Nickolay corrected me saying that amount of data from Sphinx is already in terms of 10000 hours. That includes "librivox recordings, transcribed podcasts, subtitled videos, real-life call recordings, voicemail messages". 

So it does sound like Sphinx has the amount of data which rivals commercial companies. I am very interested to see how we can train an acoustic model with that amount of data.)

### We build it, they will come?

ASR is always shrouded with misunderstanding. Many believe it is a solved problem, many believe it is a unsolvable problem. 99.99% of world population are uninformed about the problem. 

I bet a lot of people would be fascinated by SETI, which .... Woa .... allows you to communicated to unknown intelligent sentients in the universe. Rather than on ASR, which ..... Em ..... basically many regards as a source of satires/parodies these days. 

So here comes another problem, the public don't understand ASR enough to see it as an important problem. When you think about this more, this is a dangerous situation. Right now, couple of big companies control the resource of training cutting-edge speech recognizers. So let's say in the futre everyone needs to talk with a machine in a daily basis. These big companies would be so powerful that they can control our daily life. To be honest to you, this thought haunts me from time to time. 

I believe we should continue to spread information on how to properly use an ASR system. At the same time, continue to build application to show case ASR and let the public understand its inner-working. Unlike subatomic particle physics, HMM-based ASR is not that difficult to understand. On this part, I appreciate all the effort which are done by developers of CMUSphinx, HTK, Julius and all other open source speech recognition projects.

### 

### Conclusion

I love the recent move of Sphinx spreading acoustic data using BitTorrent, it is another step to work towards a self-improving speech recognition system. There are still things we need to ponder in the open source speech community. I mentioned a couple, feel free to bring up more in the comment section. 

Arthur

---

## Comments

**Nickolay Shmyrev** (2012-12-28):

Great, thanks a lot.

**三十三博** (2012-12-28):

Post modified. Thanks for the correction. In future, don't hesitate to point out any mistakes.

Thanks,
Arthur

**三十三博** (2012-12-28):

I see. Sounds like I am not up to date with my information then.

Let me modified my post then.

**Nickolay Shmyrev** (2012-12-28):

The lack of data is not an issue.
We (CMUSphinx) also have tens of thousands hours of transcribed speech data already collected. It's not about Voxforge for sure, which is very limited effort. I mean librivox recordings, trancribed podcasts, subtitled videos, real-life call recordings, voicemail messages. It's all available. The question is how to process them. The upcoming sphinx4 release will contain a proper alignment framework which is the first step in building long audio training. More to come. That's why we need a computing power.

