---
author: sayakbiswas
comments: true
date: 2015-11-28 14:15:04+00:00
excerpt: Read my experience of using the new Fedora 23 Workstation release with GNOME over the past couple of weeks.
layout: post
slug: fedora-23-workstation
title: "Fedora 23 Workstation"
image: /assets/images/post-images/23-release-945x400.jpg
headerImage: true
wordpress_id: 271
category: blog
tag:
- Fedora
- Fedora 23
- Fedora Workstation
- Review
- Fedora 23 Workstation Review
blog: true
---

What!? Two posts in a single day! That has (almost) never happened! Yes, in keeping with my promise in the previous post, here's my thoughts on the **<span class="emphasize">new Fedora 23 Workstation release</span>**.

Fedora was the **<span class="emphasize">first Linux distribution</span>** that I ever used; Fedora 7 it was, I believe. I was in the first year of college and one of our CS profs asked us to put Fedora in our new college provided HP Laptops(on which we had already installed Windows XP, of course). The image was hosted on the college network. I downloaded it, went back home and got to work installing it, excited to find something new. Of course, at that point of time I didn't know anything about installing Operating Systems outside of Windows XP. So, over the course of the installation procedure, I was appalled to find out that fedora had blown my XP partition to kingdom come along with all the data I had. The whole fiasco was my fault, of course, but I couldn't help cursing at the Fedora developers. After that I was using **<span class="emphasize">Ubuntu for a long time</span>** (started with 7.10 if i remember correctly) and then **<span class="emphasize">I moved on to openSUSE</span>** making pit stops at Arch Linux and some Fedora versions along the way. Actually before installing Fedora 23, I was using openSUSE 13.2 and had upgraded to openSUSE Leap with KDE Plasma 5. But **<span class="emphasize">Plasma 5 is not yet at the stage</span>** that I want it to be and I suffered quite a few glitches, crashes and annoyances. So I started looking for a GNOME distro, which led me to Fedora 23 Workstation. Okay enough rambling, lets get this beast of a review/impressions started.

A disclaimer before I start – this is not going to be a review or how-to in the traditional sense. I am just going to document my experience of using F23 over the past few weeks; things that nagged me and things that I liked. I downloaded the Fedora 23 Workstation 64-bit image via torrent and proceeded to install it on my **<span class="emphasize">Acer Aspire V5-573G</span>**.

Fedora 23 uses a (GTK3 based?) **<span class="emphasize">Anaconda</span>** as its installer. It is a very good looking setup program and differentiates itself from other OS installers by being **<span class="emphasize">non-linear</span>** in nature. By non-linear I mean that once you launch the installer, it throws you into a screen which can be basically considered a hub. From this screen you can launch other screens for changing your keyboard setup, setting up time zone, creating a user and setting up your partitions. You can do all this in any order you like. While I didn't have any problems with this, I can understand how new users might find this a bit wary. Something like Ubuntu's installer which takes you through all the same screens one after the other is likely to be much more conducive to the people new to Linux. But then again, both the distributions seems to have very different target audiences. While Ubuntu is almost universally agreed to be the newbie distro, Fedora with its Workstation version over the past few releases has been **<span class="emphasize">targeting the developer user base</span>**. The only complaint I have with the install process is with regards to the **<span class="emphasize">partitioner</span>**, which seems plain **<span class="emphasize">confusing</span>** at times. Case in point: Before installing Fedora, I had a dual-boot setup comprising Windows 10 and openSUSE Leap 42.1 installed with the BtrFS for the root directory and a /data directory where I had mounted my NTFS data partition to be shared between Windows and Linux distros. Now anaconda showed me all my openSUSE partitions grouped together under the banner “openSUSE”. Under this group also listed was my /data partition and this data partition was listed again under the “Windows”(or “other”?) group. Since I had decided to replace openSUSE with Fedora, I deleted all the openSUSE partitions and created / and swap partitions for Fedora. But I was stumped for a few moments as I couldn't decide what I should do with the /data that was still showing under openSUSE. If I deleted it, would it just remove the mount point or delete the entire partition? If I kept it, would I be left with some remnant of openSUSE in the installation e.g. the GRUB menu or somewhere else? I realized that would not be the case, since I was removing the entire openSUSE partition and GRUB wouldn't find it when it scans for installed operating systems. The installation went smooth after that and sure enough, I didn't find any remnants of openSUSE. The point is I realized this but new users may not. They might get confused and end up deleting their data and whatnot. What could be done to improve this is to group only the OS related partitions(say the / and /home partitions) under the OS-name banner and keep other custom created partitions separate. One other thing that might add to the usability of the partitioner is if they can provide a **<span class="emphasize">graphical display of the partition structure</span>** like Ubuntu and openSUSE do. That will definitely add to the feedback process from the system to the user regarding their actions.

