# Python based ParFlow short course <!-- omit in toc -->
This short course provides an introduction to ParFlow. All of the exercises provided here use the python interface for ParFlow. If you prefer to work through the tcl interface you can refer to these [basic](https://github.com/hydroframe/ParFlow_Short_Course) and [advanced](https://github.com/hydroframe/ParFlow_Advanced_ShortCourse) short course repos. 

## Table of Contents <!-- omit in toc -->
- [Additional Resources](#additional-resources)
- [How to use this repo](#how-to-use-this-repo)
- [Setting up your run enviroment (@Reed don't love this title)](#setting-up-your-run-enviroment-reed-dont-love-this-title)
  - [**1. Quick start**](#1-quick-start)
  - [**2. Other options for running parflow**](#2-other-options-for-running-parflow)
    - [**ParFlow Docker**](#parflow-docker)
    - [**Local ParFlow build**](#local-parflow-build)
  - [**3. Python packages for ParFlow**](#3-python-packages-for-parflow)
  
## Additional Resources
In addition to this short course there are multiple other ways to learn more about ParFlow and connect with the community we encourage you to check out these resources. 
- [ParFlow Website](https://parflow.org/): General information about the code and updates
- [Parflow Blog](http://parflow.blogspot.com/): Tips on workflows and common issues
- [Parflow GitHub Repo](https://github.com/parflow/parflow): Where all of the code lives and development happens 
- [ParFlow user Group](): **NEED link to this**
- [ParFlow Read the Docs](): **NEED link to this**
- [ParFlow manual](https://github.com/parflow/parflow/blob/master/parflow-manual.pdf): This is the main pdf of the manual documenting all the keys. 

## How to use this repo
**To Do at end**: List out the exercises and whats included

## Setting up your run enviroment (@Reed don't love this title)
If you are working with ParFlow through the python interface you will need two things (1) the actual ParFlow model, you can build this locally or run it through a Docker and (2) the python tools for interacting with ParFlow. 

The easiest way to work through the materials of this short course is to follow the quick start instructions which point you to a Docker which includes ParFlow along with all the python packages you will need.  

As you work more with ParFlow though you may want more control over your enviroment and to have your own builds. If this is you, see the notes below for other options for running parflow and for the python packages you will want to install. 

### **1. Quick start** 
The quickest way to jump in and work through these exercises is to start from our docker setup. This includes ParFlow in addition to all of the python packages you will need for the short course.  

1. Clone this repository to your local machine. 
   ``` 
   git clone {path to this repo}
   ```
   If you are new to GitHub you will first need to make sure you have GitHub installed. There are lots of great resources online to learn more aobut Git and GitHub one good place to start is the [GitHub Documentation](https://docs.github.com/en/get-started/quickstart)

2. If you don't already install Docker from [here](https://docs.docker.com/get-docker/).
   
3. When you launch the Docker it will just have access to the directory you launch it from and every directory below it. So the first step is to open a terminal windo and navigate to the directory that you cloned the short course into
   
4. Next run the following command from your terminal: 
   ```
   docker run --rm -it -p 8888:8888 -v $(pwd):/data reedmaxwell/parflowjupyter
   ```
   This will launch a notebook server with access to the directory you are in and every one below it.  

5.  After you run the previous command you should see outputs that look like this:
    ```
    To access the server, open this file in a browser:
        file:///root/.local/share/jupyter/runtime/jpserver-1-open.html
    Or copy and paste one of these URLs:
        http://0422cde8d804:8888/lab?token=bb8f1a6796cf090dfb01c06128b43b573f37feed649da96f
     or http://127.0.0.1:8888/lab?token=bb8f1a6796cf090dfb01c06128b43b573f37feed649da96f
    ```
    Open a browser window and copy and paste the last line that you get here into it. This should take you to a Jupyter notbook server and you should be able to see all the files in your directory here. 


### **2. Other options for running parflow**
#### **ParFlow Docker**
**to do**

#### **Local ParFlow build**
**to do**


### **3. Python packages for ParFlow**
**@Reed** can you add a list of the packages that are included in your docker here or maybe we just include a YAML file?


