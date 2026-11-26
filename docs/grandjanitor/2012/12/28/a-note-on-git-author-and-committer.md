---
title: "A note on GIT author and committer"
date: 2012-12-28
categories: ["cvs", "git", "git-commit", "git-log", "git-push", "svn"]
---

# A note on GIT author and committer

I considered GIT as a great improvement over CVS and SVN. SVN is okay if the codebase is not too large because SVN server sometimes get into lockup mode.

One thing I like about GIT is the differentiation between author and committer. The author is the original writer of the code. The committer would be the one who commits the code. This makes ownership and responsibility clearer. 

(Some houses discourage to look at who commit a change and demand programmers to take care of the problems themselves. My one comment: mental constipation.)

So if you want to change the author of a commit. Do

&gt;** git commit -m "Your message" --author "Firstname Lastname " yourfile.java**

In GIT commit, you will see "Firstname Lastname" become the author, to look at the original committers, use 

&gt;**git log --pretty=full ./yourfile.java**

An obviously, this information can be push to a remote repository. Simple

&gt;**git push** 

should work. 

Arthur
