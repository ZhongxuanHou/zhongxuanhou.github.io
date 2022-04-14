---
author: sayakbiswas
comments: true
date: 2013-10-27 19:14:02+00:00
layout: post
slug: fix-for-brightness-issue-in-ubuntu-13-10
title: "Fix for brightness issue in Ubuntu 13.10"
wordpress_id: 219
category: blog
tag:
- brightness
- brightness fix
- brightness issue
- fix
- kubuntu
- kubuntu 13.10
- Ubuntu
- ubuntu 13.10
blog: true
---

In Ubuntu 13.10, I found that I was unable to change the brightness either by using the brightness keys or moving the brightness slider in System Settings. To fix the issue, I had to change the file `/etc/default/grub` to reflect the following:

		GRUB_CMDLINE_LINUX=""

to

		GRUB_CMDLINE_LINUX="quiet splash acpi_osi=Linux acpi_backlight=vendor"
