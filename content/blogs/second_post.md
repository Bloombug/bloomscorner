+++
title = "Page Optimization, Plugins and Jazz"
description = "Getting a grip on what is going on behind the scenes..."
date = 2021-01-22
tags = [
    "Go",
    "Hugo",
]
draft = false
+++

So, here we go. The first step was to take a bunch of working stuff, put it into a repository, plug it to the wall and turn it on. And guess what, it works! But does it work as FAST as it should work? Does it load the bare MINIMUM to properly work, or is it bloated with JS scripts and boilerplate code? 

I am throwing these questions in here because, while connected to my (fairly quick) mobile hotspot the site loads every page quick. 
Not smoothly, just quick. 
In fact, it loads every page with a speed that makes you wonder if it could be faster. If you try and open any page using my ADSL-powered WiFi network, then it can take a whole minute to load a couple of paragraphs on a white background, with some blue links on the top right corner. Not talking about any images, or high resolution videos, not even a .gif file: just plain text on a plain background.

So, i will be trying to maximize the speed of my project, by following the advice written [here](https://martijnvanvreeden.nl/10-ways-to-improve-your-hugo-website-performance/): it should help me understand a bit more about backend Javascript performance, and help me figure out some basic performance tips and tricks when dealing with webservices.

* Now the first 2 tips that Martijn refers in his guide deal with preloading and prefetching of javascript files and page resources, respectively. It can be summarized as such:  since a Hugo page is built based on multiple parts (and, consequentially, multiple folders and files and paths), you need to load every component you may need into a page, every time you load one.

So you will be calling scripts and resources from other parts of your project. This means that, if you could make it so the project loads those scripts when they are actually needed, for instance, you can minimize the effort put into loading a simple blog page that doesn't really need to consume anything from your "video streaming" script.

In my case, there was a highlight.js script that did not need to be loaded every time i wanted to check a single blog post, so i deleted it. Since it did not brick my entire project nor did it end up starting WW3, i assume it is safe to work without such script. Baby steps people, baby steps.

I also ended up removing all font scripts the template had, because who needs all varieties of Noto Sans, right? Sans-Serif works just fine! Long gone are the days where i would spend twice the amount of time and effort trying to find a neat font to put on my project, and half of it figuring out how a "router" works. 

