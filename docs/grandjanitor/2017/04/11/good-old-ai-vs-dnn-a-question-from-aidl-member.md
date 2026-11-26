---
title: "Good Old AI vs DNN - A question from AIDL Member"
date: 2017-04-11
---

# Good Old AI vs DNN - A question from AIDL Member

Redacted from [this discussion](https://www.facebook.com/groups/DeepNetGroup/permalink/414501095609445/) at AIDL.

From [Ardian Umam](https://www.facebook.com/mamu.naidra?fref=nf) (shortened, rephrased): "Now I'm taking AI course in my University using Peter Norvig and Stuart J. Russell textbook. In the same time, I'm learning DNN (Deep Neural Network) for visual recognition by watching Standford's Lecure on CNN (Convolutional Neural Networks) knowing how powerful a DNN to learn something from dataset. Whereas, on AI class, I'm learning about KB (Knowledge Base) including such as Logical Agent, First Order Logic that in short is kind of inferring "certain x" from KB, for example using "proportional resolution".

My question : "Is technique like what I learn in AI class I describe above good in solving real AI problem?" I'm still not get strong intuition about what I study in AI class in real AI problem."

Our exchange:

My answer: "We usually call "Is technique .... real AI problem?" GOAI (Good Old Artificial Intelligence). So your question is weather GOAI is still relevant.

Yes, it is. Let's take search as an example. More complicated systems usually have certain components in search. e.g. Many speech recognition these days still use Viterbi algorithm which is large-scaled search. NNMT type of technique still requires some kind of stack decoding. (Edit, was beam search, but I am not quite sure.)

More importantly, you can see many things as a search. e.g. optimization of a function, you can solve it by Calculus, but in practice, you actually use search algorithm to find the best solution. Of course, in real-life, you rarely implement beam search to optimization. But idea of search would give you better feeling many ML algorithms like."

AU: "Ah, I see. Thank you [Arthur Chan](https://www.facebook.com/archan?hc_location=ufi) for your reply. Yes, for search, it is. Many real problems now are still utilizing search approach to solve. As for "Knowledge, reasoning" (Chapter 3 in the Norvig book) for example using "proportional resolution" to do inference from KB (Knowledge Base), is it still relevant?"

My Answer: "I think the answer is it is and it is not. Here is a tl;dr answer:

It is not: because many practical systems these days are probabilistic. So it makes Part V of Norvig's book \*feel\* more relevant now. Most people in this forum are ML/DL fans. That's probably the first feeling you should have in these days.

But then, it is also relevant. In what sense? There are perhaps 3 reasons. First is it allows you to talk with people who learn A.I. from the last generation, because people in their 50-60s (aka, your boss) learn solving AI problem with logic. So if you want to talk with them, learning logic/knowledge type of system would help. Also in AI, no one knows what topic would revive. e.g. Fractal is now the least talked-about topic in our community now. But you never know what happen in the future 10-20 years. So keep ing breath is a good thing.

Then there is the part of how you think about search, in both Norvig and Russell's books, the first few search problem is to solve logic problem such as first-order logic, chess. While they are only used in fewer system, compare to search which requires probabilities, they are much easier to understand. e.g. You may heard of people in their teens write their first chess engine, but I heard no one write (good) speech recognizer or machine translator before grad school.

The final reason is perhaps more theoretical: many DL/ML system you use, yeah... .they are powerful, but not all of them are making decision human understand. So they are not \*interpretable\*. That's a big problem. So it is still a research problem of how to link these system to GOAI-type of work."
