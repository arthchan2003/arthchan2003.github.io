---
title: "Some Speculations On Why Microsoft Tay Collapsed"
date: 2016-03-28
categories: ["ANN", "deep learning", "Language Modeling", "SMT"]
tags: ["chatbot", "deep learning", "DNN", "LSTM", "RNN", "SMT"]
---

# Some Speculations On Why Microsoft Tay Collapsed

[Microsoft's Tay](http://techcrunch.com/2016/03/23/microsofts-new-ai-powered-bot-tay-answers-your-tweets-and-chats-on-groupme-and-kik/), following [Google AlphaGo](https://deepmind.com/alpha-go.html), was meant to be yet another highly intelligent A.I. program which fulfill human's long standing dream: a machine which can truly converse. But as you know, [Tay fails spectacularly](http://tech.firstpost.com/news-analysis/microsoft-takes-down-ai-chatbot-tay-after-twitter-teaches-it-racism-305858.html). To me, this is a highly unusual event, part of it is that Microsoft's another conversation agent, [Xiaoice, was extremely successful in China](http://www.businessinsider.com/microsoft-xiaoice-turing-test-in-china-2016-2?r=UK&IR=T). The other part is MSR, is one of the leading sites on using deep learning in various machine learning problems. You would think that a major P.R. problem such as [Tay confirming "Donald Trump is the hope", and purportedly support genocide ](http://www.mediaite.com/online/twitter-turns-tay-into-a-racist-sexist-holocaust-denying-bot-in-less-than-24-hours/)should be weeded out before launch.

As I read many posts in the past week attempted to describe why Tay fails, sadly they offer me no insights. Some even written from respected magazines, e.g. in [New Yorkers](http://www.newyorker.com/tech/elements/ive-seen-the-greatest-a-i-minds-of-my-generation-destroyed-by-twitter)' "*I’ve Seen the Greatest A.I. Minds of My Generation Destroyed by Twitter"* at the end the author concluded, 

> "If there is a lesson to be learned, it is that consciousness wants conscience. Most consumer-tech companies have, at one time or another, launched a product before it was ready, or thought that it was equipped to do something that it ended up failing at dismally. "

While I always love the prose from New Yorkers, there is really no machine which can mimic/model human consciousness (yet). In fact, no one really knows how "consciousness" works, it's also tough to define what "consciousness" is. And it's worthwhile to mention that chatbot technology is not new. Google had released similar technology and get great press. ([See here](http://www.wired.com/2015/06/google-made-chatbot-debates-meaning-life/)) So the New Yorkers' piece reflect how much the public *does not understand technology.*  As a result, I decided to write a Tay's postmortem myself, and offer some thoughts on why this problem could occur and how one could actively avoid such problems.

Since I try to write this piece for general audience, (say my facebook friends), the piece contains only small amount of technicalities. If you are interested, I also list several more technical articles in the reference section. 

## How does a Chatbot work? The Pre-Deep Learning Version

By now, all of us use a chat bot or two, there is obviously Siri, which perhaps is the first program which put speech recognition and dialogue system in the national spotlight. If you are familiar with history of computing, you would probably know [ELIZA](https://en.wikipedia.org/wiki/ELIZA) [1], which is the first example of using rule-based approach to respond to users.

What does it mean? In such system, usually a natural language parser is used to parse human's input, then come up with an answer with some pre-defined and mostly manually rules. It's a simple approach, but when it's done correctly. It creates an illusion of intelligence.

Rule-base approach can go quite far. e.g. The [ALICE](https://en.wikipedia.org/wiki/Artificial_Linguistic_Internet_Computer_Entity) language is a pretty popular tool to create intelligent sounding bot. (History as shown in [here](http://www.alicebot.org/anatomy.html).) There are many existing tools which help programmers to create dialogue. Programmer can also extract existing dialogues into the own system.

The problem of rule-based approach is obvious: the response is rigid. So if someone use the system for a while, they will easily notice they are talking with a machine. In a way, you can say the illusion can be easily dispersed by human observation.

Another issue of rule-based approach is it taxes programmers to produce a large scale chat bot. Even with convenient languages such as [AIML](http://www.alicebot.org/aiml.html) (ALICE Markup Language), it would take a programmer a long long time to come up with a chat-bot, not to say one which can answer a wide-variety of questions. 

## Converser as a Translator

Before we go on to look at chat bot in the time of deep learning. It is important to ask how we can model conversation. Of course, you can think of it as ... well... we first parse the sentence, generate entities and their grammatical relationships, then based on those relationships, we come up with an answer.

This approach of decomposing a sentence to its element, is very natural to human beings. In a way, this is also how the rule-based approach arise in the first place. But we just discuss the weakness of rule-based approach, namely, it is hard to program and generalize.

So here is a more convenient way to think, you could simply ask, "Hey, now I have an input sentence, what is the best response?" It turns out this is very similar to the formulation of statistical machine translation. "If I have an English sentence, what would be the best French translation?" As it turns out, a converser can be built with the same principle and technology as a translator. So all powerful technology developed for statistical machine translation (SMT) can be used on making a conversation bot. This technology includes I.B.M. models, phrase-based models, syntax model [2] And the training is very similar.

In fact, this is how many chat bots was made just before deep-learning arrived. So some method simply use an existing translator to translate input-response pair. e.g. [3]

The good thing about using a statistical approach, in particular, is that it generalizes much better than the rule-based approach. Also, as the program is based on machine learning, all you have to do is to prepare (carefully) a bunch of training data. Then existing machine learning program would help you come up with a system automatically. It eases the programmer from long and tedious tweaking of the bot. 

## How does a Chatbot work? The Deep Learning Version

Now given what we discuss, then how does Microsoft's chat bot Tay works? Since we don't know Tay's implementation, we can only speculate: 
1. Tay is smart, so it doesn't sound like a purely rule-based system. so let's assume it is based on the aforementioned "converser-as-translator" paradigm.
2. It's Microsoft, there got to be some deep neural network. (Microsoft is one of the first sites picked up the modern "deep" neural network" paradigm.)
3. What's the data? Well, given Tay is built for millennials, the guy who train Tay must be using dialogue between teenagers. If I research for Microsoft [4], may be I would use data collected from Microsoft Messenger or Skype. Since Microsoft has all the age data for all users, the data can easily be segmented and bundled into training.

So let's piece everything together. Very likely, Tay is a neural-network (NN)-based program which can intelligently translate an user's natural language input to a response. The program's training is based on chat data. So my speculation is the data is exactly where things goes wrong.  Before I conclude, the neural network in question is likely to be an Long-Short Term Model (LSTM). I believe Google's researchers are the first advocate such approach [5] ([headlined last year and the bot is known for its philosophical undertone](http://www.wired.com/2015/06/google-made-chatbot-debates-meaning-life/).) Microsoft did couple of papers on how LSTM can be used to model conversation. [6]. There are also several existing bot building software on line e.g. Andrej Karpathy 's [char-RNN](https://github.com/karpathy/char-rnn). So it's likely that Tay is based on such approach. [7]

## What goes wrong then?

Oh well, given that Tay is just a machine learning program. Her behavior is really governed by the training material. Since the training data is likely to be chat data, we can only conclude the data *must contain some offensive speech,* given the political landscape of the world. So one reasonable hypothesis is the researcher who prepares the training material hadn't really filter out topics related to hate speech and sensitive topics. I guess one potential explanation of not doing that is that filtering would reduce the amount of training data. But then given the data owned by Microsoft, it doesn't make sense. Say 20% of 1 billion conversation is still a 200 million, which is more than enough to train a good chatterbot. So I tend to think the issue is a human oversight. 

And then, as a simple fix, you can also give the robots a list of keywords, e.g. you can just program a simple regular expression match of "Hitler", then make sure there is a special rule to respond the user with "No comment". At least the consequence wouldn't be as huge as a take down. That again, it's another indication that there are oversights in the development. You only need to spend more time in testing the program, this kind of issues would be noticed and rooted out. 

## Conclusion

In this piece, I come up with couple of hypothesis why Microsoft Tay fails. At the end, I echo with the title of New Yorker's piece: "I’ve Seen the Greatest A.I. Minds of My Generation Destroyed by Twitter" .... at least partially. Tay is perhaps one of the smartest chatter bots, backed by one of the strongest research organization in the world, trained by tons of data. But it is not destroyed by Twitter or trolls. More likely, it is destroyed by human oversights and lack of testing. In this sense, it's failure is not too different from why many software fails.

Reference/Footnote

[1] Weizenbaum, Joseph "ELIZA—A Computer Program For the Study of Natural Language Communication Between Man And Machine", Communications of the ACM 9 (1): 36–45,

[2] Philip Koehn, Statistical Machine Translation

[3] Alan Ritter, Colin Cherry, and William Dolan. 2011. Data-driven response generation in social media. In Proc. of EMNLP, pages 583–593. Association for Computational Linguistics.

[4] Woa! I could only dream! But I prefer to work on speech recognition, instead of chatterbot.

[5] Oriol Vinyal, Le Quoc, [A Neural Conversational Model](http://arxiv.org/abs/1506.05869).

[6] Jiwei Li, Michel Galley, Chris Brockett, Jianfeng Gao, and Bill Dolan, A Diversity-Promoting Objective Function for Neural Conversation Models

[7] A more technical point here: Using LSTM, a type of recurrent neural network (RNN), also resolved one issue of the classical models such as IBM models because the language model is usually n-gram which has limited long-range prediction capability.
