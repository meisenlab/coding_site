---
title: "Building a Hugo Website"
date: 2020-03-20T09:54:08-07:00
draft: false
tags: ["website", "tutorial"] 
---

This tutorial acts as a guide for creating static websites with Hugo.

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
	- Frequent uses: `open .` will open your current directory in finder. `open example_file.md` will open a file in whatever default program your computer opens it.  *Let me know if you want to know how to change your default program settings!*

Those are the three main commands, we will add some more later.

### Part 1 - Building a static website with Hugo.

There are two main types of websites on the Internet, static websites and dynamic websites.  **Static website** are composed of content that is fixed, the user cannot add or remove anything to the website. The files of the website and what the user sees will not fundamentally change in reaction to the website viewer. A **dynamic website** is one in which the user can interact, like inputing information about the user or playing a game, any website that collects user inputted information is dynamic website. 

We will be making a static website with a static website generator called Hugo. Let's just build one and after we can start poking around to see what Hugo actually does. 

1.  Follow this tutorial: [Quick Start](https://gohugo.io/getting-started/quick-start/)
2. Change the theme by picking your favorite theme [here](https://themes.gohugo.io/)

#### Part 1 Tips

- 	A nice set up for working on your site is two terminal windows and a browser window open. Have one terminal window always open "serving" your website locally `hugo server -D`.  That way, when you make changes, you can immediately see what changed on your browser window.
-  Each theme is configured differently.  The best way to understand how to easily manipulate your website is to find a Github repo with all the code for an example website.  Then poke around what they did. 
- 	If you want to play with the theme and styles of your website, you will usually have to mess with .ccs files.  This can be a little confusing, but just google it. For example, in order to change text color for `code text`, I found how to do that on [Stackoverflow here](https://stackoverflow.com/questions/38821339/hugo-pygments-how-to-change-highlighting-theme).
- When changing css files, sometimes it is good to comment using text you know is not in other places.  In .css files to make a comment you start a comment with `/*` , and end it with `*/`  For example: `/* This text is a commented out */` 


## Part 2 - Hosting on Github (in progress)

There are several ways to achieve this and unfortutley, with Hugo, it is a bit complicated.  It is easier with another Static Website Generator [Jekyll](https://jekyllrb.com/), but building those websites is harder. You win some you lose some. 

### Prerequisites

- configure your Github account onto your computer: [see here](https://help.github.com/en/enterprise/2.16/user/github/using-git/setting-your-username-in-git#setting-your-git-username-for-every-repository-on-your-computer). This just authenticates your computer to making changes under your Github id.

### Getting started with git

Let's get started with some basic git commands. There are three stages to getting something onto Github. These are the main commands for going through those stages:

1. Tracking:  `git add .`
2. Commiting `git commit -m "message describing changes"` 
3. Pushing  `git push origin master`



Then, there are a few more commands that are useful

- `git status` - (*)*This is the most useful**) tells you what files are being tracked (what will be commited at that point in time)
- `git log` - shows you a list of all commits
- `git remote -v` - shows you what remote repos your local repo is attached.

![alt text](http://cierareports.org/downloads/gitCheatSheetGitHub_ForkEasy.png "Logo Title Text 1")

### Make our first commit and push

Now go ahead and do the above. Check you can see all your code on Github.


### Host your website

Now comes the time to host your website. There are many ways to do this, but I am going to start with the most simple way. I basically am just following [this tutorial](https://gohugo.io/hosting-and-deployment/hosting-on-github/#deployment-of-project-pages-from-docs-folder-on-master-branch).

1. Change our config.toml file to read: `publishDir = "docs"`
2. Run `hugo -D`.  This should build your entire website into the `/docs` folder. 
3. Push your master branch to the remote repository: `git push origin master`
4. On the Github website, choose the docs/ folder as the website source of your repo. Do the following from within your GitHub project: Go to `Settings → GitHub Pages`
From Source, select “master branch /docs folder”. If the option isn’t enabled, you likely do not have a docs/ folder in the root of your project.
5. You now should have a message saying "Your site is published at `http://yourusername.github.io/yourreponame/`
6. Copy that site name and enter it into your `config.toml` file as `baseURL = "http://yourusername.github.io/yourreponame/`
7. Then go through the three commands for getting something on Github (add, commit, push). 
8. Check that URL (`http://yourusername.github.io/yourreponame/`) on any browser.  *Warning* it may take up to 3 minutes before you see it or any changes that you make. 

That *should* work, but likely didn't.  If no, don't fret, we will figure it out! 









