# git_tutorial
The purpose of this tiny repo is to learn the basics of git, using github.  
At first, we will play a bit with git to see how it works, then there will be a second session with slides to see how to use it in your projects.
Requirements:
+ a computer with a POSIX operating system (linux or macOS)
+ an internet connection
+ the software git installed. For example, on ubuntu-like OS, you can install it with `sudo apt install git`


## Step 1
Create an account on github.com

## Step 2
Create a repository

What is a git repository (repo in short)? 
It is what we usually use to organize a single project. It contains files (source code, images, pdfs .... anything you want).
And, most importantly, it is organized to keep track of all the __history__ of the modifications done on it.
We'll see that in a bit

+ Connect to your github account
+ Create a new repository. 
  + On the main panel, on the left, there is a green button 'new'. Click on it
  + Choose a repository name, like 'hello-world'
  + Give a short description, like 'Repo used to learn the basics of git'
  + Keep the repo public, because you should not have access to private repositories (as students, you can have access to private frpo for free, there's put a link for that below).
  That means everything on your repository will be public on the internet.
  + Tick 'Initialize this repository with a README'
  And now click on 'Create repository'. Your repo is created
+ We will now clone the git repo on your machine.
  + Open a terminal
  + Create a git directory in your home. You will store all your repositories there. `mkdir ~/git`
  + Go in your new directory: `cd ~/git`
  + To clone your repository, you will need its address: on the web page of your repository (https://github.com/<your-name>/<your-repo-name>), there is a green button 'Clone or download'. Click on it and copy the https address.
  + Now back to the terminal. Enter the cloning command: `git clone https://github.com/g1t-d3m0/git_tutorial.git`
  
