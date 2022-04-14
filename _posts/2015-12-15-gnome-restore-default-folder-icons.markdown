---
author: sayakbiswas
comments: true
date: 2015-12-15 13:22:28+00:00
layout: post
slug: gnome-restore-default-folder-icons
title: "GNOME - Restore default folder icons"
wordpress_id: 468
category: blog
tag:
- default icons
- GNOME 3
- Issue
- Fix
blog: true
---

Recently, my laptop battery got drained completely and the system shut down incorrectly. This resulted in my NTFS data drive not getting unmounted properly. The videos, music, pictures and documents folders in my NTFS drive are linked to the Home folder in my Fedora install. When I booted my system back up I was not able to access my music and videos. I figured, probably some issue with auto-mounting the NTFS drive at boot, so unmounted and remounted the drive and the issue was fixed. I rebooted once more to confirm and the auto-mounting was working. I had access to my music and videos again. But there was a different issue.

You know how the Documents, Music, Pictures and Videos folders all have specialized icons? Well, they were gone and were replaced with a generic folder icon. After looking around for some time, I got to the root cause. It turns out that my `/home/sayak/.config/user-dirs.dirs` had got corrupted. This is how the file is supposed to look like:

~~~
# This file is written by xdg-user-dirs-update
# If you want to change or add directories, just edit the line you're
# interested in. All local changes will be retained on the next run
# Format is XDG_xxx_DIR="$HOME/yyy", where yyy is a shell-escaped
# homedir-relative path, or XDG_xxx_DIR="/yyy", where /yyy is an
# absolute path. No other format is supported.
#
XDG_DESKTOP_DIR="$HOME/Desktop"
XDG_DOWNLOAD_DIR="$HOME/Downloads"
XDG_TEMPLATES_DIR="$HOME/Templates"
XDG_PUBLICSHARE_DIR="$HOME/Public"
XDG_DOCUMENTS_DIR="$HOME/Documents"
XDG_MUSIC_DIR="$HOME/Music"
XDG_PICTURES_DIR="$HOME/Pictures"
XDG_VIDEOS_DIR="$HOME/Videos"
~~~

In my case, the documents, music etc. directories were pointing to $HOME i.e. XDG_DOCUMENTS_DIR="$HOME/". Most likely, a result of the botched auto-mounting attempt from earlier.

To fix it, I just had to update the file to point to the correct locations. So, I deleted the file and executed the below command:

		xdg-user-dirs-update

And, that fixed it.
