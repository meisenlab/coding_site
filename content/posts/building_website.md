---
title: "Building a Hugo Website"
date: 2020-03-20T09:54:08-07:00
draft: false
tags: ["website", "tutorial"] 
---

There are three main reasons I would like to start this series with a website tutorial. 1. A website allows you to communicate to world the easiest - especially communicating your work through your own personal website 2. If you host your website on Github, this is an excellent way to learn how to use Git. 3. Understanding how to use git and being able to build a website allows you to collaboratively build content. We can build anything together!


## Prerequisites/ Installs

- Install homebrew: Open Terminal and copy and paste `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`. Homebrew allows you to install things onto your computer easily. 
- Get a Github account and give your name to Ciera.
- Install a plain text editor: I use [Sublime Text](https://www.sublimetext.com/). 
- Brush up on Markdown: If you go through this tutorial, you are gold. [Markdown Tutorial](https://www.markdowntutorial.com/lesson/1/)
-  Install Hugo: `brew install hugo`. Hugo is the program that helps us build our website.

### Outline

Part 0 - Getting ready and brushing up on Unix

Part 1 - Building a website with Hugo

Part 2 - Hosting on Github 

### Part 0 - Getting ready and brushing up on Unix

I like to give the minimal amount of commands to get going on using something. I will add more as we need them. But as of now, these are the three main commands you need. 

- `ls`: List. Use frequently to ask what is in a directory.
	-	Frequent uses: `ls` alone will tell you all the files in the directory you are in.  `ls name_of_directory`
- `cd`: Change Directory. 
	-	Frequent uses: `cd name_of_directory` or `cd ..` move back one directory.  If you use just `cd` without anything after you will navigate to your "home" directory.
- `open`: If you are using a mac, `open` is amazing. It basically acts analogously to clicking on something. 

Those are the three main commands, we will add some more later.

### Part 1 - Building a static website with Hugo.

There are two main types of websites on the Internet, static websites and dynamic websites.  **Static website** are composed of content that is fixed, the user cannot add or remove anything to the website. The files of the website and what the user sees will not fundamentally change in reaction to the website viewer. A **dynamic website** is one in which the user can interact, like inputing information about the user or playing a game, any website that collects user inputted information is dynamic website. 

We will be making a static website with a static website generator called Hugo. Let's just build one and after we can start poking around to see what Hugo actually does. 

1.  Follow this tutorial: [Quick Start](https://gohugo.io/getting-started/quick-start/)
2. Change the theme by picking your favorite theme [here](https://themes.gohugo.io/)


