---
author: sayakbiswas
comments: true
date: 2013-10-27 18:50:21+00:00
layout: post
slug: fix-hybrid-graphics-high-power-consumption-and-overheating
title: "Fix Hybrid Graphics high power consumption and overheating"
wordpress_id: 207
category: blog
tag:
- Ubuntu
- Hybrid Graphics
blog: true
---

**<span class="emphasize">[UPDATE]: Ubuntu now supports ATi + Intel hybrid graphics systems in the 13.10 and 12.04.03.</span> Here's how to make it work:**

Make sure any other fglrx driver is not installed. Install fglrx and fglrx-pxpress as follows:

		sudo apt-get install fglrx fglrx-pxpress

If you have added the lines in `/etc/rc.local` as in the previous solution, please remove them and reboot the system.

In my machine the AMD/Intel setup is working fine. There is no high power consumption and overheating of the system. Also, I am able to switch between the cards effortlessly through Catalyst Control Center. Thanks Ubuntu/AMD!

In systems with ATi + Intel hybrid graphics running *Ubuntu 13.04 and 13.10 distros, I have noticed high CPU usage and overheating resulting in very high power consumption and low battery backup.

For people facing the issue, this can be solved by adding the following lines in the `/etc/rc.local` file:

```
sudo chmod -R 705 /sys/kernel/debug
sudo chown -R username:username /sys/kernel/debug/vgaswitcheroo
sudo echo OFF > /sys/kernel/debug/vgaswitcheroo/switch
```

Replace `username` in the second command with your username.

After this run: `sudo update-grub` and reboot your system.

This is a temporary fix as here we disable the discrete AMD card and just keep the onboard Intel card switched on.
