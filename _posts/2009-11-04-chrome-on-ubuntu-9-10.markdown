---
author: sayakbiswas
comments: true
date: 2009-11-04 07:09:39+00:00
layout: post
slug: chrome-on-ubuntu-9-10
title: "Chrome on Ubuntu 9.10"
wordpress_id: 121
category: blog
tag:
- '9.10'
- chromium
- install
- karmic
- koala
- linux
- Ubuntu
blog: true
---

In my previous post, I gave a how-to of installing Chromium browser(development version of Google Chrome) on Arch Linux. In this post I'll show you how to install Chromium on Ubuntu 9.10(Karmic Koala).

1. Go to System->Administration->Software Sources. Go to tab "Other Software".

2. Click Add. In 'APT Line' paste the following:

		deb http://ppa.launchpad.net/chromium-daily/ppa/ubuntu karmic main

   Click Add again and paste the following:

		deb-src http://ppa.launchpad.net/chromium-daily/ppa/ubuntu karmic main

   Click Close and Reload.

3. In a terminal paste the following:

		sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 0xfbef0d696de1c72ba5a835fe5a9bf3bb4e5e17b5 && sudo apt-get update

4. Install chromium using the following command:

		sudo apt-get install chromium-browser

That's it. You're done.
I've also made a screen-cast of the procedure. Yay! My first youtube video. :D

[![Chrome on Ubuntu](http://img.youtube.com/vi/GK86JZzIaMw/0.jpg)](http://www.youtube.com/watch?v=GK86JZzIaMw)
