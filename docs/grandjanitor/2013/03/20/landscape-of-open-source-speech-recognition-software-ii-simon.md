---
title: "Landscape of Open Source Speech Recognition Software (II : Simon)"
date: 2013-03-20
categories: ["open source speech recognition", "simon"]
---

# Landscape of Open Source Speech Recognition Software (II : Simon)

Around December last year, I wrote an [article](http://grandjanitor.blogspot.com/2012/12/landscape-of-open-source-speech.html) on open source speech recognizers. I covered HTK, Kaldi and Julius. One thing you should know, just like CMUSphinx, all of these packages contain their own versions of Viterbi algorithms' implementation. So when you asked someone who is in the field of speech recognition, they will usually say open source speech recognizers are Sphinx, HTK, Kaldi and Julius. 

That's how I usually view speech recognition too. After years working in the industry though, I start to realize this definition of seeing speech recognizer = Viterbi algorithm could be constraining. In fact, from the user's point of view, a good speech application system should be a combination of

a recognizer + good models + good GUI.

I like to call the former type of "speech recognizer" as "**speech recognition engines"** but the latter type as "**speech recognition applications**". Both types of "speech recognizers" are worthwhile applications. From the users' point of view, it might just be a technicality to differentiate them. 

When I am recovering as a speech recognition programmer (another name throwing :) ), one thing I notice is that there is much effort on writing "**speech recognition applications**". It is a good trend because most people from academia really didn't spend too much time to write good speech applications. And in open source, we badly need good applications such as dictation machine, IVR and C&C. 

One effort which really impressed me is [Simon](http://simon-listens.blogspot.com/). It is weird because most of the time I only care about engine-level type of software. But in the case of Simon, you can see couple of its features are really solving problems in real life and integrated to the bigger them of open source speech recognition.

- In 0.4.0, Simon starts to integrate with Sphinx. So if someone wants to develop it commercially, they can.
- The Simon's team also intentionally make context switching in the application, that's good work as well. In general, if you always use a huge dictionary, you are just over-recognizing words in a certain context.
- Last and not least, I like the fact it integrates itself to Voxforge. Voxforge is the open source answer to a large speech database of commercial speech company. So integration with Voxforge will ensure an increasing amount of data for your application.

So kudo to the Simon team! I believe this is the right kind of thinking to start a good speech application. 

Arthur

---

## Comments

**三十三博** (2013-03-30):

This comment has been removed by the author.

**Peter Grasch** (2013-07-06):

Hi Arthur,

Simon developer here. Thanks for the kind words!

Simon now has a new homepage at http://simon.kde.org
It's also just called "Simon" ("Simon listens" was the NPO originally created to support development).
Please update the link in the side bar.

Thanks!

Best regards,
Peter

**Arthur Chan** (2013-07-06):

Hey Peter,

Thanks for the note! I have updated the link. Come back from time to time!

Arthur

