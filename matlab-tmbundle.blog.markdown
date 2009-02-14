Type: Blog Post (Markdown)
Blog: my-mili.eu
Link: http://blog.my-mili.eu/articles/2008/05/09/meet-the-new-matlab-bundle-moderator
Post: 14
Title: Meet the New Matlab Bundle Moderator
Format: markdown
Date: 2008-05-09 15:16:06 +0100
Pings: On
Comments: On

I've taken over maintainership of the TextMate Matlab bundle as of last week, after what seems to have been quite a long period without a maintainer. Hopefully, I can fix a few of the glitches (hopefully I already have), and I've got plans to add various bits of useful functionality.

My current todo list includes:
  
  * Updating the snippets to reflect TextMate conventions (work in progress).
  * Adding more snippets for useful functions to help speed up writing code.
  * Improving the language grammar.
  * Making sure that Octave remains properly supported.
  * Adding snippets to aid in writing octave-specific functions.
  * In addition, I'd love to find out how to better integrate TextMate with Matlab / Octave.

I'm ready to accept suggestions and patches from anyone who's interested in helping to make this bundle as good as some of the others!

If you don't have the bundle yet, grab it from subversion:
export LC_CTYPE=en_US.UTF-8
mkdir -p ~/Library/Application Support/TextMate/Bundles
cd ~/Library/Application Support/TextMate/Bundles
svn co http://macromates.com/svn/Bundles/trunk/Bundles/Matlab.tmbundle

If you make any useful changes, follow the instructions on the 
[TextMate wiki](http://wiki.macromates.com/Bundles/HowToContribute), and send them to me!
