# Git Tutorial: 101
The purpose of this tiny repo is to play with the basic functions of git, using github.
At first, we will play a bit with git to see how it works, then there will be a second session with slides to see how to use it in your projects.  
Requirements:
+ a computer with a POSIX operating system (linux or macOS). Windows can do the job too, but I don't know how.
+ an internet connection (if you read this you probably have one)
+ the software git installed. Have a look [on the official page](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for instructions. Choose the easiest way.


## Step 1: Create an account on github.com and configure git
This is self explaining. You need an email address for this purpose. You can change the email address linked to your account later.  

Now, open a terminal window and set the two following things:  
`git config --global user.email <your-email>`  
`git config --global user.name <your-name>`   
NB: in command lines, replace what is between '<  >' by their real values.
## Step 2: Create a git repository


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
  
## Step 3 : Clone this repository on your computer
+ We will now clone the git repo on your machine.
  + Open a terminal
  + Create a git directory in your home. You will store all your repositories there. `mkdir ~/git`
  + Go in your new directory: `cd ~/git`
  + To clone your repository, you will need its address: on the web page of your repository (`https://github.com/<your-name>/<your-repo-name>`), there is a green button 'Clone or download'. Click on it and copy the https address.  
  + Now back to the terminal. Enter the cloning command: `git clone https://github.com/g1t-d3m0/git_tutorial.git`
  + The output should look like this:  
    `Cloning into 'git_tutorial'...`  
    `remote: Enumerating objects: 3, done.`  
    `remote: Counting objects: 100% (3/3), done.`  
    `remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0`  
    `Unpacking objects: 100% (3/3), done.`  


Great ! Now the repository exists in 2 places ! It exists online, on the github servers (called 'remote'), and locally on your computer.
   
## Step 4: Start a nice coding project
For this tutorial, we will do a great coding project in C.
+ Create a new file in your repository folder (it should be `~/git/<your-repo-name/`) called `hello.c` with your favorite text editor.
+ Paste the code contained in [this file](https://github.com/g1t-d3m0/git_tutorial/blob/c_project/hello.c) (spoiler: it's a hello world)
+ Verify that you can run it. In a terminal, compile it (`gcc hello.c -o hello`), try and run `./hello`. It should print 'Hello, world!'

So the first version of your project is ready, and it looks functional.  
We will now _commit_ this code, meaning that we save the entire state of the project in git.  
Then we will push it to our remote repository.  

## Step 5: Commit and push

It is now time to commit our nice project, so it is saved forever.  

+ First, we need to stage (add) the files that have been modified or created, and that are required for this project.
+ Open a terminal, and go to your git repo: `cd ~/git/<your-repo-name>`
+ Run `git status`. It is a very useful command, that gives you informations about the current status of your repository. It should look like that:  
`On branch master`  
`Your branch is up to date with 'origin/master'.`  
` `
`Untracked files:`  
`  (use "git add <file>..." to include in what will be committed)`  
` `
`	hello.py`  
` `
`no changes added to commit (use "git add" and/or "git commit -a")`  

+ Stage (add) the file `hello.py`: `git add hello.py`. This command tells git that you want to keep track of the modifications done on the file. It is just an intermediate step, nothing is saved at this point.
+ Now git status looks like that:  
`On branch master`  
`Your branch is up to date with 'origin/master'.`  
` `
`Changes to be committed:`  
`  (use "git reset HEAD <file>..." to unstage)`  
` `
`new file:   hello.pyg`  
+ Now we will commit our changes. A commit is a sort of 'milestone', or a 'save point'. In the future you will always be able to come back to the state of the project as it was at any commit, which is very useful. The commit command:  
`git commit -m "Project hello world started: added hello.py"`
+ The output of this command gives you the branch name (we don't think about branches for now), the hash (the identifier) of the commit you just did, with its name (Project hello world started: added hello.py). It also says how many lines were added, removed, and which files were created/deleted.

So now we commited our changes, but the online version of the repository did not change (you can check in your browser). It is now time to _push_, meaning that we will send the changes commited to our repo to the online version.

+ Check the status of your repo with `git status`. It now tells you that:  
`On branch master`  
`Your branch is ahead of 'origin/master' by 1 commit.`  
`  (use "git push" to publish your local commits)`  
` `
`nothing to commit, working tree clean`  
+ Let's push: `git push`. You will be asked for your git login and password.


## Step 6: Add a new feature to the project

+ Now the hello world will be printed in colors !
+ Modify the code of hello.py: replace `printf("Hello, world!\n");` by `printf("\033[32;1mHello, world!\n");`. This will print in green.
+ Now you know the job :-)
+ Stage hello.py: `git add hello.c`
+ Commit your changes: `git commit -m "hello.c prints in green now"
+ Push them: `git push`


## Conclusion



Congratulations! Now your hello world project will live forever in github !
Git is a fantastic tool, once you get the habit to use it for your projects, you won't be able to code without it.   
Among the important features:
+ It allows to work in teams, synchronizing the code base effortlessly
+ It is a solid backup of the code: your projects, which can represent many hours of work, will never get lost
+ It keeps tracks of the states of the project: no more 'it used to work but now it's broken...'
+ These are 3 out of hundreds of nice features.
