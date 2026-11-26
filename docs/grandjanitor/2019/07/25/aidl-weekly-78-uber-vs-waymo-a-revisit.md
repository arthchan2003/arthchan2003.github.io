---
title: "AIDL Weekly #78 - Uber vs Waymo: A Revisit"
date: 2019-07-25
---

# AIDL Weekly #78 - Uber vs Waymo: A Revisit

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 78 *October 22nd 2018* ](http://aidl.io/issues/78/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we revisit the Uber vs Waymo case, and share several resources, including the second edition of Sutton and Barto's book: "Reinforcement Learning: An Introduction". 

As always, if you find this newsletter useful, feel free to share it with your friends/colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 177,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### Deals

- [Paperspace $13M](https://techcrunch.com/2018/10/16/paperspace-scores-13m-investment-for-ai-fueled-application-development-platform/)
- [Twillio acquisition](https://venturebeat.com/2018/10/17/twilios-autopilot-lets-developers-deploy-bots-across-text-message-and-ai-assistants/)
- [Samsung acquired Zhilabs](https://venturebeat.com/2018/10/16/samsung-acquires-spanish-ai-powered-network-analytics-company-zhilabs-to-bolster-5g-ambitions/)

Artificial Intelligence and Deep Learning Weekly 

## Blog Posts

### [Did Uber Steal Google's Intellectual Property? - A New Yorker's Article](https://www.newyorker.com/magazine/2018/10/22/did-uber-steal-googles-intellectual-property?currentPage=all)

Back in February, Uber and Waymo has [settled outside the court for 0.34 percent of Uber's stake](https://www.theverge.com/2018/2/9/16995254/waymo-uber-lawsuit-trial-settlement). At the time, many (including us) see the settlement as a surprising win for Uber and its new CEO, Dara Khosrowshahi. 

Reading the New Yorkers' article penned by Charles Duhigg should make you rethink, and he told us a very different story. The whole piece is also very readable and you can just see it as a historical account of rise of SDC in Google, or ... , just the rise of SDC. We give you couple of highlights here: 
- Unlike most IP's lawsuits in the valley, the Uber vs Waymo case is actually a trade-secret suit, rather than about copyright suit. This is unusual because California's state has anti-non-compete law, trade-secret can easily leak from one company to another. (In some sense, by design.) So generally it's hard for companies to protect trade secrets.
- Knowing so should make you feel curious why Google sue Levandowski in the first place. As it turns out, it is more a recent trend in which big companies try to send a message to employees: leaving with trade secrets still has consequences.
- Remember the few tens of thousands files Levandowski download? It was seen as the most important evidence against Levandowski. As it turns out, such download happens automatically, so the evidence is less damning. That's why Google's case against Waymo is shakier than we thought. And it is the true reason why Google drop the case and go for settlement.
- Okay. What can we say about Levandowski then? Let us just quote this sentence from Duhigg?

> He is a brilliant mercenary, a visionary opportunist, a man seemingly without loyalty.

What do we think? In artificial intelligence, generally, the biggest asset for a big company is the dataset they create and possess. But what if you have an equally resourceful opponent who can gather the same amount of data as you do? Then human talents would become the most important factor in your success. For example, given the same amount of data, a strong and creative MLE would create superior models. And capable ML engine designers/programmers, just like powerful system programmers are still rare in AI/DL. In some sense, they are the ones who truly carry a product from development to research.

That explains the power of the type of Levandowski.... Perhaps that also why his abuse of power seems to be unpunished too - again we quote Duhigg: 

> Levandowski, for his part, has been out of work since he was fired by Uber. It’s hard to feel much sympathy for him, though. He’s still extremely wealthy. He left Google with files that nearly everyone agrees he should not have walked off with, even if there is widespread disagreement about how much they’re worth.

[newyorker.com](https://www.newyorker.com/magazine/2018/10/22/did-uber-steal-googles-intellectual-property?currentPage=all)

---

### [Terrence Sejnowski on Deep Learning](https://www.theverge.com/2018/10/16/17985168/deep-learning-revolution-terrence-sejnowski-artificial-intelligence-technology)

The Verge has an interview with Terrence Sejnowski on his view on deep learning. There are many interesting tidbits: e.g. his view on neuroscience and deep learning are related, and how Prof. Lecun designed ConvNet. 

[theverge.com](https://www.theverge.com/2018/10/16/17985168/deep-learning-revolution-terrence-sejnowski-artificial-intelligence-technology)

---

### [" ML is losing some of its luster for me. How do you like your ML career?"](https://www.reddit.com/r/MachineLearning/comments/9p9ccz/d_ml_is_losing_some_of_its_luster_for_me_how_do/)

This is a thread we saw in Reddit. And it says a lot of the status of current MLEs: In some sense, they are actually the core development team of their products. Yet they are often under-resourced, and indeed they are responsible to educate the whole company about the latest advance in A.I. 

We want to throw out a few points: 
- First, let's not single out management as the only problem of product development. They have their issues: working on sales, dealing with operations. Also generally management is not always an easy task. Your goal as an MLE is to help and educate everyone in your company to adopt a new technology. So do communicate and even over-communicate.
- Then, we should ask is whether "feeling of ML is losing its lusters" is new. Actually, not really, ML is always a mundane job filled with tedious tasks. Just like every occupation, MLE has their fair share of joy and sorrow: Your time of struggling with code to get a script running, your time of tending a week-long training, your time to optimize inference and training routines. None of these take are trivial, but once you have done it couple of times, it still feel like one big grind.
- So, may be a good way to give us solace is just to see ML or AI the way it is - nothing fancy, nothing futuristic. MLE is just a job which can pay you bill.

Or if you feel fancy: talking about AI in a dinner party is kind of cool. But that shouldn't be why you choose MLE as a career. :)

[reddit.com](https://www.reddit.com/r/MachineLearning/comments/9p9ccz/d_ml_is_losing_some_of_its_luster_for_me_how_do/)

## Video

### [MIT AGI Conversation with Prof. Yoshua Bengio](https://www.youtube.com/watch?v=azOmzumh0vQ&feature=youtu.be&fbclid=IwAR3j86BgUdQaDvmvPnBrPd9VPfwZidLArRQtN1yR-_YQ9_jol_-ejLS7Dd4)

Shared by Lex Friedman, Prof. Bengio talked about how to make an estimator be less biased to data. 

[youtube.com](https://www.youtube.com/watch?v=azOmzumh0vQ&feature=youtu.be&fbclid=IwAR3j86BgUdQaDvmvPnBrPd9VPfwZidLArRQtN1yR-_YQ9_jol_-ejLS7Dd4)

## Book Review

### [Sutton RL book 2nd edition ](https://drive.google.com/file/d/1opPSz5AZ_kVa1uWOdOiveNiBFiEOHjkG/view)

After many years of waiting, we finally see second edition of Prof. Richard Sutton and Prof. Andrew Barto's book, "Reinforcement Learning: An Introduction" released. You can find the book shared under Creative Common license, and we share one of the links. 

If you happen to own the first edition, you would notice that second edition has different notations, and many new and updated chapters. For example, there are new chapters on the neuroscience of reinforcement learning. Case studies in chapter 16 also include discussion of AlphaGo and AlphaGo Zero, both of which are very significant advances in computer science.

To us, this is much needed update of one bible in the field. So make sure you check it out.

[google.com](https://drive.google.com/file/d/1opPSz5AZ_kVa1uWOdOiveNiBFiEOHjkG/view)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 177,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65. 

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
