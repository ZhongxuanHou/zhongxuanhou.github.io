---
author: sayakbiswas
comments: true
date: 2011-08-08 15:09:55+00:00
layout: post
slug: set-up-cc-environment-with-vim-mingw
title: "Set up C/C++ environment with vim & mingw"
wordpress_id: 204
category: blog
tag:
- Programming
- Windows
blog: true
---

For those who love writing code in vi/vim(let's face it its the greatest code editor in the world) and miss it while using Windows, it is possible to set up vim in Windows. Here are the steps to install and set up Vim with MinGW(gcc/g++).

1. Download and install gVim from [here](http://www.vim.org/download.php#pc).

2. Download MinGW automated installer from [here](http://sourceforge.net/projects/mingw/files/Automated%20MinGW%20Installer/mingw-get-inst/) and run the installer.

3. Select the package repository and the directory to install(default is C:\MinGW, I recommend leaving it as it is).

4. Select the optional components like C++, Fortran and MSYS base(this is useful; it provides the various bash shell tools like ls,grep,make,gawk etc).

5. The installer then downloads the latest version of the packages and installs them.

6. Finally, add MinGW's bin directory to the PATH environment variable.

7. To test if MinGW is set up correctly, go to the command prompt and type `g++ --version`. If you see the version number as output, then congratulations.

Hope, this post has been helpful.
