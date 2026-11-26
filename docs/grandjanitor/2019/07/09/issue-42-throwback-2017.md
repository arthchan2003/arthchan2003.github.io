---
title: "Issue 42 - Throwback 2017"
date: 2019-07-09
---

# Issue 42 - Throwback 2017

# [Issue 42 *December 30th 2017* ](http://aidl.io/issues/42/index.html#start)

## Editorial

### Thoughts From Your Humble Curators - 2017 Year End Edition

In this issue, we will re-publish several memorable stories during 2017. For news that includes Uber vs Waymo, Andrew Ng left Baidu and started deeplearning.ai. For papers, we include classic such as Sara Sabour and Prof. Hinton's work on capsule theory, as well as Prof. Bengio's consciousness prior. And finally for fact-checking, you guess it right: both "Facebook makes a kill switch of AI" and "Google AI build AO" are here. 

---

Hope you enjoy this throwback issue. As always, if you like our newsletter, feel free to subscribe/forward it your colleagues. AIDL accept donation. You can use the link at https://paypal.me/aidlio/12/ to donate. Your donation is use to cover monthly payment for our-ever growing subscription of AIDL Weekly as well as other operating cost.

Artificial Intelligence and Deep Learning Weekly

## News

### [Waymo Vs Uber](https://medium.com/waymo/a-note-on-our-lawsuit-against-otto-and-uber-86f4f98902a1)

From Issue 3: 

Waymo's Lawsuit against Uber is perhaps the biggest news last week. It was widely reported by popular outlets - The [Wired piece](https://www.wired.com/2017/02/googles-waymo-just-dropped-explosive-lawsuit-uber-stealing-self-driving-tech/) is perhaps the most well-written. The [formal complaint](https://drive.google.com/%E2%80%A6/0B7dzPLynxaXuQjY3dkllZ2ZKb0k/view) is readable and provided more interesting details. We chose the Waymo Medium piece here because it gives you a concrete technical complaints of why Waymo is unhappy. The short answer: "The KFC Bucket".

Why is this such a big deal? The KFC Bucket" you see on top of Google's self-driving car is the LiDAR system. This is the "360-degree eye" for the car - it a set of spinning lasers that maps the car's environment so it knows what's around. More importantly, it is a VERY critical component of any self-driving car. Waymo, born from Google's Self-Driving Project, has invested close to 10 years to refine said technology.

Let's step back a bit: *why is LiDAR so important to self-driving car?* Generally, self-driving car relies on LiDAR, radar and camera to collect information of its surrounding (Our opinion: audio signals ought to be part of it too). Out of the three, LiDAR is best at providing accurate 3-D representation of the surrounding of a car through laser emission/reflection and you can get information up to 100 meters of your surrounding. From an A.I.-standpoint, such 3-D representation allows better localization of the vehicle, scene understanding, and in turn allows the vehicle plan its movement correctly. In layman's terms, if you can't see well, you can't drive.

