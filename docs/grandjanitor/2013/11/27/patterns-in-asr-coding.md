---
title: "Patterns in ASR Coding"
date: 2013-11-27
categories: ["Programming"]
tags: ["ASR", "coding"]
---

# Patterns in ASR Coding

Many toolkits in ASR appears in the form of unix executables. But the nature of ASR tool is quite a bit different from general unix tools. I will name 3 here: 
1. **Complexity:** A flexible toolkit also demands developers to have an external scripting framework. In SphinxTrain, it used to be glued by perl, now by python. Kaldi, on the other hand, is mainly glued by shell script. I heard Cambridge has its own tools to do experiment correctly.
2. **Running Time:** Coding ASR is that it takes long time to verify if something is correct. So there are things you can't do: a very agile type of development by code-and-test doesn't work well. I have seen people implemented, but it leaves so many bugs in the codebase.
3. **Numerical Issues:** Another issue is that much coding in numerical algorithm could cause subtle changes of the results, it is tricky to code these changes well. When these changes penetrated to production, it is usually very hard to debug. When such changes affect performance, the result could be disastrous to you and your clients.

In a nutshell, we are dealing with a piece of software which is *complex and* *mission-critical*. The issue is how do you continue develop and maintain such software.

In this article, I will talk about how this kind of coding can be done right. You should notice that I don't favor a monolithic design of experimental tools. e.g. "why don't we just write one single tool that does everything (to train/to decode)?" There is a place of those mindsets in software engineering. e.g. Mercuria is designed in that way and I heard it is very competitive to GIT. But I prefer a Unix-tool type of design which is closed to HTK, Sphinx, Kaldi. i.e. you write many tools and each of them has different purposes. You then simply glue them together for your own purpose. I will call all the code changes in these little unix tools as **code-level changes.** While changes in the scripting level simply as **script-level changes**.

Many of these thought are taught to me by experienced people in the field. Some can be applicable in other fields: such as *Think Before Code, Conclude from your Test*. Other can be applied to machine-learning specific problem: *Match Results Numerically,* *Always Record Results.* 

## Think Before Code

In our time, the agile development paradigm is very popular. May be too popular, in my view. Agile development is being deployed in too many places which I think inappropriate. ASR is one of them.

As a coder in ASR, what you usually do are two things: making code-level changes (in C/C++/Java) or script-level changes (in Perl/Python). In a nutshell, you are doing programming in a complex piece of software. Since testing could take a long time. Code-and-test type paradigm won't work for you too well.

On the other hand, deliberate-and-slow thinking is your first line of defense for any potential issues. You should ask yourself couple of questions before any changes: 
1. Do you understand the purpose each of the tools in your script?
2. Do you understand the underlying principle of the tool?
3. Do you understand the I/O?
4. Would you expect that any changes would change the I/O at all?
5. For each tool, do you understand the code?
6. What is your change?
7. Where are your changes? How many things you need to change? (10 files, 100 files? List them out.)
8. In your head, after you make the change, do you expect your change will work? Why? Convince yourself.

These are some of the questions you should ask yourself. Granted, you don't have to all answers, but the more you know, you would reduce any potential future issues . 

## Conclude from your Tests, not from your Head

After all the thinking, are we done? No, you should still test your code, in fact you should test your code like a professional tester. Bombard your well-thought out program with test. Fix all warnings from compilers, valgrind it to fix leaks. If you don't fix a certain thing, make sure you have a very very good reason. Because any changes in your decoder and trainer could have many ramifications to upper-layer of software, to you and to your colleagues.

The worst way to think about ASR coding is to say "it should work!". No. Sometimes, *it doesn't*. You are too naive for not testing the code.

Who makes such mistakes? It is hard to nail it down. My observation is that those who always try to think through any problems in their head and have strong conviction that they are right. They are usually fresh grads (all kinds, Bachelors? Masters? PhDs? They are everywhere.) Or people who only work on research and hadn't done real-life coding that much. In a nutshell, it is a "philosophy"-thing. Some people tend to think their thought *apriori* will work as it is. This is a 8-th century thinking. Always verify your changes with experiments.

