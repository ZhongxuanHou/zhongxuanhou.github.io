---
author: sayakbiswas
comments: true
date: 2011-08-12 06:42:23+00:00
layout: post
slug: playing-mp3-files-with-java
title: "Playing MP3 files with java..."
wordpress_id: 210
category: blog
tag:
- Programming
- Java
blog: true
---

For a language as popular as Java, lack of standard ways of implementing mp3 playback is disappointing. This is understandable though, due to horde of patent and licensing issues relating to MP3 as a format. A bit of googling and I found two methods: using the Java Sound API along with the MP3 plugin and using the third party JLayer API from JavaZoom. Here I'm using JLayer as it seems to be the more popular alternative.

First we need to download the jlayer from [here](http://www.javazoom.net/javalayer/sources.html). Extract it and add the **<span class="emphasize">jl1.0.1.jar</span>** to the project. When using an IDE like eclipse adding the jar to the build path suffices otherwise **<span class="emphasize">jl1.0.1.jar</span>** should be added to the `CLASSPATH`.

JLayer provides two built in players that play mp3s using the library: `javazoom.jl.player` and `javazoom.jl.player.advanced`. I'm using the Player class.

Create an instance of the Player class while providing a FileInputStream object of the mp3 file. Then use the play() method of the class to start playback.

Below is a very basic implementation of the playback process:

```java
import java.io.*;
import javazoom.jl.player.Player;

public class JavaPlayerTest {

	public static void main(String[] args) {
		try {
			FileInputStream mp3file = new FileInputStream(args[0]);
			Player playmp3 = new Player(mp3file);
			playmp3.play();
		} catch (Exception e) {
			System.out.println(e);
		}
	}
}
```
