---
title: "Python multiprocessing"
date: 2013-03-18
categories: ["cmu sphinx", "multiprocessing", "Python"]
---

# Python multiprocessing

As my readers may noticed, I haven't updated this blog as I have pretty heavy workload. It doesn't help that I was sick in the middle of March as well. Excuses aside though, I am happy to come back. If I couldn't write much about Sphinx and programming, I think it's still worth it to keep posting links.

I also come up with requests on writing more details on individual parts of Sphinx. I love these requests so feel free to send me more. Of course, it usually takes me some time to fully grok a certain part of Sphinx and I could describe it in an approachable way. So before that, I could only ask for your patience.

Recently I come up with parallel processing a lot and was intrigued on how it works in the practice. In python, a natural choice is to use the library multiprocessing. So here is a simple example on how you can run multiple processes in python. It would be very useful in the modern days CPUs which has multi-cores.

Here is an example program on how that could be done:

```
1:  import multiprocessing  
2:  import subprocess  
3:    jobs = []  
4:    for i in range (N):  
5:      p = multiprocessing.Process(target=process,   
6:                      name = 'TASK' + str(i),   
7:                      args=(i, ......  
8:                    )  
9:      )  
10:     jobs.append(p)  
11:     p.start()  
12:   for j in jobs:  
13:     if j.is_alive():  
14:        print 'Waiting for job %s' %(j.name)  
15:        j.join()  
```

The program is fairly trivial. Interesting enough, it is also quite similar to the multithreading version in python. Line 5 to 11 is where you run your task and I just wait for the tasks finished from Line 12 to 15. 

It feels little bit less elegant than using Pool because it provides a waiting mechanism for the entire pool of task. Right now, I am essentially waiting for job which is still running by the time job 1 is finished. 

Is it worthwhile to go another path which is thread-based programming. One thing I learned in this exercise is that older version of python, multi-threaded program can be paradoxically slower than the single-threaded one. (See this [link ](http://eli.thegreenplace.net/2012/01/16/python-parallelizing-cpu-bound-tasks-with-multiprocessing/)from Eli Bendersky.) It could be an easier being resolved in recent python though.

Arthur

---

## Comments

**602e03f4-2327-11e2-8544-000bcdcb8a73** (2013-03-22):

Hello,

Here's another article request -

In what ways does sphinx3_align differ from sphinx3_decode with constrained finite state graph? For ex. I can align "I'm a girl" with an audio and can also decode the same audio with an FSG "I'm -&gt; a -&gt; girl"

Are there any algorithmic/practical differences?

**三十三博** (2013-03-22):

The shorter answer is their internal structure are completely different. So you might expect a lot of difference between the two.

But then again, once you specify the same input. There are a lot of nuances in the algorithm. So I might write about it soon.

