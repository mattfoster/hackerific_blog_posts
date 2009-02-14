Title: Graphing version control system changes
Category: scripting
Tags: ruby,script,cvs,svn,svk,graphing


Version control is a big part of my, (and many other peoples') workflow. I'm a big fan of [svk](http://svk.bestpractical.com/) and I regularly use [svn](http://svn.tigris.org) for projects I'm working on, and, perhaps most importantly, the code and docs comprising my PhD to date.

✂------✂------✂------✂------✂------✂------✂------✂------✂------✂------

In a few months, when I start writing my thesis, I want a way to track my progress from the very beginning. That's why last week I started tinkering on a ruby script to plot the total number of lines in my SVK repository, and plot the results in a graph. This post describes how I went about scripting a solution.

First of all, I decided on the following requirements:
* Create a graph of total lines, and the net number of changes (lines deleted/inserted) over the history of the repository. 
* The graph should be an anti-aliased PNG, ready for the web. 
* The script should integrate with svn/svk using a post-commit hook.

I didn't want to have to rely on anything too esoteric, but I was happy to use any rubygems I needed, as well as [gnuplot](http://www.gnuplot.info/) to draw the graph if needed. 
I also ended up coding a graph drawing function with gruff, which I made the default.

