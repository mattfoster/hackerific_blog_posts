Type: Blog Post (Markdown)
Blog: my-mili.eu
Link: http://blog.my-mili.eu/articles/2007/10/26/making-vnc-work-properly-over-ssh
Post: 6
Title: Making VNC work properly, over SSH
Keywords: 
Format: none
Date: 2007-10-26 09:18:57 +0100
Pings: On
Comments: On

Today I tried to connect to my machine using VNC on my Mac, using the bizarrely named [Chicken of the VNV](http://www.apple.com/downloads/macosx/networking_security/chickenofthevnc.html). All I got was a fairly large black window.

You see, yesterday, when I enabled the VNC server in the gnome control centre, I forgot to uncheck the option which controls whether to pop up a message, on the _server_, asking whether the VNC connection can continue.

I think it's a tad silly enabling this by default -- how many people do you think use VNC to their desktop whilst they're sat at it? But I can understand GNOME erring on the side of caution, and perhaps assuming user stupidity (as ever, [perhaps](http://www.desktoplinux.com/news/NS8745257437.html)?).

Luckily I have SSH access, so I was fairly sure I could fix it. Here's how I did:

`gconftool-2 -s -t bool /desktop/gnome/remote_access/prompt_enabled false`

That's it! If remote access was disabled, I could also have remotely enabled that with: 

`gconftool-2 -s -t bool /desktop/gnome/remote_access/enabled true`

Have you got any useful `gconftool` tips? Please leave a comment.
