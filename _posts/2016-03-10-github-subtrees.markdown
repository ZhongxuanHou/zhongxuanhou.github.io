---
author: sayakbiswas
comments: true
date: 2016-03-10 15:51:50+00:00
excerpt: Use git subtrees to manage multiple projects under one repository
layout: post
slug: github-subtrees
title: "GitHub Subtrees"
wordpress_id: 525
category: blog
tag:
- git subtree
- GitHub
- subtree merge
- version
- Version Control
blog: true
---

I have been familiar with git ever since I started using Linux. I used 'git clone' quite a bit to compile and install latest versions of software, but that's where most of my 'familiarity' was limited to. I did mess around with creating local repositories and committing but that's all. We used SVN at work, so most of my version control knowledge is based on SVN. So, I am still figuring out lot of git stuff that most people probably already know.

So, I was looking for a way to have a single repository for a class and all my projects for that class would be stored under that repository. That's when I came across this nifty little feature [here](https://help.github.com/articles/about-git-subtree-merges/) called Git subtree merges, which allows you to manage multiple projects under a single repository.

The workflow as I understand it is as below:




  1. I created a repository called `advanced-data-structures`. This is my main repository.


  2. Then I created another repository called `RedBlackEventCounter`. This holds the actual project code. Made changes, committed and pushed to this remote.


  3. Then I added the remote of `RedBlackEventCounter` to the master of `advanced-data-structures`.

				git remote add -f RedBlackEventCounter https://github.com/sayakbiswas/RedBlackEventCounter.git

  4. Merged `RedBlackEventCounter` into `advanced-data-structures`.

				git merge -s ours --no-commit RedBlackEventCounter/master

  5. Copied the git data of `RedBlackEventCounter` repository into a new directory in the `advanced-data-structures` repository.

				git read-tree --prefix=RedBlackEventCounter/ -u RedBlackEventCounter/master

  6. Commit and push the changes.

				git commit -m "Added RedBlackEventCounter reference into advanced-data-structures"
				git push origin master


Now, this subtree doesn't automatically sync with the changes made in the upstream repository. GitHub's documentation recommends using the below command to update:

		git pull -s subtree remotename branchname


**<span class="emphasize">[Update - 03/15/2016]:</span> The above command seems to work properly now. I'm not sure what had happened earlier; probably some mistake on my part. Need to dig deeper. So my workflow is now:**

		git pull -s subtree RedBlackEventCounter master
		git push origin master

**<span class="emphasize">The below is not needed anymore.</span>**

But for some reason, it doesn't work out for me. I keep getting the error

		error: Entry %filename% overlaps with %filename%. Cannot bind.

So, what I do is create a temporary directory and pull in everything from subtree remote. Copy over everything from this directory to the subtree directory. Remove the temporary directory, stage all, commit and push.

		mkdir RedBlackTemp
		git read-tree --prefix=RedBlackTemp/ -u RedBlackEventCounter/master
		git commit -m "Pulled upstream changes"
		cp -rf RedBlackTemp/* RedBlackEventCounter/
		git rm -rf RedBlackTemp
		git add .
		git commit -m "Merged upstream changes into master"
		git push origin master

I know it is quite cumbersome to do this everytime you make a change. I guess there is a better way that I just don't know yet. So, if anybody has an idea, please let me know.