After the installation process completed, I rebooted my PC and was greeted with a black and white GRUB screen. The fedora GRUB correctly detects my Windows installation to be Windows 10 and titles it as such unlike openSUSE which thought it was Windows 8. A very minor observation but very important to the usability perspective nonetheless. Fedora 23 comes with **<span class="emphasize">GNOME 3.18</span>** which is the latest and greatest GNOME release. I had been a GNOME user when I started using Linux, then moved to openSUSE/Arch Linux + KDE 4 when GNOME started shipping on GNOME Shell and Ubuntu started shipping Unity. Back then I found GNOME Shell to be too unstable and feature-less and Unity, well frankly, I found Unity to be boring. So, coming back to GNOME after all these years, I am pleased to say that **<span class="emphasize">I love it.</span>** It is stable and properly usable out of the box, although I did add a few extensions. I never completely understood the what Activities were meant for in KDE4, but I should say I really like the Activities workflow in GNOME probably because the entire shell is based around it instead of just being an extra. You press the Super(Windows logo) key(or you could just click on the top left corner where it says Activities)to land into the **<span class="emphasize">Activities overview screen</span>** to get an OS X Expose like view of all your active windows.

![Screenshot from 2015-11-28 13-04-14.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-13-04-14.png)

Here you can start typing to search for an application you wish to launch and you are presented with a filtered list of installed application. Also, if the application is not installed you are presented with matching applications from the repositories, clicking on which will open GNOME Software allowing you to install it. **<span class="emphasize">NEAT</span>**! The whole process feels very intuitive, slick and snappy aided in no small part by the fluid animations of Windows moving about, search results popping up and the like. There is also the Edge Tiling feature popularized by Windows 7. I guess it is now a part of all major Desktop Environments. One gripe I have about the GNOME UI is that there is **<span class="emphasize">no Minimize button</span>** by default. Looks like they never added it back once they removed it back in the early days of GNOME Shell. I agree that since there is no taskbar, it is now of little use. But seeing as all other environments and OS's have this feature, they should keep it even if it just pushes the current backward into the stack. See, I still use Windows very frequently, as do a lot of other users I'd wager. Coming from there and booting up GNOME, I find myself moving my mouse to the top right and finding no Minimize button. I find this a bit jarring. Not having a maximize button is okay with me as I can maximize windows by double clicking the title bar and this is how I do it in other environments as well. Of course, it can be easily fixed by using the bloody brilliant GNOME Tweak Tool.

Fedora comes with the usual repertoire of LibreOffice, Evolution, Videos, Rhythmbox, Shotwell etc. that you find installed by default in a myriad of other distributions.

![Screenshot from 2015-11-28 12-47-57.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-12-47-57.png)

The first thing I did after booting into Fedora was install the **<span class="emphasize">GNOME Tweak Tool.</span>** I don't understand why this is not installed by default. This application allows you to install gnome extensions, apply new themes and some general tweaks(like adding a minimize button!) with simple clicks. This is useful for beginners and power users alike and every GNOME distribution should ship this by default.

![Screenshot from 2015-11-28 13-22-13.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-13-22-13.png)

