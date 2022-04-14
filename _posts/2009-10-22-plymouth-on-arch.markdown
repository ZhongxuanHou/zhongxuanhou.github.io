---
author: sayakbiswas
comments: true
date: 2009-10-22 16:08:58+00:00
layout: post
slug: plymouth-on-arch
title: "Plymouth on Arch"
wordpress_id: 112
category: blog
tag:
- Arch
- linux
- Plymouth
blog: true
---

I'm now enjoying beautiful splashes at boot on my Arch box. Yes, plymouth works quite well on Arch. To get it working well, execute the folowing steps:

1. First get [KMS](http://wiki.archlinux.org/index.php?title=Special%3ASearch&search=KMS&go=Go) enabled in your kernel.

2. Next install plymouth-git from aur:

		yaourt -S plymouth-git

3. Then edit `/etc/mkinitcpio.conf` and add 'plymouth' (without the quotes) in the HOOKS line after base, udev and autodetect.

4. Rebuild initrd using(as root):

		mkinitcpio -p kernel26

5. To change themes, do:

		sudo plymouth-set-default-theme  --rebuild-initrd

   You can find themes in `/usr/share/plymouth/themes`.

6. Reboot

The only problem I have with this method is that `plymouthd` does not get stopped even after plymouth splash ends. For that I have to do (as root)

		killall plymouthd

everytime I login(not a very viable solution). So, if you guys have any better solution, feel free to tell me.

Cheers!
