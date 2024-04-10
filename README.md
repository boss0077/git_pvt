# Git_pvt

<h2>  &nbsp;Tools I Have Used</h2>
<p align="left">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="vscode" width="45" height="45"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" alt="bash" width="45" height="45"/>
</p>

# Day 1 : Intro 🚀
Git is VCS- version control system aka, RCS- revised control system
Used to track changes on our local files on our own computer.
Git is open source software, GitHub is a platform(or hosting service) for it.
Founded by Linus Torvalds in 2005 - who is also founder of Linux kernel.
Simple example for VCS is google docs, git , ppt etc

Basic linux code 
```sh
Pwd - to show name of current directory.
Cd  - change the directory 
Ls - is to list all the files in current directory 
Mkdir - is to create new file  
```

Repository - repo : place we see all the versions of the code in one place.
Git init : cmd to initialise the repository  in local machine 
Git status : to get the repository status 
Git clone ‘URL’ : to clone a repo.
The file(.git) will be hidden which will follow the git repository


# Day2 : Commands	
Git add : to change code in repository 
	git add . : Will add all the altered files in staging area
Git commit : committing the changes
	git commit -m “comment” —command we use
Git push and git pull : push or pulling changes 
Git status, git log and git diff : checking status logs and changes
	git log : show the log of committed code to repo 

Working directory : is where files are like personal computer
Staging area ; place where we move(add) file before commit 
Repository(local) : when we commit the code it will be reflected  in repository
If we push then the repository is local will be pushed to GitHub
If we pull then the repo in GitHub is synced in local machine 

Before doing push we need to run 
	git branch -M main  —where main will be the local branch name 
Eg: git remote add origin (link with token)
 Then git push -u origin main — where origin main is the remote repo name

Git fetch : will fetch the data from remote repo and put it in local repo.
			here the data will not be transferred to local pc(working directory) but just 			to see the updates - using git checkout main
Git pull : will pull the data to working directory where we can see the file.
	here we pull all the data to local repo	and can see all data 

—Note : In general should pull before pushing to remote branch to be in sync.

After doing fetch we cannot see the commits in logs then we need to run 
Git checkout origin/main — in this we can view the remote repo in local pc 
	note : the above command will switch to remote repo: origin/main
Then running command Git switch main will change the repo to local one
Finally we can do git pull where we can see the data in local repo.


# Day 3 : Git Branches 
Branches allows to organise repo and splits so multiple people can work on it.
We need branches to focus on new update without breaking old code.
Initial branch when we do (git init) - it will just create main branch.
Branches are just pointers to commit.

HEAD - will help in getting to know where we are in regards to branches and commits.  For this we use — git checkout.

```sh
 To create new branch - git branch “branch name”
To switch new branch - git switch “branch name”
To change branch name - git branch -m “branch name”
To delete branch - git branch -d “branch name”
```

Git Merge - 
We have fast-forward merge where there is no change in main and easy to merge.
We might	have some conflict for merge then we have to choose manually.

Git Diff -
Tool to display the differences in versions(data sets)


# Day 4 : Undoing 
To get the hash codes - git log --oneline
To get to that pointer then - git checkout “specific hash”
To get back to main branch - git checkout main

—ITS BEST TO USE GIT REVERT THAN OTHER—

Git restore - to restore file to its previous most recent commit. -cannot undo
This can also upstage wt we have in staging area using git add.
I.e. if we try to code a lot in between and is difficult to undo it as it crashed then to move back to previous stable committed code we use restore.
We can do above by - git restore —staged filename

Git reset  -  
Allows us to remove commits and reset the branch.
It will not change the file itself but just reset the commit .

Git revert -
It creates new commit that matches the historical state previous commit.
I.e. if we have some buggy code and want it for tracking purpose then we can revert it tho it will be in history it will be reverted to previous commit change.

# Day 5 : Workarounds
Git stash - temporarily shelves changes made to working copy so we can work  on something else to come back and reapply later.
i.e. it is generally useful when we want to quickly switch branches but in middle of changing file.
Later to get the stash back - git stash pop

Git remote - lets you to create, view and delete connection to other repository.
Remote is a URL where host repo leaves such as GitHub URL
To list remote connections with URL - git remote -v

.gitignore - special file to list which files not to track.

Workflow patterns:
	●	single branch workflow
	●	branch based development

We can do pull request from GitHub too and with many users if in project working on different features its most helpful.

Forking in GitHub: 
It only creates a copy in GitHub and we can clone it to local repo and work on it while staying connected with original one (upstream). Where if we get updates on original repo it will be reflected in local repo. 

Git hub actions:
It is CI/CD continuous integration and continuous delivery platform that allows to build, test and deploy pipeline.

Git hub actions has detailed file called  - YAML file. 


