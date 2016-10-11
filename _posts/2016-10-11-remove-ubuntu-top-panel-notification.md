---
layout: post
title: "Remove notification from Ubuntu top panel"
date: 2016-10-11 22:50:15 +0100
categories: ubuntu unity panel
---

Just the other day, I ran into this issue where I had a printer notification showing up
in the Unity top panel of my Ubuntu 14.04 workstation. I had already got rid of any printers
on my system, hence I couldn't get rid of this notification. If I clicked on the notification
it opened up the printer queue window which had an empty queue.

A search on the web led me to a couple of articles that helped me get rid of it. One of them was
[this answer on askubuntu.com](http://askubuntu.com/questions/152380/how-can-i-remove-the-default-indicators-and-add-custom-ones).
So here's the 2 steps that finally got rid of it.

1. `sudo apt-get remove indicator-printers`
2. `sudo killall unity-panel-service`
