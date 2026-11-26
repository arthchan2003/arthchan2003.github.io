---
title: "AIDL Weekly Issue 71 - Humans vs OpenAI Five"
date: 2019-07-25
---

# AIDL Weekly Issue 71 - Humans vs OpenAI Five

Artificial Intelligence and Deep Learning Weekly - Issue 71

The definitive weekly newsletter on A.I. and Deep Learning, published by [Waikit Lau](http://bit.ly/2lhpKGC) and [Arthur Chan](http://bit.ly/2mx0aiV). Our background spans MIT, CMU, Bessemer Venture Partners, Nuance, BBN, etc. Every week, we curate and analyze the most relevant and impactful developments in A.I.

We also run Facebook's [most active A.I. group](http://bit.ly/2lPc6MX) with 191,000+ members and host a weekly ["office hour" on YouTube](https://goo.gl/kPTYc9).

# [Issue 71 *August 27th 2018* ](http://aidl.io/issues/71/index.html#start)

## Editorial

### Thoughts From Your Humble Curators

This week we bring you the story of the first match between Open AI vs Humans in a 5v5 battle. Unlike 1v1, 5v5 gameplays feature collaboration between human experts, and currently it is unknown if computer agents can learn these complex interaction and strategy by itself.

As always, if you like our newsletter, feel free to share it with your friends/colleagues.

---

This newsletter is published by Waikit Lau and Arthur Chan. We also run Facebook's most active A.I. group with 169,000+ members and host an occasional "office hour" on YouTube. To help defray our publishing costs, you may donate via link. Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

Join our community for real-time discussions here - [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly

## News

### [RTX 2080 Pricing ](https://www.theverge.com/2018/8/20/17758724/nvidia-geforce-rtx-2080-specs-pricing-release-date-features)

As Nvidia released new architecture [Turing](https://www.nvidia.com/en-us/design-visualization/technologies/turing-architecture/), we also starts to see new card comes up. For further analysis we point your to the article by Tim Dettmer which we also share this Issue.

[theverge.com](https://www.theverge.com/2018/8/20/17758724/nvidia-geforce-rtx-2080-specs-pricing-release-date-features)

---

### Deals

- [Camera $20 Million](https://venturebeat.com/2018/08/23/carmera-raises-20-million-to-map-cities-for-self-driving-cars/)
- [Getaround $300 Million](https://www.bloomberg.com/news/articles/2018-08-21/softbank-invests-in-another-ride-sharing-startup-getaround)

Artificial Intelligence and Deep Learning Weekly

## Blog Posts

### [Which GPU(s) to Get for Deep Learning - by Tim Dettmers](http://timdettmers.com/2018/08/21/which-gpu-for-deep-learning/)

Tim Dettmer's article on choice of GPUs for deep learning is a must-read for us AIDLers. This time he update his popular article "Which GPU(s) to Get for Deep Learning" to include the latest RTX 2080. We like his conclusion about RTX 2080 than 2080 Ti: he believes that 2080 is more cost-effective.

[timdettmers.com](http://timdettmers.com/2018/08/21/which-gpu-for-deep-learning/)

---

### [Layman Description of Technical Terms in Deep Learning. ](https://www.facebook.com/photo.php?fbid=1799482573451324&set=gm.706159236443628&type=3&theater&ifg=1)

Here is a nice layman description of deep learning terminologies.

[facebook.com](https://www.facebook.com/photo.php?fbid=1799482573451324&set=gm.706159236443628&type=3&theater&ifg=1)

---

### [Understanding an Algorithm](https://twitter.com/fchollet/status/1033446573030567936)

Many of you asked AIDL whether you can understand deep learning after taking several beginner courses. As ML practitioners, our answer is to make sure you can implement classic algorithms in training or inference yourself, compare your work with SOTA, and understand the strengths and weaknesses of various open source package down to the code level.

We think François Chollet explains better:

"A popular quote goes "if you can't explain it in simple terms, you don't understand it well enough" (often incorrectly attributed to Einstein or Feynman).

I think a more accurate take is: "if you can't explain it in arbitrarily precise terms, you don't understand it well enough""

"In particular, if you understand something clearly, you should be able to describe it in precise algorithmic terms to a computer: you should be able to implement it from scratch (as a simulation, as a framework, etc).""

[twitter.com](https://twitter.com/fchollet/status/1033446573030567936)

---

### [OpenAI Five Lost to Human Experts in Dota 2](https://blog.openai.com/the-international-2018-results/)

Few weeks ago, we learn that OpenAI created [OpenAI Five](https://blog.openai.com/openai-five/) to compete in one of the most competitive eSport game: Dota 2. We have covered previous Open AI's Bot for DotA at length in [Issue 25 Fact-checking section](http://aidl.io/issues/25#start), we noted that it would be much tougher to move from a 1v1 mode to 5v5 mode because that require learning, complex strategy. But then OpenAI surprised us by showing that they can beat semi-pros in 5v5! So we did feel optimistic for the prospect for this week game at The International.

The difference between "The International" Match and the previous report, (also shared in this issue) is that the bot was dealing with semi-pro rather than genuine professional players. Unfortunately OpenAI failed. But then when you look at data and the phenomena they saw, we might be just hitting a scalability problem. Perhaps training for few more months would make the bot strong enough. See our analysis in the next item.

[openai.com](https://blog.openai.com/the-international-2018-results/)

---

### [OpenAI Five](https://blog.openai.com/openai-five/)

We included an an older link from OpenAI so that readers can have a sense of previous OpenAI bot publicized in Jun this year. One major difference, as we mentioned previously is that this time OpenAI bot is dealing with pro players who collect prize money for living. More importantly is that three of the players were playing together competitively.

So what can we say about the strength of current OpenAI Five? First of all, when the players are at solo [MMR](https://dota2.gamepedia.com/Matchmaking_Rating) around 5500, Five doesn't seem to have problem to beat the team formed by the players in that level. Whereas the pros Five deal with have MMR rating 7000+ (e.g. [xiao8's rating is 7333](https://www.dotabuff.com/players/98887913)). So just like machine's long history of defeating humans in chess, we might be just looking at a scalability problem.

You may ask: is it a scalability problem which we can solve in reasonable amount of time? For example, it seems that machines MMR rating doesn't just improve linearly over time. For example, we know that from March to June, a three month period, we see the bot trained from scratch can now beat a semi-pro at 5500, but then another three month period of time from June to now, machines don't quite make up the gap of 1800 points.

Our discussion so far is based on solo MMR, if you look at the players records, team MMR could be a better metric to decide relative strength of a team. Would it be possible to estimate that number? So far, we don't see such number published yet.

The true picture is also obscured by the fact that there are change of rules of courier. As OpenAI point out, it forces the machine to use a more aggressive strategy, which humans can exploit.

If we were OpenAI researchers, we would probably spend time to analyze the two lost games, and ask how can we learn even faster than now? Given what we see so far, we still place our bet on the machine, and it sounds like we are almost there.

[openai.com](https://blog.openai.com/openai-five/)

## About Us

This newsletter is published by [Waikit Lau](https://twitter.com/waikit) and [Arthur Chan](https://twitter.com/arthchan2003). We also run Facebook's most active [A.I. group](https://www.facebook.com/groups/DeepNetGroup) with 169,000+ members and host an occasional ["office hour"](https://www.youtube.com/channel/UC3YM5TEbSqIpFGH85d6gjKg) on YouTube. To help defray our publishing costs, you may donate via [link](http://paypal.me/aidlio/9). Or you can donate by sending Eth to this address: 0xEB44F762c58Da2200957b5cc2C04473F609eAA65.

**Join our community for real-time discussions here:** [Expertify](https://expertify.co)

Artificial Intelligence and Deep Learning Weekly
