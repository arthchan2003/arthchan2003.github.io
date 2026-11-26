---
title: "AIDL Weekly #20: Did DeepMind Fail to Comply Data Protection Law?"
date: 2019-06-18
---

# AIDL Weekly #20: Did DeepMind Fail to Comply Data Protection Law?

Artificial Intelligence and Deep Learning Weekly - Issue 20 [Issue 20 *July 7th 2017* ](http://aidl.io/issues/20/index.html#start)

## Editorial

### Patient Privacy and DeepMind - Thoughts from Your Humble Curators

It's summer! One of us is on vacation, so we have a shorter issue in terms of items (only 8). Yet, there are two long articles. The first is our investigation on the matter of whether DeepMind and Royal Free have violated patient privacy. We will examine both reports from the Independent Commissioner as well as DeepMind's Independent Review Panel.

The second is a closer look of the growth of Skills on Amazon Alexa. Why are they growing so quickly? Are they real? We will dig into Amazon's current and July's promotion strategy to understand it more.

Other than the two pieces on DeepMind and Amazon, we also cover 5 blog pages with topics ranged from Kaggle's Adversarial Attack Challenges to Spectrum's piece of "Brain as a Computer".

As always, if you like our newsletter, please subscribe and forward it to your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Screen Sharing on Steroids](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Collaborate fully](http://i.imgur.com/ds4FU08.gif) with your team. Works in your browser. No Download. No login. Get up and running in seconds. Integrated with Slack. Don't be like [them](https://www.youtube.com/watch?v=DYu_bGbZiiQ). Just [\#GetStuffDone](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [ICO to DeepMind : "Just That You Can, Doesn't Mean That You Should."](https://deepmind.com/blog/ico-royal-free/)

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

### [Closer Look at Amazon Skills Growth Number. ](https://techcrunch.com/2017/07/03/amazons-alexa-passes-15000-skills-up-from-10000-in-february/)

Amazon has grown its Skills from 10000 to 15000 in the past few short months.

What do the numbers mean? We will use this [Wired piece](https://www.wired.com/2017/02/amazon-alexa-hits-10000-skills-plenty-room-grow/) as the basis of our analysis. 
- First of all, skills were first reported around the end of 2015 with 135 skills, but at the end of 2016, the number grew to ~7000 skills. So we are talking about ~600 skills/month growth.
- Yet we also know that in January 2017, 3000 more skills appeared. That brought the skills number to 10000 in the Wired piece.
- Now there are 4 calendar months from February to June. So we know that the growth in last 4 months is ~1250 skills/month.

So the first conclusion you may draw is that "Wow! Skill's growth in the last 4 months is faster than the average growth last year!" That's very tempting. But then smart [AIDL members](https://www.facebook.com/groups/DeepNetGroup/) remind us that in June, Amazon was running a promotion to [give away 2500 Echoes for developers who publish a new Skill](https://github.com/alexa/skill-sample-nodejs-fact). So let's assume each developer publish 1 skill and we discount exactly 2500 skills from the Feb-Jun numbers, we are really talking about ~600 skills/month, which doesn't seem to be too different from the numbers from 2016.

Now one question you should also ask is did Amazon run any other promotions before June? Yes there was, from our discussion with members who are developers, Amazon gave out Echo Dot to hackathons if you publish several Skills. There are also incentives for top-performing [Skill developers](https://techcrunch.com/2017/05/16/amazon-begins-rewarding-top-performing-alexa-skill-developers-with-direct-payments/). But it's hard to imagine their effect is bigger than the 2500-Echo give away.

Btw, Amazon is giving out [5000 Echoes](https://developer.amazon.com/alexa-skills-kit/alexa-developer-skill-promotion) in July too. They also provide templates for developers to speed up the process. So perhaps, next month we will see the number of Skills swell to ...... 15000+5000=20000.

In terms of numbers, Amazon has seemingly huge advantage of number of Skills compare to Google's and Microsoft's. Such number is boosted by on-going marketing campaign. In our view, this is classical vanity metric marketing, like when iOS reported 1M apps in the App Store but it works as it gets coverage. Coverage begets legitimacy in the eyes of consumers.

Acknowledgement: We thank AIDL member Stuart Gray for mentioning Amazon's June promotion to us.

[techcrunch.com](https://techcrunch.com/2017/07/03/amazons-alexa-passes-15000-skills-up-from-10000-in-february/)

## Blog Posts

### [NIPS 2017: Non-targeted Adversarial Attack](https://www.kaggle.com/c/nips-2017-non-targeted-adversarial-attack)

Woohoo! Google Brain is organizing a new Kaggle challenge, called Non-targeted Adversarial Attack Challenges (NAAC) on adversarial images. Of the three tasks, two is about creating images which can attack an existing system. The other is about defend against adversarial attack. The task is part of the NIPS 2017 competition track and it will last for three months.

Why would Brain want to organize such a task? Perhaps the elephant in the room is that adversarial attack is a sore point of all known deep learning systems, and some of the adversarial images can be embarrassingly different from the recognized class. In the past, such images are usually generated by the researchers, but in the scale of Google, it's possible that they might be observing some of these images in the wild.

[kaggle.com](https://www.kaggle.com/c/nips-2017-non-targeted-adversarial-attack)

---

### [The Brain as a Computer](http://spectrum.ieee.org/computing/hardware/the-brain-as-computer-bad-at-math-good-at-everything-else)

Here's one interesting article describing various efforts of brain-inspired chip development by Prof. [Karlheinz Meier](https://www.kip.uni-heidelberg.de/user/meierk/?lang=en) who is also co-director of the [Human Brain Project (HBP)](https://www.humanbrainproject.eu/en/).

Let's back up a little bit, why would people want to simulate the brain then? For the most part, understanding the brain.

Our understanding of brain is still fairly primitive. That's why quite a portion of neuroscientists believe to further understand brain, a full simulation of brain is necessary. That's what [Human Brain Project (HBP)](https://www.humanbrainproject.eu/en/) supposed to do. But unlike other big science projects such as Human Genome Project, HBP is more controversial because the resource required is huge. As you can read from the article, it takes a [supercomputer to simulate 1.73 billion nerve cells connected by 10.4 trillion synapses couple of year ago](http://www.riken.jp/en/pr/press/2013/20130802_1/). This is only ~2% of all number of cells in the brain (the latest number is [86 billion](http://www.riken.jp/en/pr/press/2013/20130802_1/) and the model is crude. Is it worthwhile to dedicate such resource? That's a great question many people are pondering.

Regardless, perhaps one important benefit of learning about brain structure is that we might be able to emulate the brain structure with circuits. In this piece, Prof. Meier discussed three neuromorphic systems, SpiNNaker, TrueNorth and BrainScaleS. I think it is very educational for people who try to learn the "next big thing" in the ANN world.

[ieee.org](http://spectrum.ieee.org/computing/hardware/the-brain-as-computer-bad-at-math-good-at-everything-else)

---

### [The AI Imposter](https://www.linkedin.com/pulse/ai-impostor-h-r-tizhoosh?trk=v-feed&lipi=urn%3Ali%3Apage%3Ad_flagship3_feed%3BcZJtBIk1FIUlDgt85t2nfQ%3D%3D)

One of our active Forum members, [Keith Aumiller](https://www.facebook.com/keith.aumiller), once remarked that all our "Humble" posts, like "Humble Administrators" and the current "Humble Curators" (aka AIDL Weekly Editorial) are not that humble at all. That's true and not true. For the most part, while we have a lot of experience working on ML problems and starting new AI companies, we are nowhere on par with professors and researchers who had been pushing the envelope on ML/AI. So calling ourselves "Humble" always feel appropriate to us.

That brings us to this post: Prof. Tizhoosh's warning about AI Imposter is real. You might see a lot of posts from so-called "Deep Learning Consultants", or the "Influencers" lately. They might be bright in their own field, but their "success" in AI seems overnight. Their "deep understanding" comes from no where. You know when you press them on the detail, "How SMT BLEU scores improve with deep learning?" "How does GAN actually work? Do we really know?" "What is depth in Convnet?" "What do you when you can't use deep learning?" They are tongue-tied and try to switch topics. Or online, they would just come up with controversial posts/comments to hype up their like counts.

We only agree Prof Tizhoosh's post in principle only, and as AIDL members opine - if experts only confined PhD with 10 years of experience. The bar is just too high to cross. Of course, we also feel that the whole "Turing Imposter test" is weird.

But to AIDL Members: Beware of AI Imposters. In particular, when you brought up a technical subject in AI, make sure you do know it enough to opine. And for others' sake, **may you be humble too**. You want to help other people for sure. You want to build up your own reputation for sure. But if you don't know something, just say you don't know. The world will become a better place if we present ourselves truthfully.

[linkedin.com](https://www.linkedin.com/pulse/ai-impostor-h-r-tizhoosh?trk=v-feed&lipi=urn%3Ali%3Apage%3Ad_flagship3_feed%3BcZJtBIk1FIUlDgt85t2nfQ%3D%3D)

---

### [Why can't you guys comment your f\*king code?](https://www.reddit.com/r/MachineLearning/comments/6l2esd/d_why_cant_you_guys_comment_your_fucking_code/)

In this angry post from a redditer, source code of facebook's recent research ["Deal or no deal? Training AI bots to negotiate"](https://code.facebook.com/posts/1686672014972296/deal-or-no-deal-training-ai-bots-to-negotiate/end-to-end-negotiator) was harshly criticized. It results in a storm of ~500 comments discussion at Reddit.

Here is one insightful comment from pdehaan: 

> I've struggled with some of these issues myself (I'm a programmer first, with an interest in ML). Some general thoughts I've encountered: 
> - Academic papers are by their nature often the wrong place to look if you're trying to grok ideas. Space is at a premium in many publications, so authors are incentivized to write papers that are information dense.
> - A lot of researchers aren't "programmers first". By that I mean they often approach code as a one-off means to an end, not something they're sticking into a real system and responsible for maintaining indefinitely.
> - Related to the above, the audience they're used to communicating to often have similar experience. What's obvious to them (and thus not elaborated on) isn't always going to align with what's obvious to you.
>
> ...that's not to say things shouldn't be improved. Some of the ideas coming out are immensely useful, and improving usability is a valuable activity. This is an area where developers shine - code is what they deal with every day. If you spend time working through shitty uncommented code, improve it.
>
>
>
> Worst case you have better code to work from, but the feedback can also be useful for helping authors to write better code in the future. If they're publishing code, there's at least a decent chance they'll take feedback to heart. Most people don't want to put shitty code out there, but that's not necessarily their area of expertise.

Well said! In our experience, part of your job as a developer is to decode cryptic machine learning source code. Sadly, such skill is one your value proposition as a ML programmer. :)

[reddit.com](https://www.reddit.com/r/MachineLearning/comments/6l2esd/d_why_cant_you_guys_comment_your_fucking_code/)

---

### [DeepMind Edmonton Office](https://deepmind.com/blog/deepmind-office-canada-edmonton/)

Not only Prof. Richard Sutton is the new director, DeepMind also hires 6 researchers who published the [DeepStack paper](https://www.deepstack.ai/). It does sound fairly exciting, may be DeepMind can keep its on-going streak on beating various games in championship level.

[deepmind.com](https://deepmind.com/blog/deepmind-office-canada-edmonton/)
