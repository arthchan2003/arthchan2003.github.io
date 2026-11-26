---
title: "Sphinx 4 from a C Background : Setting up Eclipse as the IDE"
date: 2012-12-28
categories: ["beginner", "Eclipse", "installation", "jsapi", "package explorer", "problems windows", "Sphinx4", "subclipse", "svn", "tutorial"]
---

# Sphinx 4 from a C Background : Setting up Eclipse as the IDE

This is another baby step on how one can learn about Sphinx 4. As I mentioned in the previous [post](http://grandjanitor.blogspot.com/2012/12/sphinx4-from-c-background-installation.html), it is nicer to use an IDE when you use Java code. Since I have some exposure in Eclipse, I choose it as an example on how to setup a Sphinx 4 build.

Before I go on there were many posts, written by others, discuss the procedure. You may take a look of them as well.

- [Getting Start with Sphinx4](http://srwoes.smargav.com/2009/04/getting-started-with-sphinx4-and.html) from "Speech Recognition Woe" written by "Amit S"
- [Setting up Development Environment](http://cmusphinx.sourceforge.net/2012/05/setting-up-development-environment/) from CMUSphinx Blog written by GSOCer. (If you know who write it, let me know so I can properly credit)

You will also need to know how to install JSAPI ([link](http://cmusphinx.sourceforge.net/sphinx4/doc/jsapi_setup.html)). It is crucial to get the compilation right. 

### Eclipse as a Development Environment

If you never use Eclipse before, it is a little bit like a more versatile version of Emacs. It's major use is on Java but lately there are more and more people use it as IDE for C/C++ as well. Not to say there are more different development packages for different programming languages. 

If you come from background such as emacs/vi development, one thing you need to know is that shortcuts are quite different from your current platform. That takes some time to adapt to but generally I think the advantage worth the cost.

Another thing you might want to be mentally prepare, Eclipse's Java compilation doesn't generate build log. Instead it will generate a list of errors in compilation. They are basically equivalent thing. Though, if you are used to Visual C++ type of IDE with an error log, you won't get what you want. 

To me, those are minor nuisances, using Eclipse to browse code has the extra advantage of readily-made documentation as well as a flatten structure. Those features will save you many keystrokes if compared to using vanilla emacs. 

In my description, I am using Eclipse Juno. Hopefully it won't change too much by the time you are compiling the code. Of course, if there is popular demand, I might write another post which describe later version of Eclipse as well.

### The compilation in High Level

Building Sphinx 4 essentially means the following four tasks:

1. Downloading Sphinx4 source code
2. Install JSAPI.
3. Incorporate the proper libraries.
4. Do the build.

In my case, I slightly stumbled on 1, naturally, just like you, I was thinking "well, why JSAPI something separate from the codebase?" Of course, if you worked in Java before, there are many projects required you to build with external codebase. So I don't think too bad. 

So let me go through the procedure of the build. 

**Downloading Sphinx4 source code from Subclipse**

- A plain simple svn command is fine, downloading the tarball will give you a more stable version. I will suggest a more attractive option is to use SVN module of Eclipse, subclipse. To do that, you may want to follow "Downloading Subclipse" from [Setting up Development Environment](http://cmusphinx.sourceforge.net/2012/05/setting-up-development-environment/) . (Notice that there was a typo in the post should be "tigris" instead "trigris" on the location field.)
- Once you finished checking out Subclipse. Start a new Project

    - **New -&gt; Project -&gt; SVN -&gt; Checkout Projects from SVN**

- Choose "**Create a New Repository Location"**

    - Type **[https://cmusphinx.svn.sourceforge.net/svnroot/cmusphinx](https://cmusphinx.svn.sourceforge.net/svnroot/cmusphinx/trunk/sphinx4)**

- Remember to only download trunk/sphinx4 (Note: there are many branches and location, for starter, you will be interested how the trunk look like.)

Once you check out the code, in your Package Explorer (Alt-Shift-Q -&gt; P) will look like this. 

![PackageExplorerSphinx4Compilation.png](http://1.bp.blogspot.com/-w08BuE_6cD4/UN4mk5MIPtI/AAAAAAAACh4/_G0boEP_Vq4/s640/PackageExplorerSphinx4Compilation.png)

Package Explorer View after code is check out from SVN

Now you might notice that there is a red question mark besides the sphinx4 project (I named it "sphinx4_grandjanitor" but you can name it whatever you want.) You might also notice that in your Problem screen, there are 2 errors :

![ProblemsSphinx4Compilation.png](http://4.bp.blogspot.com/-0cKmqwN0Bn0/UN4noD6PS4I/AAAAAAAACiE/xtKZuD2LkQg/s400/ProblemsSphinx4Compilation.png)

Now this is really because lib/jsapi.jar wasn't installed correctly. So the next step is to install jsapi.jar

**Install JSAPI**  
**  
**I tried the install of both Windows Vista and Linux. In windows, go to sphinx4lib and type

**&gt; jsapi.exe**  
**  
**Then accept the license.

In Linux, in the same directory. do

&gt; **sh jsapi.sh**  
**  
**One common problem for Linux here: you need to install uudecode if you want to install jsapi. In that case, try to install sharutil. On Ubuntu, it works for me when I do

&gt; **apt-get install sharutil**   
**  
**At this point you should see your directory should have a file named jsapi.jar

**Incorporate the proper libraries**  
**  
**This is another part which took me a while. Before you go on to configure your path, you need to do one more step to make to configure libraries. In Eclipse, right click you Sphinx4/lib directory and choose **Refresh** first. This will make jsapi.jar appears your Package Explorer. It should look like this:

| ![correct_version_of_package_explorer.png](http://1.bp.blogspot.com/-44D443U_YG4/UN4qLykBvFI/AAAAAAAACiY/MBB9ShpWhNs/s1600/correct_version_of_package_explorer.png) |
| --- |
| When JSAPI.jar is properly installed |

Then, you can change the build path, go to your project again, right click and choose **Build Path -&gt; Configure Build, Libraries,** choose **Add Jar,** then add the libraries you need.

**Now.... wait, what are the jar files we need again?**  
**  
**Yeah, so this is another place which can cause confusions. In fact, because Sphinx has expanded its code from time to time, so the answer of which jar files to add depends. As of Dec 28, 2012, you should add

- junit
- jsapi
- js
- fst

This list will likely to grow in future. I am also pretty sure you might need to do different things if you want to compile in a different setting or write your own code.

**Do the build**  
**  
**In modern Eclipse, building should be automatic, what you should see should be 0 errors but many warnings. I generally don't approve of warnings but as a developer, it's pretty tough to eliminate them all.

### Conclusion

There you have it, a little guide on Sphinx 4 compilation with Eclipse. Notice that this guide may or may not fit your purpose because I focus on downloading the code from Subclipse. Doing a **Link Source** should do the trick if you want to incorporate the code yourself. I might do another post later but the web has many articles described this already, you should be able to find a set of good instructions. 

Arthur

Related Posts: 

[Sphinx4 from a C background : first few steps](http://grandjanitor.blogspot.com/2012/12/sphinx4-from-c-background-first-few.html)

[Sphinx4 from a C background : Installation of Eclipse](http://grandjanitor.blogspot.com/2012/12/sphinx4-from-c-background-installation.html)

**  
**

**  
****  
**

---

## Comments

**三十三博** (2012-12-30):

You are welcomed, Mr. Anonymous.

If there is any topic you are interested, feel free to suggest here as well.

**602e03f4-2327-11e2-8544-000bcdcb8a73** (2012-12-29):

Thanks!

