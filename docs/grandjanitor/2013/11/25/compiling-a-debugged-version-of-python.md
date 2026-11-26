---
title: "How to Compile a Debugged Version of Python"
date: 2013-11-25
categories: ["Debugging"]
tags: ["debugging", "Python"]
---

# How to Compile a Debugged Version of Python

For the most time, you shouldn't need to care about the internals of python. It is usually thought as a tool and assumed to be bug-free.

Of course, there are moments you should question these assumptions. Sometimes, the interpreter fails itself. It could segfault, it could be too slow.

A more common scenario is that you write C-extension for a python and things are not working. So what do you do? You can go to stare at the source code and hope that you find the issues. Or you can just *debug the python*. e.g. you can simply see python as a program and your script as arguments. Most of the time, when your interpret the custom extension, it will just link it with the library you wrote.

If you want to do it right, you also want to have a debugged version of python. So the question you have is how to compile. Is it difficult? The answer is that compiling python is surprisingly simple. In fact, I think it is a very joyful activity. (That's just me......)

Anyway, the following is a procedure I used. I use Python2.7.5 as an example. It is so-called the old standard. The tip now is Python2.7.6. I think the same procedure works. 

## 1, Download Python Source Code

For Python2.7.5, you can do it by

wget http://www.python.org/ftp/python/2.7.5/Python-2.7.5.tgz 

## 2, Configure Python in Debug Mode

./configure --with-pydebug --prefix ./my_installation_path/ 

## 3, Compile and Install the debug version

make OPT='-g'

make install 

## Notes:

- Remember, valgrinding the debugged version of python will generates tons of messages (because valgrind would think much memory space was not freed.) So remember to use the right suppression file. See [http://svn.python.org/projects/python/trunk/Misc/README.valgrind](http://svn.python.org/projects/python/trunk/Misc/README.valgrind)
- You also need to reinstall all libraries that make your application works.
- And remember, different version of .pyc may not be compatible with each other. So make sure you use the correct version of python to rerun your applications.

Arthur
