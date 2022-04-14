---
author: sayakbiswas
comments: true
date: 2009-01-17 11:37:34+00:00
layout: post
slug: font-appearance-in-ubuntu
title: "Font Appearance in Ubuntu..."
wordpress_id: 84
category: blog
tag:
- linux
- Ubuntu
- fonts
- customization
- tips
blog: true
---

As I said in my previous post, fonts are the most coveted jewelerry to brace your desktop. So keeping it clear and beautiful is a must.

To get good fonts in Ubuntu(I feel the defaults suck quite a bit), you can install the `msttcorefonts` package. Make sure you have the universe repository enabled. Fire up the terminal and type the following:

		sudo apt-get install msttcorefonts

If you've got other fonts, installing them is as easy as copying the fonts files to the `~/.fonts` directory. If you don't find the directory, you can just create one.

After the installation, go to System-->Preferences-->Appearance. Select the Fonts tab. Select your favourite fonts for the different purposes from the dropdown lists(my favourite is Trebuchet MS) and set a good size(I have set mine to 8 ) so that they look clean and clear.

Now if you are using an LCD screen, you can make them look even better. Under the Fonts tab, select 'Subpixel smoothing(LCDs)' under Rendering. Then Click on Details. Select Resolution to be 96 dpi. Under Hinting, select 'Slight'. Close the windows and see the difference for yourself.
