---
author: sayakbiswas
comments: true
date: 2016-01-15 00:47:42+00:00
layout: post
slug: install-spotify-in-fedora-23
title: "Install Spotify in Fedora 23"
wordpress_id: 493
category: blog
tag:
- Fedora
- spotify
- linux
blog: true
---

I have had an interest in Spotify ever since it launched but never got to try out as it is not available in India. So, I never understood what the buzz was all about. But, I recently moved to US to start Grad School at University of Florida. So, finally I was able to try out Spotify for myself and I must say it is really impressive. It lets me discover a bunch of new music so easily. I find myself listening mostly to the pre-prepared playlists by Spotify like the Power Ballads, Evening Acoustic playlist etc. I quickly installed Spotify in Windows and proceeded to install it on my Fedora 23 setup. Below are the steps:

  1. Add the negativo17 repo for spotify.

			sudo dnf config-manager --add-repo=http://negativo17.org/repos/fedora-spotify.repo

  2. Install Spotify by running

			sudo dnf install spotify-client

Aaaaanddd....you are done. Launch and enjoy!

Until next time!
