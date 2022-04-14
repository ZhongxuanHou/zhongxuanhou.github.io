---
author: sayakbiswas
comments: true
date: 2009-10-22 15:18:24+00:00
layout: post
slug: increased-boot-up-speed
title: "Increased Boot-Up Speed...."
wordpress_id: 99
category: blog
tag:
- Arch
- linux
blog: true
---

I found out a way to increase boot-up speed in Arch. Previously, I used to load the `network` daemon in `/etc/rc.conf` `Daemons` array. The `network` daemon used to take quite a bit of time to load and also sometimes fail killing splashy(giving a message: "Something failed, killing splashy") and falling back to text mode. But now I replaced the `network` daemon with `networkmanager` daemon and it works like a charm. Boot-up speed has increased and splashy does not crash anymore. It's great.

To manage network with networkmanager in KDE4, install `kdemod-networkmanager-git` and `kdemod-networkmanagement-knetworkmanager-kde4` and reboot. You'll see the `knetworkmanager` icon in the System Tray. That's it.

But one thing which I don't understand is why `network` daemon takes so much time to load and `networkmanager` lesser.
