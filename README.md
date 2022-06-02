# Python based ParFlow short course <!-- omit in toc -->
This short course provides an introduction to ParFlow. All of the exercises provided here use the python interface for ParFlow. If you prefer to work through the tcl interface you can refer to these [basic](https://github.com/hydroframe/ParFlow_Short_Course) and [advanced](https://github.com/hydroframe/ParFlow_Advanced_ShortCourse) short course repos. 

## Table of Contents <!-- omit in toc -->
- [ParFlow Examples Contained in this repo](#parflow-examples-contained-in-this-repo)
- [Additional Training Resources](#additional-training-resources)
- [Setting up your run enviroment](#setting-up-your-run-enviroment)
  - [**1. Quick start**](#1-quick-start)
  - [**2. Other options for running parflow**](#2-other-options-for-running-parflow)
    - [**ParFlow Docker**](#parflow-docker)
    - [**Local ParFlow build**](#local-parflow-build)
  - [**3. Python packages for ParFlow**](#3-python-packages-for-parflow)

## ParFlow Examples Contained in this repo

1. **Little Washita ParFlow Simulations**: These exercises walk through a variety of simulation configurations for the Little Washita watershed. All script are setup just to build and run the Parflow simulation. Refer to the pre and post processing list for examples of creating inputs and evaluating outputs. 
     - [LittleWashita_ParFlowCLM_AnnotatedExample.ipynb](https://github.com/hydroframe/parflow_python_shortcourse/blob/main/exercises/little_washita/LittleWashita_ParFlowCLM_AnnotatedExample%20copy.ipynb): This is the most fully documented script. It illustrates the complete setup for a watershed simulation running with ParFlow-CLM
     - [LittleWashita_Parkinglot.ipynb](https://github.com/hydroframe/parflow_python_shortcourse/blob/main/exercises/little_washita/LittleWashita_Parkinglot.ipynb): A simplified test case without CLM where we evaluate drainage networks by making the subsurface impermable and applying a simple rain pulse to the domain.
     - [LittleWashita_Spinup.ipynb](https://github.com/hydroframe/parflow_python_shortcourse/blob/main/exercises/little_washita/LittleWashita_Spinup.ipynb): An illustration of how to 'spinup' your model to achieve a steady state groundwater configuration. 
     - [LittleWashita_TableInput.ipynb](https://github.com/hydroframe/parflow_python_shortcourse/blob/main/exercises/little_washita/LittleWashita_TableInput.ipynb): An alternate verson of the main CLM example illustrating how you can set subsurface properties with a csv table rather than within python. 
  
2. **Little Washita Pre and Post Processing Examples**: 

## Additional Training Resources
In addition to this short course there are multiple other ways to learn more about ParFlow and connect with the community we encourage you to check out these resources. 
- [ParFlow Website](https://parflow.org/): General information about the code and updates
- [Parflow Blog](http://parflow.blogspot.com/): Tips on workflows and common issues
- [Parflow GitHub Repo](https://github.com/parflow/parflow): Where all of the code lives and development happens 
- [ParFlow user Group](https://groups.google.com/u/1/g/parflow): **NEED link to this**
- [ParFlow Read the Docs](https://parflow.readthedocs.io/en/latest/index.html): Complete documentation of all ParFlow keys and options. 
- [ParFlow manual pdf](https://github.com/parflow/parflow/blob/master/parflow-manual.pdf): now older, PDF version of the manual. 

## Setting up your run enviroment
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
   
4. Next run the following command from your terminal on mac / linux: 
   ```
   docker run --rm -it -p 8888:8888 -v $(pwd):/data reedmaxwell/parflowjupyter
   ```
   and run this command on Windows:
   ```
   docker run --rm -it -p 8888:8888 -v %cd%:/data reedmaxwell/parflowjupyter
   ```
This will launch a notebook server with access to the directory you are in and every one below it.  If you get a 404 error or file not found you might have [this issue](https://github.com/darribas/gds_env/issues/8).

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
ParFlow docker (using TCL) and discussion is included in the ParFlow GitHub Repo: [https://github.com/parflow/docker](https://github.com/parflow/docker)


#### **Local ParFlow build**
Local ParFlow build guides can be found in the [ParFlow Wiki](https://github.com/parflow/parflow/wiki/ParFlow-Installation-Guides) and the [ParFlow Blog](http://parflow.blogspot.com/search/label/compiling).

### **3. Python packages for ParFlow**
Please see the requirements.txt for this repo.