Whether LiDAR is crucial to self-driving has always been a question Part of the problem is the prohibitive cost of the device, back in 2013, [some quotes](https://www.technologyreview.com/s/520431/driverless-cars-are-further-away-than-you-think/) suggest it cost up to $80k to include LiDAR into a vehicle.

Then, *what is so special about Waymo's LiDAR system?* There are two parts of the answers. First of all, it is patented by Waymo in ["Devices and methods for a rotating LIDAR platform with a shared transmit/receive path"](https://www.google.com/patents/US8836922), filed back in 2014. Early this year, report suggest that Waymo was able to [cut cost of LiDAR by close to 90%](https://arstechnica.com/cars/2017/01/googles-waymo-invests-in-lidar-technology-cuts-costs-by-90-percent/). So what Uber allegedly has is not just an abstract design, but a highly cost-effective production-quality design, which presumably is what that 9GB, 14000 files is about.

Why is all this drama relevant to AIDL? Because autonomous vehicles is one of the most clear-cut and self-contained applications of A.I. that is impactful on many levels. It'll be driven by both innovation and offensive/defensive legal IP positions. For a $60-billion company like Uber, they can afford to litigate. For smaller companies though, as Bryan Walker Smith, a law professor at the University of South Carolina and an expert in self-driving regulations, said in the [IEEE piece](http://spectrum.ieee.org/cars-that-think/transportation/self-driving/what-waymo-wants-from-its-trade-secret-fight-with-uber/?utm_source=CarsThatThink&utm_medium=Newsletter&utm_campaign=CTT03012017), 

> “Companies will discover that trivial yet essential parts of automated driving have already been patented,” ...... “Google’s patent for driving on the left side of the lane when passing a truck comes to mind. These kind of patents could stop startups without a large defensive patent portfolio from even entering the field.”

The last question perhaps is *who is Anthony Levandowski?* And why was he mentioned so many times? [Levandowski](https://en.wikipedia.org/wiki/Anthony_Levandowski) is a rock star of self-driving car. He built a self-driving motorcycle back in 2004, worked with [Sebastian Thrun](https://en.wikipedia.org/wiki/Sebastian_Thrun) in 2007. He then formed two companies, one on mobile mapping using LiDAR, the other is a [self-driving Prius](https://www.cnet.com/news/robotic-prius-takes-itself-for-a-spin-around-sf/). Both were acquired by Google and he worked until early 2016.

From this little description, we know Levandowski is an important figure of Google's effort in self-driving. The Wired piece also painted him as a rule-breaker: 

> Levandowski has built a reputation for a cavalier approach to rules in general. In December, he insisted Uber’s autonomous cars didn’t need to apply for a special permit under California law and set them loose in San Francisco. The California DMV disagreed and revoked the vehicles’ registrations.

Judging from the complaints, Waymo has evidence on both Levandowski was searching and copying the files, and the fact that he is using the trade secret on Uber's design. Levandowski's departure also lead to many ex-employers left and join his startup Otto, which as you know [bought by Uber](https://techcrunch.com/2016/08/18/uber-acquires-otto-to-lead-ubers-self-driving-car-effort-report-says/) for $680 million price tag. No wonder Waymo filed such explosive lawsuit. Chris Swecker, a former assistant FBI director, would say "I would be very surprised if there wasn’t a full criminal investigation behind this."

[medium.com](https://medium.com/waymo/a-note-on-our-lawsuit-against-otto-and-uber-86f4f98902a1)

---

### [First Level 4 SDC in US](https://www.theverge.com/2017/11/7/16615290/waymo-self-driving-safety-driver-chandler-autonomous)

From Issue 37: 

This is huge. So this is the first Level 4 SDC on the road. Level 4 is commonly known as "mind off", which means human supervision is not necessary. Deploying a Level 4 on the road shows that Waymo is confident about their technology.

Phoenix was chosen because restrictions of SDC is nada at this point. But then cities around the States is frantically changing laws so that they can be the new hub of SDC. In this rate, we can expect SDC deployment would spread across united states soon.

[theverge.com](https://www.theverge.com/2017/11/7/16615290/waymo-self-driving-safety-driver-chandler-autonomous)

---

### [Andrew Ng Leaving Baidu](https://medium.com/@andrewng/opening-a-new-chapter-of-my-work-in-ai-c6a4d1595d7b#.x9b4oswqq)

From Issue 6: 

Perhaps the biggest news this week: Andrew Ng is leaving Baidu. As all of you know, Ng started Coursera, taught the perhaps most well-known MOOC, [Machine Learning](https://www.coursera.org/learn/machine-learning), found Google Brain, and later lead important researches in Baidu such as speech recognition. No one will doubt he is one of the giants in today's world of deep learning. So it comes to be a surprise for his departure and leave many speculations on his next move. He said in his Medium post, he would "explore new ways to support all of you in the global AI community". That makes you wonder, what can be bigger than Google or Baidu?

Our speculation is that Ng might join an initiative such as OpenAI which is a joint effort from multiple companies, or he starts a new research initiative, similar to his own Coursera, or Fei-Fei Li's Imagenet project, both create tremendous values to the community.

Regardless of his choice, we wish the good Professor well in his new journey. There are still many unsolved problems in machine learning. We are waiting for a world-class talent like Andrew to help solving them.

[medium.com](https://medium.com/@andrewng/opening-a-new-chapter-of-my-work-in-ai-c6a4d1595d7b#.x9b4oswqq)

---

### [Google's Hole Cards - TPU v2](https://www.nextplatform.com/2017/05/17/first-depth-look-googles-new-second-generation-tpu/)

From Issue 14: 

Imagine this, [Nvidia P100](http://www.nvidia.com/object/tesla-p100.html) is probably the best GPU you can buy last year, you bought one, but realize there is yet another device which is as fast as 32 P100 combined! So here is TPU v2, a monster device quietly developed last 2 years and it's only released after v1's specification is opened. We chose the article from The Next Platform, because it has the best writeup.

[nextplatform.com](https://www.nextplatform.com/2017/05/17/first-depth-look-googles-new-second-generation-tpu/)

---

### [Tesla hires Andrej Karpathy ](https://techcrunch.com/2017/06/20/tesla-hires-deep-learning-expert-andrej-karpathy-to-lead-autopilot-vision/)

From Issue 18: 

Tesla is hiring our beloved teacher of cs231n, Dr. Andrej Karpathy, away from Open.ai. Karpathy would become the Director of AI and Autopilot Vision at Tesla. And according to piece from TC, he will closely work with Jim Keller, who now overseeing both software and hardware division. How should we see the whole event? 
- If you really think about it, Dr. K only work in an industrial research setting for about a year. Yet he is now overseeing a major A.I. functionality of Tesla. Normally you would expect such position to be filled by a Professor-level personal. But for a freshly PhD? This event is simply extraordinary.
- The first thing to mention is perhaps Dr. K himself, a young scholar in the field of deep learning, his skill is known to be proficient in multiple subfields of deep learning - albeit computer vision, his unreasonably popular article on ["Unreasonable Effectiveness of RNN/LSTM"](http://karpathy.github.io/2015/05/21/rnn-effectiveness/), his foray into topics such as [reinforcement learning](http://karpathy.github.io/2016/05/31/rl/) and [generative models](https://blog.openai.com/generative-models/). Even his software such as [convnet.js](http://cs.stanford.edu/people/karpathy/convnetjs/) and [arxiv-sanity](http://www.arxiv-sanity.com/) are super well-received. Of course, he is also an early pioneer of [image captioning](http://cs.stanford.edu/people/karpathy/deepimagesent/). We know that this guy is a real deal, has the right stuffs and has it all in deep learning.
- But the whole event also shows certain desperation of Tesla : wouldn't a professor level of expertise make more sense? Would Dr. K has enough industrial experience to tackle the AI challenges of Self Driving Car?
- Despite his skill, we believe Dr. K is facing a tremendous challenge - there is certainly a huge technical problems of how to really get Tesla to go beyond Level 2 of autonomy. Tesla is also facing fierce competitions from Waymo and 10+ car vendors.
- But then, Tesla's gamble does make sense - Dr. K is not only a deep learning researcher, he is also a beloved teacher of many AI/DLers. His star power not only gain respect for Tesla, but will help to attract more talents in the future.

In any case, we congratulate Dr. K for joining Tesla. We only hope that he can still lecture on deep learning from time to time.

[techcrunch.com](https://techcrunch.com/2017/06/20/tesla-hires-deep-learning-expert-andrej-karpathy-to-lead-autopilot-vision/)

---

### [ICO to DeepMind : "Just That You Can, Doesn't Mean That You Should."](https://deepmind.com/blog/ico-royal-free/)

From Issue 20 

This week, UK's Independent Commissioner's Office (ICO) said that DeepMind and UK's National Health Service (NHS) "failed to comply the protection law".

Back in September 2015, DeepMind and The Royal Free London NHS Foundation Trust ("Royal Free") entered into an agreement where Royal Free transferred 1.6 Million records of patient data to DeepMind. In February 2016, such data enabled DeepMind to launch an application called [Stream](https://deepmind.com/applied/deepmind-health/working-nhs/how-were-helping-today/). One objective of Stream is that it can identify and treat [acute kidney injury (AKI)](https://www.thinkkidneys.nhs.uk/).

In April 2016, New Scientist get hold of the [agreement](https://drive.google.com/file/d/0BwQ4esYYFC04NFVTRW12TTFFRFE/view?usp=sharing) and [reported the event](https://www.newscientist.com/article/2086454-revealed-google-ai-has-access-to-huge-haul-of-nhs-patient-data/). They found that the data included sensitive patient information, such as if the patient HIV-positive or drug overdose.

As a consequence, not only ICO was formed to investigate if DeepMind violates any laws. Another watchdog group, [National Data Guard (NDG)](https://www.gov.uk/government/organisations/national-data-guardian) was also investigating the matter, and it concluded in May that DeepMind's handling of 1.6 Million record data has ["inappropriate legal basis"](https://www.theguardian.com/technology/2017/may/16/google-deepmind-16m-patient-record-deal-inappropriate-data-guardian-royal-free).

That brings us to ICO's decision this Monday. But that's not the end of the story! A turn of event happened two days later - an [independent review panel decides that DeepMind didn't breach the Data Protection Act](https://www.buzzfeed.com/tomchivers/googles-ai-company-didnt-break-the-law-over-nhs-data-report?utm_term=.wwEBBWAD8#.ro1DDno8V). They found "that DMH had acted only as a data processor on behalf of the Royal Free, which has remained the data controller." ([Source](https://deepmind.com/applied/deepmind-health/transparency-independent-reviewers/independent-reviewers/)) Yet ICO thinks DeepMind is less absolved.. (quoted from [ICO letter](https://ico.org.uk/media/action-weve-taken/undertakings/2014353/undertaking-cover-letter-revised-04072017-to-first-person.pdf)) 

> The processing of patient records by DeepMind significantly differs from what data subjects might reasonably have expected to happen to their data when presenting at the Royal Free for treatment.

For example, patients present due to accidents or receiving radiology, had no prior agreement with Royal Free to share their data. In the view of ICO, it violated UK [Data Protection Act](https://en.wikipedia.org/wiki/Data_Protection_Act_1998)'s Principle One: Personal data shall be processed fairly and lawfully. Similarly, the ICO found that there are 3 more principles from the Act were violated by DeepMind.

---

While [some experts commended](https://www.buzzfeed.com/tomchivers/googles-ai-company-didnt-break-the-law-over-nhs-data-report?utm_term=.wwEBBWAD8#.ro1DDno8V) the effort of DeepMind setting up an independent panel, the ICO's investigation gave an impression that the DeepMind-Royal Free deal was hastily done and were in violation.

Given the size of data and the prominence of the group, one would think the brilliant DeepMind decision makers would be more careful here e.g. Shouldn't they check if the patient has consent of their data being used? Shouldn't the patient be informed if their record is shared? It didn't seem to be the case.

Perhaps more frustrating is that many DeepMind's development on patient privacy seems to all happen after the fact. e.g. the [confidential patient record based on blockchain](https://deepmind.com/blog/trust-confidence-verifiable-data-audit/) happened only this year after the probing.

When it comes to applying machine learning on healthcare, the whole DeepMind-Royal Free incident reminds us that patient data is very different than other types of data. We share the view of the Information Commissioner, [Elizabeth Denham](https://iconewsblog.wordpress.com/category/Elizabeth-Denham/). Really, ["It’s not a choice between privacy or innovation"](https://iconewsblog.wordpress.com/2017/07/03/four-lessons-nhs-trusts-can-learn-from-the-royal-free-case/), if DeepMind didn't rush, they could have come up with a fool-proof solution.

As a final word and rephrasing Denham's another lesson - Just that you can do Deep Learning, **doesn't mean you should.**

Acknowledgement: We thank AIDL member Stuart Gray for bringing up the issue to the forum.

Reference: 
- [New Scientist's Original Article Back in April 2016](https://www.newscientist.com/article/2086454-revealed-google-ai-has-access-to-huge-haul-of-nhs-patient-data/)
- [UK Data Protection Principle](https://socialdialogue.gov.mt/en/Documents/Entities/data-protection-principles.pdf)
- [National Data Guard's take of the matter](https://www.theguardian.com/technology/2017/may/16/google-deepmind-16m-patient-record-deal-inappropriate-data-guardian-royal-free)
- [ICO decision](https://ico.org.uk/about-the-ico/news-and-events/news-and-blogs/2017/07/royal-free-google-deepmind-trial-failed-to-comply-with-data-protection-law/)
- [ICO letter](https://ico.org.uk/media/action-weve-taken/undertakings/2014353/undertaking-cover-letter-revised-04072017-to-first-person.pdf)
- [ICO undertaking](https://ico.org.uk/media/action-weve-taken/undertakings/2014352/royal-free-undertaking-03072017.pdf)
- [ICO Forth Lessons Learn](https://iconewsblog.wordpress.com/2017/07/03/four-lessons-nhs-trusts-can-learn-from-the-royal-free-case/)
- [DeepMind Response to ICO](https://deepmind.com/blog/ico-royal-free/)
- [DeepMind Independent Reviewers](https://deepmind.com/applied/deepmind-health/transparency-independent-reviewers/independent-reviewers/)
- [DeepMind Independent Reviewers' Annual Report](https://deepmind.com/documents/85/DeepMind%20Health%20Independent%20Review%20Annual%20Report%202017.pdf)
- [DeepMind's Verifiable Data Audit](https://deepmind.com/blog/trust-confidence-verifiable-data-audit/)

[deepmind.com](https://deepmind.com/blog/ico-royal-free/)

---

### [deeplearning.ai - A Closer Look At Prof. Andrew Ng's Deep Learning Course](https://www.deeplearning.ai/)

From Issue 24: 

By now, we all know that deeplearning.ai is a new series of courses, or specialization, developed by Prof. Andrew Ng. First off, we really appreciate Prof. Ng to create a new deep learning class right after he left the industry. One of us (Arthur) has quickly browsed through the curriculum of Course 1 to 3, here are some notes: 
- Only Course 1 to 3 are published now, they are short classes, more like 2-4 weeks. It feels like the [JHU Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science) and it feels good for beginners. Assume that Course 4 and 5 are long, say 4 weeks. So we are talking about 17 weeks of study.
- Unlike the standard Ng's ML class, python numpy is the default language. That's good in our view because close to 80-90% of practitioners are using python-based frameworks and knowledge of numpy is always very useful.
- Course 1-3 has around 3 weeks of curriculum overlapped with "Intro to Machine Learning" Lecture 2-3. But you should still check the course out even if you have some ML background. The course helps you to see other ML techniques from the eyes of a DL researcher. For example, Course 1 would guide you how to optimize a logistic regressor with back-prop like algorithm.
- Course 2 is about optimization, there we're introduced Tensorflow.
- Course 3 is more about how to setup a deep learning system pipeline. While it is only two weeks long, we find this Course the most exciting because we can hear what Prof. Ng thinks about DL after his years in industry.
- Course 4 and 5 are about CNN and RNN respectively, they are not yet published. From the outline so far, they are good preliminary classes before you take cs231n or cs224n.
- So our general impression here is that the specialization is more a comprehensive class, comparable with Hugo Larochelle's Lectures, as well as Hinton's NNML. Yet the latter two classes are known to be more difficult. Hinton's class in particular, are known to confuse even PhDs. So that shows one of the values of this new DL class: it is a great transition from "Intro to ML" to more difficult classes such as Hinton's.
- But how does it compared with other similar course such as Udacity's DL nanodegree then? We are not sure yet, but the price seems to be more reasonable if you go through the Coursera route. Assume we are talking about 5 months of study, you are paying $245. Compare to Udacity's price tag of $549. Ng's specialization looks like a bargain.
- Better than that: many of you Weekly readers are likely to take many other courses before considering Ng's class. In that case, you would find finishing the class faster than you thought. That also mean, you can spend *less than $245* on the class.
- We also found that many existing beginner classes advocate too much on running scripts, but avoid linking more fundamental concepts such as bias/variance with DL. Or go deep to describe models such as Convnet and RNN. cs231n did a good job on Convnet, and cs224n teach you RNN. But they seem to be more difficult than Ng or Udacity's class. So again, Ng's class sounds like a great transition class.
- Throughout the class, there are interviews with luminaries in DL community, including Prof. Hinton, Dr. Ian Goodfellow and Dr. Andrej Karpathy. Just listening to them may worth the $49 price tag.

Our current take: *We are going to take the class ourselves.* And we highly recommend this class to any aspiring students of deep learning.

[deeplearning.ai](https://www.deeplearning.ai/)

## Factchecking

### A Closer Look at The Claim "Facebook kills Agents which Create its Own Language"

From Issue 24: 

As we fact-checked in Issue [18](http://aidl.io/issues/18#start) and [23](http://aidl.io/issues/23#start), we rated the claim 

> Facebook kills Agents which Create Its Own Language.

as **false**. And as you might know, the faked news has spread to 30+ outlets which stir the community.

Since the Weekly has been tracking this issue much earlier than other outlets (Gizmodo is the first popular outlet call the faked news out), we believe it's a good idea to give you our take on the issue, especially given all information we know. You can think of this piece as more a fact-checking from a technical perspective. You can use as a supplement of the [Snope's piece](http://www.snopes.com/facebook-ai-developed-own-language/).

Let's separate the issue into few aspects:

1, *Does Facebook kills an A.I. agent at all?*

Of course, this is the most ridiculous part of the claim. For starter, most of these "agents" are really just Linux processes. So..... you can just stop them by using the Linux command *kill*. The worst case.... *kill -9* or *kill -9 -r*? (See Footnote [1])

2, *What Language does AI Agents Generated and The Source*

All outlets, seem to point to couple of sources, or the original articles. As far as we know, none of these sources had quoted academic work which is directly the subject matter. For convenience, let's call these source articles to be "The Source" (Also see Footnote [2]). The Source apparently has conducted original research and interview with Facebook researchers. Perhaps the more stunning part is there are printouts of how the machine dialogue look like. For example. Some of the machine dialogue looks like 

> Bob: "i can i i everything else"
>
>
>
> Alice: "balls have zero to me to me to me to me ....."

That does explain why many outlets sensationalized this piece, because while the dialogue is still English (as we explained in Issue #18), it does look like codeword, rather than English.

Where does the printout comes from? It's not difficult to guess - it comes from the open source code of ["End-to-End Negotiator"](https://github.com/facebookresearch/end-to-end-negotiator) But then the example from github we can find there looks much more benign: 

> Human : hi i want the hats and the balls
>
>
>
> Alice : i will take the balls and book &lt;eos&gt;
>
>
>
> Human : no i need the balls
>
>
>
> Alice : i will take the balls and book &lt;eos&gt;

So one plausible explanation here is that someone has played with the open source code, and they happened to create a scary looking dialogue. Th question, of course, are these dialogue generated by FB researchers? or does FB researchers just provide The Source the dialogue? Here is the part we are not sure. Because the Source does quote words from Facebook's researcher (see Footnote [3]), so it's possible.

3, *What is Facebook's take?*

Since the event, Prof. Dhruv Batras has post a [status at July 31](https://www.facebook.com/dhruv.batra.dbatra/posts/1943791229195215) in which he simply ask everyone to read the piece ["Deal or No Deal"](https://code.facebook.com/posts/1686672014972296/deal-or-no-deal-training-ai-bots-to-negotiate/) as the official reference of the research. He also called the faked news "clickbaity and irresponsible". Prof. Yann Lecun also came out and [slam at the faked newsmaker](https://www.facebook.com/yann.lecun/posts/10154653925097143).

Both of them decline to comment on individual pieces, including The Source. We also tried to contact both Prof. Dhruv Batra and Dr. Mike Lewis on the validity of the Source. Unfortunately, they are both unavailable for comments.

4, *Our Take*

Since it's an unknown for us whether any of The Source is real, we can only speculate what happened here. What we can do is make as technically plausible as possible.

The key question here: is it possible that FB researchers have really created some codeword-like dialogue and passed it off to the source? It's certainly possible but *unlikely*. Popular outlets have general bad reputation of misinforming the public on A.I., it is hard to imagine that P.R. department of FB don't stop this kind of potential bad press in the first place.

Rather, it's more likely that FB researchers only publish paper, but somebody else is misusing the code the researchers open sourced (as we mentioned in Pt. 2). In fact, if you reexamine the dialogue released by The Source: 

> Bob: "i can i i everything else"
>
>
>
> Alice: "balls have zero to me to me to me to me ....."

It looks like the dialogue was generated by models which are not *well-trained*, this is true especially if you compare the print out with the one published by Facebook's github.

If our hypothesis is true, we side with FB researchers, and believe that someone just write a over-sensational post in the first place causing a stirs of the public. Generally, everyone who spreads the news should take responsibility to check the sources and ensure integrity of their piece. We certainly don't see such responsible behavior in the 30+ outlets who report the faked news. It also doesn't look likely that The Source is written in a way which is faithful of the original FB research. Kudos to Gizmodo and Snope's authors who did the right thing. [4]

Given the agent is more likely to behave like what we found on Facebook's github, we maintain our verdict as in Issue 18 and 23, it is still very unlikely that FB agents are creating any new language. But we add qualifier "very unlikely" because as you can see in Point 3, we still couldn't get Facebook researchers' verification as of this writing.

So let us reiterate our verdict: We rate the "Facebook killing agents" *false*. We rate "Agents that create its own language" *very likely false*.

AIDL Editorial Team

Footnote:

[1] So, immediately after the event, couple of members was [joking](https://www.facebook.com/groups/DeepNetGroup/permalink/480006772392210/) about the public was being ignorant about what so-called AI agents are.

[2] We avoiding naming what The Source is. There seems to be multiple of them and we are not sure which one is the true origin.

[3] The author of The Source seems to have communication with Facebook researcher [Prof. Dhruv Batra](https://www.cc.gatech.edu/~dbatra/index.html) and quote the Professor's word, e.g. 

> There was no reward to sticking to English language,

as well as talking with researcher Mike Lewis, 

> Agents will drift off understandable language and invent codewords for themselves,

[4] *What if we are wrong? Suppose the Source is real, and the Agents does Generated Codeword-Like Dialogue, Are they new Language?*

That's more a debatable issue. Again, just like we said in Issue 18, suppose you start from training a model like from an English database, the language you got will still be English. But can you characterize a English-like language as a new language? That's a harder question. e.g. a creole is usually seen as another language, but a pidgin is usually seen as just a grammatical simplification of a language. So how should we see the codeword generated by purported "rogue" agent? Only professional linguist should judge.

It is worthwhile to bring up one thing: while you can see the codeword language just like any machine protocol such as TCP/IP, the Source implies that Facebook researcher have consciously making sure the language adhere to English. Again, this involves if the Source is real, and whether the author has mixed in his/her own researches into the article.

Artificial Intelligence and Deep Learning Weekly

---

### On Google's "AI Built an AI That Outperforms Any Made by Humans"

For those who are new at AIDL. AIDL has what we called "The Three Pillars of Posting". i.e. We require members to post articles which are relevant, non-commercial and non-sensational. When a piece of news with sensationalism start to spread, admin of AIDL (in this case, Arthur) would fact-check the relevant literature and source material and decide if certain pieces should be rejected. And this time we are going to fact-check a popular yet misleading piece "AI Built an AI That Outperforms Any Made by Humans". 
- The first thing to notice: "AI Built an AI That Outperforms Any Made by Humans" by a site which historically sensationalized news. The same site was involved in sensationalizing the early version of AutoML, as well as the notorious "AI learn language" fake news wave.
- So what is it this time? Well, it all starts from Google's [AutoML published in May 2017](https://research.googleblog.com/2017/05/using-machine-learning-to-explore.html) If you look at the page carefully, you will notice that it is basically just a tuning technique using reinforcement learning. At the time, The research only worked at CIFAR-10 and PennTree Banks.
- But then Google's AutoML released another version in November. The gist is that Google beat SOTA results in Coco and Imagenet. Of course, if you are a researcher, you will simply interpret it as "Oh, now automatic tuning now became a thing, it could be a staple of the latest evaluation!" The model is now distributed as [NASnet](https://arxiv.org/abs/1707.07012).
- Unfortunately, this is not how the popular outlets interpret. e.g. Sites were claiming "AI Built an AI That Outperforms Any Made by Humans". Even more outrageous is some sites are claiming "AI is creating its own 'AI child'". Both claims are false. Why?
- As we just said, Google's program is an RL-based program which propose the child architecture, isn't this parent program still built by humans? So the first statement is refutable. It is just that someone wrote a tuning program, more sophisticated it is, but still a tuning program.
- And, if you are imagining "Oh AI is building itself!!" and have this imagery that AI is now self-replicating, you cannot be more wrong. Again, remember that the child architecture is used for other tasks such as image classification. These "children" doesn't create yet another group of descendants.
- A much less confusing way to put it is that "Google RL-based AI now able to tune results better than humans in some tasks." Don't get us wrong, this is still an exciting result, but it doesn't give any sense of "machine is procreating itself".

We hope this article clears up the matter. We rate the claim "AI Built an AI That Outperforms Any Made by Humans" **false**. 

Here is the original [Google's post](https://research.googleblog.com/2017/11/automl-for-large-scale-image.html).

Artificial Intelligence and Deep Learning Weekly

## Member's Question

### [What is the Difference Between Deep Learning and Machine Learning?](/grandjanitor/2017/07/09/what-is-the-difference-between-deep-and-machine-learning/)

From Issue 21: 

This is written by one of us (Arthur). When a new member asked about the difference between DL and ML, we were surprised by many well-intentioned yet misleading answers. For example, many claim the fact DL uses a lot of data is the key differentiator from ML, and such answer is fairly misleading. Both ML and DL can use a lot of data, it's just DL is *more effective in utilizing more data*. Unfortunately, there are too many articles floating around took up this misleading claim.

Since what is "deep" is a fairly fundamental concept in deep learning, this article is likely to help you. Enjoy!

[thegrandjanitor.com](/grandjanitor/2017/07/09/what-is-the-difference-between-deep-and-machine-learning/)

## Paper/Thesis Review

### [Reading Prof. Yoshua Bengio's "The Consciousness Prior"](https://arxiv.org/abs/1709.08568)

Prof. Yoshua Bengio released an intriguing note last week on an idea called "The Consciousness Prior". The framework is interesting and I would point out several interesting aspects of it. 
- The consciousness mentioned in the paper is much less of what would think as [qualia](https://en.wikipedia.org/wiki/Qualia) but more about access of the different representations.
- The terminology is not too difficult to understand, suppose there is a representation of the brain at a current time h_t, *a representation RNN* F is used to model such representation.
- Whereas the protagonist here is the *consciousness RNN*, C, which is to used to model a consciousness state. What is \*consciousness state& then? It is actually a low-dimension vector of the representation h_t.
- Now one thing to notice is that Bengio believe that *consciousness RNN, C* should by itself include some kind of attention mechanism. What that means is that attention being used in NNMT these days should be involved. In a nutshell, C should "pay attention" to only important details within this consciousness vector when it updates itself.
- I think so far the idea is already fairly interesting, in fact, just the idea one interesting thought : what if we just initialize the consciousness vector to be random instead, in that case, there will be a new representation of brain appears. As a result. this mechanism mimic human brains on exploring different scenario we conjured with imagination.
- Bengio's thought also encompass a training method which he called verifier network, V. The goal of the network to match the current representation h_t with previous consciousness state c\_{t-k} (states?). The training as he envisioned can be a Variational autoencoder (VAE) or GAN.
- So far the idea doesn't quite echo with human's way of thinking. Human seems to create high-level concepts, like symbols to simplify our thinking. So Bengio addresses these difficulty by suggesting we can just use another network to generate what we mean from the consciousness state, he called it U. Perhaps we can call it *generation network*. This network can well-be implemented by memory-augmented networks style of architecture which distinguish key/value pairs. In this case, we can map the consciousness to more concrete symbols which symbolic logic or knowledge representation framework can use. ... Or we humans can also understand this consciousness representation.
- This all sounds good, but as you may hear from many readers of the paper. There is no experimental results. So this is really a theoretical paper.
- To be fair though, the good professor has outlined how each of the above 4 networks can be actually implemented. He also mentioned how such idea can be experimented in practice. E.g. he believe one good arena is reinforcement learning tasks.

All-in-all, this is an interesting paper, it's a pity that the detail is scanty at this point. But it's still quite worthwhile for your time to read. 

[arxiv.org](https://arxiv.org/abs/1709.08568)

---

### [Swish: a Self-Gated Activation Function](https://arxiv.org/abs/1710.05941)

Perhaps the most interesting paper last week is the Swish function. Here are some notes: 
- Swish is extraordinarily simple. It's just swish(x) = x \* sigmoid(x).
- Derivative? swish'(x) = swish(x) + sigmoid(x) (1 - swish (x)) Simple calculus.
- Can you tune it? Yes, there is a tunable version which the parameter is trainable. It's call Swish-Beta which is x \* sigmoid( Beta \* x)
- So here's an interesting part of why it is a "self-gating function". So.... if you understand LSTM, essentially it introduced a multiplication sign. e.g. input gate and forget gate, give you are weight of "how much you want to consider the input" and "how much much you want to forget". (http://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- So swish is not too different - there is the activation function but it is weighted by the input itself. Thus the term self-gating. In a nutshell, in plain English, "because we multiply".
- It's all good, but does it work? The experimental results look promising. It works on Cifar-10, Cifar-100. On Imagenet, it beats Inception-v2 and v3 when swish replace ReLU.
- It's worthwhile to point out the latest Inception is in v4. So the imagenet number is not beating stoa even within Google, not to say the best number in Imagenet 2016. But that shouldn't matter, if something consistently improve on some models of Imagenet, it is a very good sign it is working.
- Of course, looking at the activation function. It introduces a multiplication. So it does increase computation when compare with a simple ReLU. And that seems to be the complaint I heard. That's what I have. Enjoy!

[arxiv.org](https://arxiv.org/abs/1710.05941) 

---

### [Capsules](https://arxiv.org/abs/1710.09829v1)

From Issue 36: 

This is the Hinton's new invention of capsules algorithm. Here is a write up: It's TL;DR but we doubt we completely grok the idea anyway. 
- The first mention of "capsule" is perhaps in the paper ["Transforming Auto-encoders"](http://www.cs.toronto.edu/~fritz/absps/transauto6.pdf) which Hinton and students coauthored.
- It's important to understand what capsules try to solve before you delve into the details. If you look at Hinton's papers and talks, capsule is really an idea which improve upon Convnet. Hinton has two major complaints.
- First, the general settings of Convnet assumes that one filter is being used across different locations. This is also known as "location invariance". In this setting, the exact location of a feature doesn't matter. That has a lot to do with robust feature parameter estimation. It also drastically simplify backprop with weight sharing.
- But then location invariance also removes one important information of an image: the apparent location.
- Second assumption is max pooling. As you know, pooling usually removes a high percentage of information from the previous layer. In early architectures, usually pooling is the key to shrink the size of a representation down. Of course, later architectures had changed. But pooling is still an important component.
- So the design of capsule has a lot of do to tackle problems of max pooling: Instead of losing information, can we "route" pixel values from previous layer correctly so that they are in optimal use?
- Generally "capsule" represents a certain entity of an image, "such as pose (position, size, orientation), deformation, velocity, albedo, hue, texture etc". Notice that they are not hard-wired and automatically discovered.
- Then there is how the low level information can "route" to higher level. The mechanism is intriguing in this current implementation:
- First, your goal is to calculate a softmax in the form of exp(b*{ij} / Sum_k exp(b*{ik} where b\_{ij} is the output of lower level capsule i to a higher level capsule j. This is something you can train.
- Then what you do is iteratively estimate b\_{ij}. This appears in Procedure 1. The 4 steps are: a, calculate the softmax weight b. b, compute the prediction vector from a capsule i, then form a weighted sum, c, squash the weighted sum d, update softmax weight b based on the squash value and weighted sum.
- So why the squash function, our guess is it is to normalize the value computed in b. According to Hinton, a good function is v_j = |s_j|^2 / (1 + |s_j|^2) \* s_j / |s_j|
- The rest of the architecture actually looks very much like a Convnet. The first layer was a Convnet with ReLU activation.
- Would this work? The authors say yes. Not only it reaches the state of art benchmark of MNIST. It can also tackle more difficult tasks such as CIFAR-10, SVNH. In fact, the authors found that in both task they already achieve better results when first Convnet was first used to tackle these tasks.
- It also works well for two tasks called affMNISt and multiMNIST. First is MNIST go through affine transform, second is MNIST regenerated with many overlappings. This is quite impressive, because you will need to use much data augmentation and effort of object detection to get these cases working.
- The part, we have some doubts - is this model more complex than convnet? It's possible that we are just fitting a more complex model to get better results.
- Nice thing about the implementation: it's in Tensorflow, so we can play with it in the near future. Have fun!

[arxiv.org](https://arxiv.org/abs/1710.09829v1)