Also. No one say, testing always eliminate all problems. But if you *think and test*. The chances of making mistakes will be tremendously reduced. 

## Scale It Down

The issue about large amount of testing in ASR it that it takes a long time. So what should you do?

Scale it down.

e.g. Suppose you have 1000 utterance test, you want to reduce the testing time. Make it a 100 utterance test, or even 10. That allows you to verify your change quickly.

e.g. If you have an issue appears in 1 min utterance, try to see if you can repeat the same issue on a 6 second one.

e.g. If you are trying a procedure for 1000 hour of data, try to test it with 100 hour first.

These are just some examples. This is a very important paradigm because it allows you to move on with your work faster. 

## Match Results Numerically

If you make an innocuous change, but the results are slightly different. You should be very worried.

The first question you should ask is "How can this happen at all?" For example, let's say if you add a command-line option, your decoding results shouldn't change.

Are there any implicit or explicit random number generators in the code? Or have you accidentally take in users' input? Or else, how come your innocuous change would cause changes in results?

Be wearied about any one who say "It is just a small change. Who cares? The results won't change." No, always question the size of the changes. Ask for how many significant digits are match if there are any difference. If you could try to learn more about intrinsic error introduced by floating point calculation. (e.g. "[What Every Computer Scientist Should Know About Floating Point Calculation](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=2&cad=rja&ved=0CDkQFjAB&url=https%3A%2F%2Fece.uwaterloo.ca%2F~dwharder%2FNumericalAnalysis%2F02Numerics%2FDouble%2Fpaper.pdf&ei=802WUqmsOurKsQT1v4KYDQ&usg=AFQjCNEdaRdrUdVsgp-B6cqeLd9HS9Ezkg&sig2=iRnGW4IxQ_5em-uSaSYucQ&bvm=bv.57155469,d.cWc)" is a good start.)

There is another opposing thought: i.e. It should be okay to have some numerical changes. I don't really buy it because once you allow yourself to drift 0.1% 10 times, you will have a 1% drift which can't be explained. The only times you should let yourself go is you encountered randomness you can't control. Even in those cases, you should still explain why your performance would change. 

## Predict before Change

Do you expect your changes would give better results? Or worse results? Can you explain to yourself why your change could be good/bad?

In terms of results, we are talking about mainly 3 things : word-error-rate, speed and usage of memory. 

## Setup an Experimental Framework

If you are anyone serious about ML or ASR, you should have tested your code many times. If you have tested your code many times, you will realize you can't use your brain to manipulate all your experiments. You need a system.

I have written [an article in V1](http://grandjanitor.blogspot.com/2013/03/good-asr-training-system.html) about this subject. In a nutshell, make sure you can repeat/copy/record all your experimental detail including versions of binary, parameters. 

## Record your Work

With complexity of your work, you should make sure you keep enough documentation. Here are some ideas: 
1. *Version Control System* : for your code
2. *Bug tracking* : for your bugs and feature requests
3. *Planning document*: for what you need to do in a certain task
4. *Progress Note:* record in a daily basis on what you have done/learned experimentally.

Yes, you should have many records by now. If you don't have any, I feel worried about you. Chances are some important experimental details were forgotten. Or if you don't see what you are doing is an experiment...... Woa. I wonder how you explain what you do to other people. 

## Conclusion

That's what I have today. This article summarizes many important concepts on how to maximize your success of doing any coding changes. Some of these are habits which take time to setup and get used to. Though from my experience, these habits are invaluable. I found myself writing features which have less problems. Or at least when there are problems, they are problems I hadn't and couldn't anticipate.

Arthur

---

## Comments

**Luk Lau** (2013-12-16):

There are a lot of practices under the umbrella of "Agile". Beside XP practices, I believe you will find value in the BDD approach (http://cukes.info).

cheers

luk

