---
title: "On Kurzweil : a perspective of an ASR practitioner"
date: 2013-01-26
categories: ["ASR", "Kurzweil", "Speech Recognition"]
---

# On Kurzweil : a perspective of an ASR practitioner

Many people who don't work on the fields of AI, NLP and ASR have heard of Kurzweil. To my surprise, many seem to give little thought on what he said and just follow his theory wholeheartedly. 

In this post, I just want to comment on one single little thing, which is whether real-time speech-to-speech translation can be achieved in 2010s. This is a very specific prediction from Kurzweil's book "[The Singularity is Near](http://en.wikipedia.org/wiki/Predictions_made_by_Ray_Kurzweil#2010)".

My discussion would mainly focus on ASR first. So even though my examples below are not exactly pure ASR systems, I will skip the long winding wording of saying "ASR of System X". And to be frank, MT and Response system probably goes through similar torturous development process anyway. So, please, don't tell me that "System X is actually ASR + Y", that sort of besides the point.

Oh well, you probably ask why bother, don't we have a demo of real-time speech-to-speech translation from Microsoft already? 

True, but if you observe the[demo ](http://www.youtube.com/watch?v=Nu-nlQqFCKg)carefully, it is based on read speech. I don't want to speculate much but I doubt it is a generic language model which wasn't tuned to the lecture. In a nutshell, I disbelieve it is something you can use it in real-life.

Let's think of a more real-life example: Siri, are we really getting 100% correct response now? (Not to boil down to ASR WER ...... yet) I don't think so. Even with adaptation, I don't think Siri understand what I said every single time. For most of the time, I follow the [unofficial command list](http://www.mactalk.com.au/31/104774-list-siri-commands.html) of Siri, let it improve with adaptation..... but still, it is not perfect. 

Why? It is the hard cold reality: ASR is still not perfect, with all the advancement in HMM-based speech recognition. All the key technologies we know in the last 20 years: CMLLR, MMIE, MPE, fMPE, DMT, consensus network, multipass decodings, SAT, SAT with MMIE or all the nicest front-ends, all the engineerings. Nope, we are not yet having a feel-good accuracy. Indeed, human speech recognition is not 0% WER neither but for some reasons, the current state-of-the-art ASR performance is not reaching there.

And Siri, we all know is the state-of-the-art.

Just digress a little bit: Now most of the critics when they write to this point, will then lament that "oh, there is just some invisible barrier out there and human just couldn't make a Tower Babel, blabla....". I believe most of these "critics" have absolutely no ideas what they are talking about. To identify these air-head critics, just try to see if they put "cognitive science" into the articles, then you don't know they never work on real-life ASR system.

I, on the hand, do believe one day we can get there. Why? Because when people work on one of these speech recognition evaluation tasks, many would tell you : given a certain test set and with enough time and gumption, you would be able to create a system without any errors. So to me, it is more of an issue of whether some guys grinding on the problem, but not feasibility issue.

So where are we now in ASR? Recently, In ICASSP 2012, a [Google paper](http://dejanseo.com.au/research/google/37681.pdf), trained 87 thousand hour of data. That is probably the largest scale of training I know. Oh well, where are we now? 10%. Go down from 12%. So the last big experiment I know, it's probably the 3000 hours experiment back in 2006-7. The Google authors are probably using a tougher test set. So the initial recognition rate was yet again lower.

Okay, speculation time. So let's assume, that human can always collect 10 times more labelled data for every 6-7 years AND we can do an AM training on them. When will we go to have say 2% WER on the current Google test set? If we just think of very simple linear interpolation. It will take 4 \* 6 years = 24 years to collect 10000 times more data (or 8 billion hour of data). So we are way-way past the 2010s deadline from Kurzweil. 

And that's a wild speculation. Computation resources probably will work out itself by that time. What I doubt most is whether the progress would be linear. 

Of course, it might be non-linearly better too. But here is another point: it's not just about the training set, it's about the test set. If we truly want a recognizer to work for \*everyone\* in the planet, then the very right thing to do is test your recognizer on our whole population. If we can't then you want to sample enough human speech to represent the Earth's population, the current test set might not be representative enough. So it is possible that when we increase our test set, we found that the initial recognition rate has go down again. And it seems to me our test set is still in the state of mimicking human population. 

My discussion so far are mostly on acoustic model. On the language model side, the problem will mainly on domain specificity. Also bear in mind, human language can evolve. So, say we want to build a system which build a customized language model for each human being in the planet. At a particular moment of time, you might not be able to get enough data to build such a language model.

For me, the point of the whole discussion is that ASR is an engineering system, not some idealistic discussion topic. There will always be tradeoff. You may say: "What if a certain technology Y emerge in the next 50 years?" I heard that a lot Y could be quantum computing or brain simulation or brain-human interface or machine implementation of brain. Guys..... those, I got to admit are very smart idea in our time, and give it another 30-40 years, we might see something useful. For now, ASR really has nothing to do with them. I never heard of machine implementation of the audio cortex, or even an accurate construction of audio pathway. Nor, there is an easy progress of dissecting mammal inner ear and bring understanding on what's going on in human ear. From what I know, we seem to know some, but there are lots of other things we don't know.

That's why I think it's better to buckle down and just to try to work out our stuffs. Meaning, try to come up with more interesting mathematical model, try to come up with more computational efficient method. Those .... I think are meaningful discussion. As for Kurzweil, no doubt he is a very smart guy, but at least on ASR, I don't think he knows what he talks about. 

Of course, I am certainly not the only person who complains Kurzweil. Look at how [Douglas Hofstadter's](http://www.americanscientist.org/bookshelf/pub/douglas-r-hofstadter) criticism:

"It’s as if you took a lot of very good food and some dog excrement and blended it all up so that you can't possibly figure out what's good or bad. It's an intimate mixture of rubbish and good ideas, and it's very hard to disentangle the two, because these are smart people; they're not stupid."

Sounds like very reasonable to me.

Arthur
