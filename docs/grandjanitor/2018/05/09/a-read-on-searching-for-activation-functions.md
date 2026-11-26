---
title: "A Read on \"Searching for Activation Functions\""
date: 2018-05-09
---

# A Read on "Searching for Activation Functions"

(First published at AIDL-LD and AIDL-Weekly)

Perhaps the most interesting paper last week is the Swish function. Here are some notes:

\* Swish is extraordinarily simple. It's just swish(x) = x \* sigmoid(x). \* Derivative? swish'(x) = swish(x) + sigmoid(x) (1 - swish (x)) Simple calculus.  \* Can you tune it? Yes, there is a tunable version which the parameter is trainable. It's call Swish-Beta which is x \* sigmoid( Beta \* x) \* So here's an interesting part of why it is a "self-gating function". So.... if you understand LSTM, essentially it introduced a multiplication sign. The multiplier strengthen the gradient and effectively resolve the vanishing/exploding gradient problem. e.g. input gate and forget gate, give you weights of "how much you want to consider the input" and "how much much you want to forget". ([http://colah.github.io/posts/2015-08-Understanding-LSTMs/](https://l.facebook.com/l.php?u=http%3A%2F%2Fcolah.github.io%2Fposts%2F2015-08-Understanding-LSTMs%2F&h=ATMl6maMcciWBM6BLtWDsAGyaOeza1xElwe1j-RvbkMa1qI7zNl2BwI-SjHauhMSzcxQnW2ag3k0C5W6UFIV5TueXhygQNHBaA2UKgNaDs1msoCdi8EfGmHcRXjvHC3MC9CqxYTxPn3T7HriAhlZi5Ub)) \* So swish is not too different - there is the activation function but it is weighted by the input itself. Thus the term self-gating. In a nutshell, in plain English, "because we multiply". \* It's all good, but does it work? The experimental results look promising. It works on Cifar-10, Cifar-100. On Imagenet, it beats Inception-v2 and v3 when swish replace ReLU. \* It's worthwhile to point out the latest Inception is in v4. So the imagenet number is not beating stoa even within Google, not to say the best number in Imagenet 2016. But that shouldn't matter, if something consistently improve on some models of Imagenet, it is a very good sign it is working. \* Of course, looking at the activation function. It introduces a multiplication. So it does increase computation when compare with a simple ReLU. And that seems to be the complaint I heard. 

That's what I have. Enjoy!
