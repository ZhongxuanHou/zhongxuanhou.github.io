---
author: sayakbiswas
comments: true
date: 2015-12-08 15:21:06+00:00
excerpt: Fix for screen tearing issues in Fedora 23
layout: post
slug: fedora-23-and-screen-tearing
title: "Fedora 23 and screen tearing"
wordpress_id: 422
category: blog
tag:
- Fedora
- Fedora 23
- fix
- Intel
- Issue
- Screen
- Screen Tearing
- Tearing
blog: true
---

As I mentioned in my Fedora 23 review, I am very happy with this new release. So, I was a bit disappointed when I notice the issue with screen tearing. Now this is probably an issue with my particular set up and a lot of people may not run into this issue.

I have an Acer Aspire V5 with an integrated Intel HD 4400 and nVidia GT 750M and I use bumblebee for dynamic switching. So, by default the system runs on the Intel card. I noticed that when I move any window there is some tear. Naturally, I went on google looking for a fix for the issue. And I found [this](https://ask.fedoraproject.org/en/question/79299/screen-tearing-and-low-fps-with-intel-hd-4400/) post on Ask Fedora. Basically the fix is to create the file `/etc/X11/xorg.conf.d/20-intel.conf` and have the below content in it:

		# /etc/X11/xorg.conf.d/20-intel.conf
		Section "Device"
		Identifier "Intel Graphics"
		Driver "intel"
		Option "AccelMethod" "sna"
		Option "TearFree" "true"
		EndSection

And then reboot! The issue should be fixed.
