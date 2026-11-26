---
title: "Some Reflections on Programming Languages"
date: 2012-12-24
categories: ["C++", "java", "perl", "programming languages", "Python", "Thought"]
---

# Some Reflections on Programming Languages

This is actually a self-criticizing piece. Oh well, but call it reflection doesn't hurt.

When I first started out in speech recognition, I have a notion that C++ is the best language in the world. For daily work? "Unix commands such as cut, split work well. " To take care of most of my processing issues, I used some badly written bash shell. Around the middle of the grad school, I started to learn that perl is lovely for string processing. Then I thought perl is the best language in the world, except it is a bit slow.

After C++ and perl, I then learned C, Java, Python. A little bit of objective-C and sampled many other languages. For now, I will settle on C and Perl are probably the two languages I am most proficient. I also tend to like them the most. There is one difference between me and the twenty-something me though - instead of arguing which language is the best, I will simply go to learn more about any programming language in the world.

Take C as an example, many would praise it to be the procedure language which is closest to the machine. I love to use C and write a lot of my algorithms in C. But when you need to maintain and extend a C codebase, it is a source of a pain because, there is no inherent inheritance mechanism to work with, so a programmer needs to implement their own class-implementation. Many function pointers. There is also no memory-checking, so an extra step of memory checking is necessary. Debugging is also a special skill.

Take perl. It is very useful in text processing and has very flexible syntax. But this flexibility also makes perl script hard to read sometimes. For example, for a loop, do you want to implement it as a foreach-loop or by a map? Those confuse lesser programmers. Also, when you try to maintain large scale project with perl, many programmers remark to me OOP in perl seems to "just organize the code better".

How about C++? We love the templates, we love the structure. In practice though, the standard changes all the time. Most house fixes the compiler version to make sure their C++ source code compiled. 

How about Java? There is memory boundary checking. After a year or two on a dot-com, I also learned that Tomcat servlet is a thing in web development. It is also easy to learn and one mainstream programming language taught in school these days. Those I dig. What's the problem? You may say speed is an issue. Wrong. Many Java code can be optimized such that it is as fast as its C or C++ codebase. The issue in practice is that the process of bytecode conversion is non-trivial to many. That is why it raises doubts in a software team on whether the language is the cause of speed issues. 

For me, I also care about the fate of Java as an open language after Oracle bought Sun Microsystem.

How about Python? I guess this is a language I know least about. So far, it seems to take care of a lot of problems in perl. I found the regular expression takes some time to learn. Though other than that, the language is quite easy to learn and quite nice to maintain. I guess the only thing I would say it is the slight difference between different Python 2.X starts to annoy me. 

I guess a more important point here: every language has its strength and weakness. In real life, you probably need to prepare to write the same algorithm in all languages you know. So there is no room for you to say "Hey! Programming language A is better than programming language B. Wahahaha. Since I am using A rather than B, I rock, you suck!" No, rather you got to accept that writing in unfamiliar language is essential for tech person's life.

I learned this through my spiritual predecessor, Eric Thayer, who organized the source code of SphinxTrain. He once said to me, (I rephrase here,) "Arguing about programming languages is one of the most stupidest thing in the world."

Those words enlightened me. 

Perhaps that is why I have been reading "C Programming a Modern Approach", "The C++ Programming Language", "Java in a Nutshell", "Programming Perl" and "Programming Python" from time to time because I never feel satisfy with my skills on any of them. I hope to learn D and Go soon and make sure I am proficient in Objective-C soon. It will take me a lifetime to learn them, but on something deep like programming, learning, other than arguing, seems to be a better strategy to go.

Arthur
