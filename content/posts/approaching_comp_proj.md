---
title: "Approaching Large Computational Projects"
date: 2020-06-01T09:54:08-07:00
draft: false
tags: ["ciera", "about", "brainstorming"] 
---



## How to Approach a Large Computational Research Project

Below are some general strategies and tips for approaching the design of large computational data analysis project. These strategies are by no means standards of what you should do, rather, suggestions. Every project, person, and team is different for approaching a computational project, so feel free to judge for yourself if these do or do not work for you. Below is the culmination of my experiences and those suggestions that came up during a discussion in the Eisen Lab Coding Club Discussion on May 26, 2020. 

### How I think of Designing a workflow

Below is a Figure from a paper I wrote with Sara Stoudt and Valeri Vasquez at the Berkeley Institute of Data Science (releasing soon!).  This figure illustrates how I see data analysis really occurring in academic data science. You go iterate through phases that are defined by who your audience is for your analysis code. At any phase you can develop research products. The whole workflow and even the design of the workflow constitutes research. 

Workflow vs Pipeline Terminology: 



### General Computational Project Workflow Tips

-   Outline what you want to accomplish. Write that out in plain English. Diagram out if possible!  
	Some examples from my projects:
	-  [MS2](https://github.com/DiscoveryDNA/reading_czi_stack_videos_GH)
	-  [TFBS Presence](https://github.com/DiscoveryDNA/TFBS_presence)
-  Spend the time to survey on how people approach the problem! Give yourself time to really explore what tools are out there.
    - Google Everything
    - Ask People Around You
    - Peak into paper methods, especially those that have a Github repo. Most papers aren't packaged well enough to actually reproduce their work, but they can be helpful.
-  Reduce your dataset to something small and can be handled on your computer.  
	-  Learn how to randomly sample your dataset to make a subset. 
	-  Or deal with one file at a time. 
	-  Don't spend time dealing with the challenges of looping through many files or dealing with memory issues until the end. 
-  Design a pipeline by trying to solve all your goals as shitty as possible 
	- All computational projects deal with inputs and outputs of data, so it is best to have a concrete example of what these are instead of spending time trying predict. You will never guess what sort of weird data configurations you will need from the start. This often comes up when you have to use a specific tool/library/package that only works with a specific data type. 
	- Make notes on what aspects are shitty in the pipeline while working through. Those notes will become the next steps of your work AFTER the pipeline is finished. 
	- Once the shitty pipeline is finished, its easier to split up the project for others to work on.  Each person can be assigned an aspect of the pipeline without affecting others work. 
	- Trying to get through the pipeline as quickly as possible decreases scope creep. Keep your main goals of the project at the forefront of your mind and resist the urge to go down interesting wormholes (unless you know they will teach you a valuable skill!). 
- Take lots of notes
	-  Especially when learning. Make entire notebooks that are for only learning a technique to explore. 
		- ex: [Exploring finding dots](https://github.com/DiscoveryDNA/reading_czi_stack_videos_GH/blob/master/notebooks/01_explore.ipynb)
- Realize that the time it takes to organize your files, design your pipeline, learn new skills, and take detailed notes is part of your job. Give yourself time for these aspects. The end result is not just a research paper. You can even wrap up this work into more intermediate products such as tutorials, Data Management Plans, Blog Posts, and published intermediate datasets. Balance how your research products serve your career.

### Image Analysis Workflow Tips

Overly simplified Image Analysis steps:

1. Input image and explore
2. Reduce noise and Segment a Feature (back and forth)
3. Analyze

### Tips

- Images are very visual - take advantage of this. Find the best ways to look through your work easily. Make sliders (see Marc's tutorial). Ask questions of your images and get a feel for all the slices before you start analyzing. Figure out ways to ask these questions programatically (with code). 

- Become comfortable with the many dimensions of your data. There are many dimensions to 4D data (X, Y, Z, time) and in the case of confocal microscope videos, your data has an addition dimension - channels! When beginning to explore this data, learn to look at each dimension in pieces. For example, find the first time point of the first channel and just look through each image. Do this at each time point to you get a firm idea of what is in the data. Do this in multiple ways. Ask questions of the data, write these questions down. Record your concerns.

- Visualize everything at every step and keep notes. Visualize the image, but also visualize more abstract questions with plots. Display intermediates. For example, you will setting the parameters of image analysis algorithm parameters often. Learn to visualize how your image changes depending on the parameter you set. Don't just delete all the code and visualizations that helped you choose the parameter. Leave in the notebook with notes on why you choose a particular parameter. 

- Its okay to play with the images, develop a prototype pipeline, or even do the whole pipeline in Fuji. Depending on your project or skill level, attempting to do image analysis in Python is overwhelming. There are advantages to using a Python (automation, reproducibility, learning more in depth characteristics of you data and how to code), but really, if you have no interest, doesn't help your career, and get can to your results without it - do it. But, you should try, just from experience, I hated to code when I started graduate school and it took over two years to actually learn that I enjoy it. Now I'm obsessed and it opened so many more doors career wise than any other skill I learned over the past 15 years.


