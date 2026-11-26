---
title: "A View on Version Control Systems"
date: 2013-11-23
categories: ["Version Control"]
tags: ["CVS", "GIT", "SVN"]
---

# A View on Version Control Systems

Ask 10 persons about what is the best version control system, they will come up with 10 different answers. You might hate it, but some people still think rcs and cvs is the thing. Some believe since subversion is a drop-in replacement of cvs so it is the best. Some told me that that VisualSourceSafe is still their tool of the choice. "Because we are using Windows."

No matter what people's choice are, version control always sticks to an organization for long long time. What should you learn as a programmer? My take: *All of them* and then use the one when appropriate.

In another words, I was an agnostic user. So why my view is useful?

Reason Number 1: If you work in software for a while, you always hear people here and there proclaim the superiority of their favorite programming language, IDE, platform. They give you a feeling that feel "damn good" about it. *I honestly don't*. Programming is fun and stuffs. But for most parts, I do it for living. So my criterion is that it has to be practical and efficient. Programmers who are very evangelical about their tools are great turn-off for me. Not to say, if there are institutional or political perspective when someone tries to push a tool, it only makes everyone suffocates.

Reason Number 2: I am agnostic but I did make a choice at the end. Hopefully this article is more objective than many of those who feel "damn good" about their choice of tools.

So this is my take and I hope this is helpful for you. Before I say anything about any systems, I will bring up a trivial choice about version control: 

## Do No Version Control

"You should grow up."

That's what I said to many seemingly intelligent people who wrote smart algorithms but never control the source code. They may be very experienced researchers who are in the position of having no need to write any program in their lives. They may be very talented programmers who can write 1000 lines of code without any mistakes. They may be actually smart and can discern small issues in 10000 lines of code with a glance. They might simply dislike the idea of check-in. They might feel their code is not perfect enough or they don't want to expose themselves to any responsibility

But what they should do is to grow up.

Why? Let me first give you some exceptions of when you can skip version control: 
1. As a programmer, you only need to work alone for all of your life.
2. If you could, in some method, be able to record all 1000 changes in previous years in some form. I think that's okay, I guess it's a bit tedious. You are still a very organized and when there are issues you should be able to look up your notes.
3. You can remember all your changes. People who has eidetic memory can do such things.
4. You only learn programming for around a year or so. You simply don't know better.

If these 4 exceptions applied to you, I have nothing to say. Do whatever you like in programming. Version control is nothing important at all.

But now, when you need to work with some other people and find it necessary to record your changes. You have some experience and certainly realize you can't remember every single thing like Sheldon Cooper. (Breaking exceptions 1,2,3 and 4 already.) Then version control becomes a necessity.

For me, when I start to work on a decoder in Hong Kong, I found that I need to share the code. My paper record, already filled in 6 volumes of notebooks, can no longer caught up with complexity of my work. I certainly don't have photographic memory. That was when I realized version control is necessary. Here comes my version control system : CVS 

## CVS

I was using CVS in the company Speechworks. Discovering CVS helps my programming and paper writing a lot. Many of my early papers were checked-in into a self-made CVS repository.

If your programming is very simple and you don't expect too many changes in the directory structure. CVS is fine. "cvs co" checkout the code, "cvs update" update the code, "cvs commit" will check-in your code. Nice and easy.

The simplicity stops there. Once you need to check-in a binary file. Your cvs add needs to add -kb. Weird? Isn't it? But that's what many people have been doing for decades? How about directory? Once you add a directory to your file structure. You can't version control the directory. If you want to change the directory location, you need to *manually** do a mv in the repository*. Scary? If there are deadlocks, you need to ask your admin to remove a special lock file residing on the directory. Obviously you need to be lucky to see if you can connect to a cvs server.

The reason is that CVS is essentially a hacked-up of an older version control system RCS, which doesn't even allow concurrency. (Therefore the 'C' in CVS, stands for concurrency.) RCS based its system using text files. There are many issues with such approach. Permission can be a problem. But then, as CVS was thought of a dropped-in replacement of RCS. So no big deal, a lot of people were using it.

At the time when I first start using version control, there are not many free choices. So I went with CVS for 3.5 years. That's very closed to end of my employment from CMU. That was the time, couple of us realized CVS has too many issues to move forward with. All the small issues I mentioned can eat you up for a day. This makes a very scary trend for developers. Developers are either checking in too quickly. For fear anything they've done was lost. Or they refrain from check-in until things are very stable. Both are bad.

That was the time I started to use SVN. 

## Subversion

Subversion, was meant to be an improvement of CVS. In a way it is. It solves many of the problems I mentioned about CVS. Files can now checked in regardless of whether they are text or binary. You can version directory, you can version file removal. The thing I like most is that versioning become a package-based rather than a file-based business. It reduces much confusions when you need to work with a huge package.

