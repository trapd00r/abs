Archlinux ABS Git
=================

This is a unofficial mirror of the Archlinux svn server.

Why
---------------

I maintain alot of my own packages and tracking changes 
using just abs was not enough and svn did not keep the 
same abs structrue.

How it works
---------------

Once a day I run git svn fetch and pull any changes into 
the svn branch.The svn branch contains the exact untouched 
archlinux svn it also containsthe same svn commit logs. 

I then rebase the svn branch into master. Master has been layed out to represent
abs. The layout only needed to be done once and rebasing takes care of the rest. 

Issues
--------------

If you have any issues with the master branch vs the svn branch . please post an
issue @ [Issues](http://github.com/str1ngs/abs/issues)

The master branch is still not stable enough to replace abs. However if you 
are in doubt you can use the svn branch it remains untouched. 

There are some problems when new packages are moved around in svn. Right now I have
a script that detrunks where needed but I think git can handle it alone if you are
git savy maybe you can take a look at it.

The mirror does not contain the full archlinux svn history its only contains
from revision 84267 on. I do not plan on pulling that history.

The svn commits are kinda cryptic. I need to dig deeper and find a better way to present them.

How to Contribute and use it
--------------

Contributing is very easy start by _watching_ the project on github. From there on you can
pull from this repo.  

All you have to do is clone git://github.com/str1ngs/abs.git . And where you would normally
use abs to sync. You just cd into the abs directory to pull. I also suggest you keep your
custom changes on another branch then git rebase the master branch when you want to update
your packages.  You could also pull origin master into your custom branch but you might 
have to use git pull --rebase. I have not tested it yet. 
