---
title: "Subword Units and their Occasionally Non-Trivial Meanings"
date: 2013-01-29
categories: ["biphone", "diphone", "hetaphone", "phone", "phonemes", "quadphone", "quinphone", "subword units", "triphone"]
---

# Subword Units and their Occasionally Non-Trivial Meanings

While I was writing the next article on bw, I found myself forget the meaning of different type of subword units (i.e phones, biphones, diphones, triphones and such). So I decide to write a little note. 

On this kind of topics, someone would likely to come up and say "X always mean Y bla bla bla etc and so on." My view (and hope) is that the wording of a certain should reflect what it means. So when I hear a term and can come up with multiple definition in your head, I would say the naming convention is a little bit broken. 

Phones vs Phonemes  
Linguist distinguish between *phoneme* and *phone* The former usually means a kind of abstract categorization of a sound, whereas the latter usually mean the actual realization of a sound. 

In a decoder though, what you see most is the term phone.

#### Biphones vs Diphones

(Ref [here](http://www.academia.edu/213762/Acoustical_Modelling_of_Phone_Transitions_Biphones_and_Diphones_-_What_are_the_Differences)) " ..... one important diﬀerence between the two units. Biphones are understood tobe just left or right context dependent (mono)phones. On the other hand, diphones represent the transition regions that strech between the two ”centres” of the subsequent phones. "

So that's why there can be left-biphone and right-biphone. Diphones is intuitively better in synthesis.

Possible combination of left-biphones/right-biphones/diphones are all N^2. With N equals to the number of phones. 

Btw, the link I gave also has a term called "bi-diphone", which I don't think it's a standard term. 

#### Triphones

For most of the time, it means considering both left and right context. Possible combinations N^3. 

Quinphones

For most of the time, it means considering both the two left and two right contexts. Possible combinations N^5. 

#### **Heptaphones**

**  
**

For most of the time, it means considering both three left and three right contexts. Possible combinations N^7. 

#### "Quadphones" and Other possible confusions in terminology.

I guess what I don't feel comfortable are terms such as "Quadphones". Even quinphones and heptaphones can potentially means different things from time-to-time. 

For example, if you look at LID literature, occasionally, you will see the term quadphone. But it seems the term "phone 4-gram" (or more correctly quadgram...... if you think too much,) might be a nicer choice. 

Then there is how the context looks like: 2 left 1 right? 1 right 2 left? Come to think of it, this terminology is confusing for even triphones because we can also mean a phone depend on 2 left or 2 right phones. ASR people don't feel that ways probably because of a well-established convention. Of course, the same can be said for quinphone and hetaphones. 

Arthur