There are still issues. The major one is *speed.* I remember checking out a SVN project for around 1.5 year took 30 minutes. I remember my boss yelled at me as he couldn't check-in stuffs into subversion. I remember the guys ended up trying to write something on SVN and make sure all the tools can be used in practice.

But the major issue is still *speed.* Here is why, let's say you are a working programmer, most of the time, your life really comes down to some suited dudes giving you 1) random tasks 2) with random length of completion 3) at a random time. So chances are while you were assigned to complete a feature which can take 2 weeks. Suited dudes will come by and say we need to fix a bug in the GUI today! ("And you can't have lunch!") So no matter what you do, being able to manipulate the source tree as quickly as you can is extremely crucial. My many late nights were caused by slow/broken connection to the SVN server. Doing certain things everyday is also impossible, e.g. do a clean check-out and test. It got stuck from time-to-time.

Branching is also discouraged. SVN is better on this regard. But CVS is the worst. This ultimately makes SVN still not a perfect tool for version control. After all when you branch in SVN, unless you are careful, the check-out time will be longer. So of course, we end-up still having people who refrain from check-out/check-in. Despite their bosses are yelling at them, I can only offer them (and myself) sympathy. 

## My Denial Period

After I used subversion, destiny treated me badly: I need to return to a CVS-based environment and I cursed every moment of it. But that was the time I heard about GIT. I've been to presentations by many intelligent people. They tried to convince me with thousands different reasons. e.g. They will tell you GIT, as a distributed system can use to mimic any centralized version control system. They will tell you branching is such a great thing when using GIT. They will tell you all the tools of GIT are very refined and much better than CVS and SVN.

Now strangely, there was a period of time I don't really give too much thought on GIT at all. The reason is a little bit subtle: once you have been through couple of version control systems, you realized that version control is an imperfect business. True, you can't version control a directory in CVS. But oh well, you don't have start another directory all the time.......

And with a new version control system, that means there are more changes to your environment. Quite frankly, every couple of years there would be a new system come up. Are we sure we really have something better?

That's what I thought. So *shame on me*, for couple of years I was unconsciously *against* adopting GIT. But just like many prudent programmers, my reason is well calculated. Some people will say, "*You just need to read a little bit about GIT, you will learn that it's **good**".*  Well, when you are prudent, you probably have some stuffs to keep you busy! When is the time to read up?

## GIT

My bad, but my peer GIT evangelists did a bad job too. The truth is many programmers calculates like me before they pick up a new tool.

So let me tell you *one and only one important reason* why GIT is a good choice for version control. It is a keyword I mentioned more than once in this article already:

**SPEED!!!**

Yes. Speed. Speed is the ultimate reason why any CVS and SVN user would want to switch to GIT. True, GIT can simulate a centralized system. *But who cares?* If system B can only simulate system A, why the hack do I care about system B at all? The ultimate answer is speed. GIT was first developed to improved transmission of other version control system. So a local check-out is usually much faster than SVN and CVS.

How about check-in? Again, speed is faster in GIT. Because GIT is using distributed version control, check-in is fast and you mostly clean your system until you push to the centralized server. Disaster recovery is better.

How about branching? Again, speed is faster in GIT. Because GIT branch by creating a pointer on the tree object. No big deal in making a branch. You can then frequently branch. It is *enjoyable* to branch. Branching even becomes part of your routine eventually!

That's not because GIT is good at branching, it's because GIT is *fast* at branching.

So the ultimate reason of why one wants to use GIT is *speed*. You can hold other point of view, but those views will make it very hard for your colleague to be convinced. You will also make the same mistakes I made: get too used to your own version control system. 

## Some Final Notes

I am not the first person who advocate GIT. Nor I would be the last one. So the point of this article is really not about whether you should use GIT or not.

I believe the point is this kind of story is that it teaches you **why technical changes in an organization are that tough**. Many people who have years of experience on the belt, end up refraining new and good changes. The worst thing is, just like me, they are have good-intention to be stubborn.

Another point is that technical ideas are necessarily spread even if they are good. In my case, logic and experience, shielded me from using GIT. Chances are 10 years later when somebody told me about a new super-duper version control system, I will refrain from it too!

How do I see my own mistakes? I guess my take is that before you make a decision on using/learning a certain tools, try to use the system at least once. Read at least one book is also useful. e.g. I read the following books on CVS, SVN and GIT: 
1. CVS Book by Karl Fogel
2. Version Control with Subversion by C. Michael Pilato, Ben Collins-Sussman, Brian W. Fitzpatrick
3. Pro GIT by Scott Chacon

In any case, thanks for reading this far.

Arthur