Also I installed **<span class="emphasize">Fedy</span>** from **[here](http://folkswithhats.org/)**, a really nice post-install tool which makes installing non-free codecs, microsoft fonts, google chrome, steam etc. a simple one-click affair. **<span class="emphasize">Cool stuff!</span>**

![Screenshot from 2015-11-28 13-24-32.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-13-24-32.png)

And now, a list of miscellaneous tweaks, additions, deletions, observations, likes and dislikes that I made from my usage.




  * I removed Rhythmbox and installed **<span class="emphasize">GNOME Music</span>** in its stead. Somehow, I feel Rhythmbox doesn't really gel well with the GTK3 look and feel and GNOME Music was enough to cater to my Music listening needs.


  * I removed Shotwell and installed **<span class="emphasize">GNOME Photos</span>**. I will concede that I did just to get the complete GNOME feel :P


  * I installed Bumblebee along with the proprietary NVIDIA drivers from [here.](https://fedoraproject.org/wiki/Bumblebee) I did run into an issue where I installed just the 64-bit bumblebee libraries and Steam was refusing to start. It turns out Steam needs the 32-bit libraries to work. So, I installed the multilib bumblebee stuff and it got fixed.


  * Installed the **<span class="emphasize">Inconsolata</span>** and PT fonts.


  * Also installed **<span class="emphasize">GNOME Todo, Calendar, Transmission and Builder</span>**.


  * Installed the below extensions from extensions.gnome.org


    * **<span class="emphasize">Messaging Menu</span>**


    * **<span class="emphasize">Chat Status</span>**


    * **<span class="emphasize">Removable Drive Menu</span>** – make life so much easier if you are switching between external drives


    * **<span class="emphasize">Media Player Indicator</span>** – A must have extension for me.![Screenshot from 2015-11-28 13-51-22.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-13-51-22.png)


    * **<span class="emphasize">User Themes</span>** – Need this to install new GNOME-Shell themes.


    * **<span class="emphasize">Battery Percentage</span>**





  * As I mentioned earlier, I use a **<span class="emphasize">DATA partition</span>** to share stuff like Music, Videos and Pictures between Linux and Windows. So, usually I automount my data partition at boot-up on to a folder called /data with rw options. Then I would create symlinks of the folders from the /data location to my home folder. Previously, I used to edit the /etc/fstab file to accomplish this. This time I used GNOME Disks to do the same. ![Screenshot from 2015-11-28 13-55-39.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-13-55-39.png)So basically, you open Disks select your partition, click on the gears icon, click Edit Mount options and you will be presented with the above screen.


    * Switch off Automatic Mount Options, check the Mount at Startup and Show in User Interface boxes.


    * Add the options

			uid=<your user id>, gid=<your group id>

	  You can get the ids by running

			cat /etc/passwd | grep <your username>

	  I would love to be able to get this information somewhere from the GUI, say the Users section in the Settings app.

    * Change the default mount point to whichever directory you want to mount your partition, /data for me.


    * Click OK and you are good to go.


    * Then I created symlinks from /data partition to my home directory by running commands similar to:

			ln -s /data/Documents /home/sayak

	  Dolphin has this feature where if I right-click drag a folder to another directory, it asks me if I want to create a link. I would like to see something similar implemented in Nautilus as well.

  * Suspend and Resume seemed to work just fine. But I couldn't find any option to put my system into **<span class="emphasize">Hibernate mode</span>**. If anybody knows how to do it, I would really love to know.

  * I was pleased to find that Videos now has the option to enable a plugin which allows you to download subtitles from the app itself. This is one feature that makes SMPlayer(on Linux) and PotPlayer(on Windows) my favourite video playback applications.

  * Another gripe regarding the GNOME's UI design. It seems that as part of GNOME 3.16, the developers overhauled the **<span class="emphasize">file copy dialog</span>**. Now when you're copying a file you get a tiny circle at the top right section of Nautilus' header bar. This circle fills up with black as the copy operation progresses.
![Screenshot from 2015-11-28 16-07-00.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-16-07-00.png)
If you click on the circle, you get more details as in the shot below.
![Screenshot from 2015-11-28 16-07-05.png](http://sayakbiswas.github.io/assets/images/post-images/screenshot-from-2015-11-28-16-07-05.png)
This looks pretty sexy if you are working in Nautilus all the while the file is copying. But if you are working on a different application during this operation you would have no way of knowing the progress other than alt-tabbing back to Nautilus. This has been talked about before by others as well and the solution seems to be taking this dialog off of Nautilus and placing it in the top right System Status menu, similar to KDE and Unity. This will make sure that the progress notification is always visible to the users.

  * A new feature that arrived with GNOME 3.18 and one that I like quite a bit is the **<span class="emphasize">Google Drive integration.</span>** So, if you've added your Google account via the Online Account configuration section in the Settings Panel, you will find that the file manager now has a section with your gmail ID and a network icon on the left side. Click on it and you can access all your google drive stuff from here.

  * One thing that is missing and is useful for laptops is auto-brightness dimming when you lose power and you system is running on battery. On that note, I have also installed “**<span class="emphasize">tlp</span>**” which has been known to improve battery life on laptops. With tlp installed, my laptop gave me a run time of almost 5 hours on battery. It included watching an hour long episode of Doctor Who and listening to music on speakers while writing this review. Heck, I had even booted up my CentOS VM for a few minutes.

  * While on the topic of VM's, I would like to say that **<span class="emphasize">Boxes</span>** is a potentially great tool. Although it needs some more polishing to become something I can recommend without any reservation. I have set up two Virtual Machines using Boxes, one for openSUSE Leap and other for CentOS 7. The setup was a breeze especially the one for CentOS 7. As soon as I selected the CentOS 7 iso, Boxes gave me the option to set up a preconfigured VM, asking me just for the username and password I would like to use. Once I provided those details, Boxes started the install procedure automatically. Next thing I knew there was a notification at the top of my screen saying CentOS box is ready to use. It didn't ask me for anything else. I was like – WOW! May be this is something to do with the Fedora and CentOS relationship. I would definitely like to see similar features for setting up other, at least major, systems like openSUSE, Mint, Ubuntu and Debian. But everything was not peaches while using Boxes, there were times when I would launch Boxes and it would not show any of my two VM's. I would need to relaunch the application for the VM's to show up. Also, if I select an ISO from my NTFS drive for setting up a VM, the application fails and shows the error: “Box Creation Failed”. Wonder what's going on there.

  * Another complaint relates to the update management. This is handled by **<span class="emphasize">GNOME Software's Update</span>** module. Most of the time Software doesn't show any available updates even if I manually hit the Check for Updates button. But then I go and do a

			sudo dnf update

	in the terminal or check for updates in Yumex, and I can see a whole bunch of software updates just waiting to be installed. I am not sure if there is some filter in Software that strips out some updates from the result list or something else is at work here, but it sure is weird.

  * **<span class="emphasize">Touchpad Issues</span>** – My laptop came with an Elantech touchpad. When I installed and booted Fedora for the first time the touchpad was very jumpy, to the point that I was unable to properly close any window. I just couldn't aim for the X button. I didn't run into this issue in openSUSE Leap KDE. It could be a regression in the new 4.2 kernel series, though that's just me speculating. I searched for this issue in google and came across the below fix in [Ask Fedora](https://ask.fedoraproject.org/en/question/69254/fedora-22-touchpad-cursor-slags-and-jumps/).

		su
		dnf install xorg-x11-drv-synaptics
		cd /usr/share/X11/xorg.conf.d/
		ln -s 50-synaptics.conf 99-synaptics.conf
		reboot

Also, tap to click doesn't work in the log in screen. If anybody knows a solution to this problem, please feel free to let me know.

In conclusion, I will say that Fedora 23 Workstation has been working really well for me. This is probably the most polished Fedora release I have ever used. Looks like their approach of focusing on three core products is working out quite well for them. I am **<span class="emphasize">really satisfied</span>** with this. The only thing I miss from openSUSE is the YaST control center. Oh Well! Maybe I should give Leap with GNOME a try.

Until next time!
