---
title: "Start to look at the repository tree"
date: 2012-05-02
categories: ["Logios", "pocketsphinx", "Sphinx", "sphinx_fsttools"]
---

# Start to look at the repository tree

Programming as a profession is a a strange one. If you are a doctor, you can usually carry your knowledge and skills from one place to another provided that you have exactly the same tool. If you are a programmer, you speed and skill are partially determined by the tools you build in house for a particular place. So for example, I am not supposed to use any tool I built when I worked in the small video-advertising start-up. Even if I can do something in 1 second at that period of time, if I change my job, I will need to restart and rebuild the tool again. We are probably talking about days to rebuild the tool and weeks to refine it again.

There is one exception: if you worked in open source, much of your code would be stored in a public place. Even when you have left your job for long time, it is legit for you to use it again. You don't have to solve the same problem again and again. This is the beauty of open source and I am greatly benefited by it personally. 

As I start to regain my muscles in Sphinx, I start to notice that there are much changes in last 6 years. Just look at the top level of Subversion:

| [File](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/?sortdir=down#dirlist) ![up.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/up.png) | [Rev.](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/?sortby=rev#dirlist) | [Age](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/?sortby=date#dirlist) | [Author](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/?sortby=author#dirlist) | [Last log entry](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/?sortby=log#dirlist) |
| --- | --- | --- | --- | --- |
| ![back_small.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/back_small.png) Parent Directory |  |  |  |  |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) CLP/ | [**10079**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/CLP/?view=log) | 23 months | dhdfu | Finally add an -F argument to use the full path in the control file as the label… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) PocketSphinxAndroidDemo/ | [**11117**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/PocketSphinxAndroidDemo/?view=log) | 9 months | nshmyrev | Wrapper for nbest |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) SimpleLM/ | [**22**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/SimpleLM/?view=log) | 12 years | rickyhoughton | Initial revision |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) Speech-Recognizer-SPX/ | [**8933**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/Speech-Recognizer-SPX/?view=log) | 3 years | nshmyrev | Update module to recent pocketsphinx API |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) SphinxTrain/ | [**11350**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/SphinxTrain/?view=log) | 9 days | nshmyrev | Extract warped features during 000 stage if VTLN is enabled. See for details[ht](https://sourceforge.net/tracker/?func=detail&atid=301904&aid=3515214&group_id=1904)… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) archive_s3/ | [**7289**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/archive_s3/?view=log) | 4 years | egouvea | Fixed error message in decoder script reporting failure in bw, and made result d… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) cmuclmtk/ | [**11035**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/cmuclmtk/?view=log) | 10 months | nshmyrev | Fixes bug in wngram2idngram and adds a test for it |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) cmudict/ | [**11348**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/cmudict/?view=log) | 3 weeks | air | cleaned up documentation and code (a bit) recompiled the dict |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) gst-sphinx/ | [**7848**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/gst-sphinx/?view=log) | 4 years | dhdfu | Support changing language models at runtime (maybe) |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) htk2s3conv/ | [**11336**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/htk2s3conv/?view=log) | 6 weeks | nshmyrev | Adds warning about different number of mixtures |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) jsgfparser/ | [**7230**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/jsgfparser/?view=log) | 4 years | dhdfu | Fix the main program to output the only public rule if no rule is specified, and… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) logios/ | [**11339**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/logios/?view=log) | 4 weeks | tkharris | remove duplicated code |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) misc_scripts/ | [**10147**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/misc_scripts/?view=log) | 22 months | dhdfu | handle zero references |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) multisphinx/ | [**10945**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/multisphinx/?view=log) | 12 months | dhdfu | clean up better and introduce vocabulary maps |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) pocketsphinx/ | [**11351**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/pocketsphinx/?view=log) | 8 days | nshmyrev | Updated lat2dot script. I need to move it to the other location though |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) pocketsphinx-extra/ | [**9972**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/pocketsphinx-extra/?view=log) | 2 years | dhdfu | add sc models with mixture_weights and mdef.txt files |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) scons/ | [**5868**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/scons/?view=log) | 5 years | egouvea | updated the scons support to reflect that plugin.jar is now part of the package |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) share/ | [**5532**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/share/?view=log) | 6 years | egouvea | Setting dsp and dsw files to have have windows EOL regardless where it's downloa… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) sphinx2/ | [**8767**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/sphinx2/?view=log) | 3 years | egouvea | Updated the sphinx-2 MS files to MS .NET, consistent with the other packages, an… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) sphinx3/ | [**11329**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/sphinx3/?view=log) | 2 months | nshmyrev | Patch to solve memory issues in python module. See for details[https://bugzilla](https://bugzilla.redhat.com/show_bug.cgi?id=791280)… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) sphinx4/ | [**11344**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/sphinx4/?view=log) | 3 weeks | nshmyrev | Properly sets logger for AudioFileDataSource. Thanks to Bandele Ola. |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) sphinx_fsttools/ | [**10791**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/sphinx_fsttools/?view=log) | 14 months | nshmyrev | Some bit in AM to FST conversion |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) sphinxbase/ | [**11346**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/sphinxbase/?view=log) | 3 weeks | nshmyrev | Properly select buffer size when using audioresample. Thanks to balkce See fo… |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) tools/ | [**9009**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/tools/?view=log) | 3 years | nshmyrev | Updated to the latest release of sphinx4 |
| ![dir.png](http://cmusphinx.svn.sourceforge.net/viewvc-static/images/dir.png) web/ | [**10249**](http://cmusphinx.svn.sourceforge.net/viewvc/cmusphinx/trunk/web/?view=log) | 21 months | nshmyrev | There is no sphinx3 development anymore |

How exciting is that? You got only 6 to 7 top level directories 7 years ago!

From now on, I will start to put more notes on different tools in the repository. 

The Grand Janitor

---

## Comments

**Nickolay Shmyrev** (2012-12-15):

It's pretty much pollutted with the old things which nobody knows how to run.

I've cleaned up it recently, moved some really old things to branches and grouped others. It's a better now, but more cleanup to come later.

