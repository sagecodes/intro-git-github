# Introduction to Git and Github
## URL for this repo: [git.sage.codes](https://github.com/sagecodes/intro-git-github)

## Setting up your computer


- Have patience. Setting up software tools can be frustrating, but you'll get trough it! 

#### Please set up the following:

- [Install git https://git-scm.com/downloads](https://git-scm.com/downloads)
- [Create a github account https://github.com/join](https://github.com/join)
- Install a text editor like [VS code](https://code.visualstudio.com/) or [Atom](https://atom.io/)
- create a folder and open your text editor to that folder (This is where we will do file changes!)

## About me:
Hello I'm [Sage Elliott](http://sageelliott.com/). I'm a Technology Evangelist here at Galvanize! Previously I've worked as a software and hardware engineer with Startups and Agencies in Seattle, WA and Melbourne, FL. I love technology! I'm currently learning more about building AI and VR projects. 

- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)


## About you!

Give a quick Intro!

- Whats your name?
- Whats your background?
- Why are you interested in JavaScript?


## Overview
The goal of this brief course is to get you comfortable enough to start using git and github with your projects! The best way to learn it is to start using it on your projects outside of this workshop!

In this workshop at a minimum we should be learn to:

- Create a git repo
- understand the git stage cycle
- add changes to the repo
- create repo on github
- push our repo up onto github
- push changes onto github
- pull changes from github
- clone a repo from github to our machine

Lets do it!!!!! 


#### Before we begin:
* This course is for absolute beginners
* Feel free to move ahead
* Help others when you can
* Be patient and nice
* You will get through it!
* git and github is complicated! Don't worry if it doesn't 100% make sense to you after the workshop. If you keep using it will!




## What is Git?
Git is a version control system used to track changes in your files. 

why use it:

- undo mistakes & changes
- experiment on branches(a duplicate of your project) 
- use with github or other online options to share and collaborate

Git was created in 2005 by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds)(the creator of [Linux](https://en.wikipedia.org/wiki/Linux)).

## What is Github?

Github an online hosting and collaboration service that can be used with the version control system git.

In 2018 Microsoft purchased Github for 7.5 billion!

Created in 2008 by Chris Wanstrath, PJ Hyett and Tom Preston-Werner.

Github is free to use as long your projects are open / visible to anyone.  If you want private repos for yourself or a team you need to sign up for a paid account.


## Who uses Git & Github?

Almost everyone in the working world uses some form of version control. The most popular by far is Git. 

A lot of companies use Github as their online collaboration tool, but there are other very similer options such as, [Bitbucket](https://bitbucket.org/product) and [Gitlab](https://about.gitlab.com/).



## What is Github?
Github is a way to store you files tracked with git online.

why use it:

- sharing projects with others (Collaboration and Code Reviews)
- backup your projects
- great way for companies to see your skillset!
- release to production 

## Git Started:

We're going to to use our terminal / command line. One windows you should us the `git bash` program that got installed when you followed the setup section.

a few terminal commands we will want to remember.

- `cd` change directory 
	- `cd foldername` moves you into the folder you specify
	- `cd ..` moves you back one folder
- `ls` List items in folder
- `ls -a` List all items (even hidden files)

How to exit terminal text editors (DONT GET STUCK)

- nano `ctr + x` `ctr + o`(save & exit)
- vi/vim `:q`(exit) `:wq`(save & exit)

##### Setup
We should do this before we start using git

`git config --global user.email "name@email.com"`
`git config --global user.name "FirstName LastName"`

##### First commit
- `git init`
- `git add .` 
- `git status`
- `git commit -m"Commit Message"`

You just made your first commit!

sometimes you don't want to add every file like the `git add .` command does. Instead you may want to only commit specific files. You can use `git add filename.file` command. replace "filename.file" with the actual name of your file. 

##### Other ways to commit
 
$ADD IN HERE


##### git commit messages


So what happened?
3 stages of git

- Modified (When we used `git status` and saw it red)
- staging (When we used `git status` and saw it green)
- commited 

lets make a small change to our file

- `git status`
- `git add .`
- `git commit -m"message"`

Lets see what commits we have made so far!

- `git log`
- `git log -p` (pres `q` to get back to bash promt)

##### Undo staging

- `git reset HEAD` will pull all the files out of staging
- `git reset HEAD filename.file` this will pull the file out staging


##### Git Diff
- `git diff`
- `git diff --staged`

##### Remove and move
git rm filename.file
git mv filename.file filenamechange.file

##### Disgarding Changes
- `git checkout -- filename.file`

Similarly we can use this command to bring back a deleted file `git checkout -- deletedFileName.file`


##### revert

`git revert cbb60c825aa5b0a1b3c7804de2fe6378c428bfd2`

`git revert HEAD`

##### Branches
`git branch branchname`
`git checkout branchname`


##### merging

`git merge branchname`


## Git out of here!
.gitignore


## Git squashed
Squashing a commit is common in work enviroments

`git rebase -i origin/master` use `f` on commits to change to `fixup`

`r` to reword commit message
`i` to enter interactive mode in vim
esc to get back to where to exit `:wq` (enter)


`git push origin featureBranch --force` commit will need to be forced since history was rewritten


## Git Shared with Github

- `git clone https://github.com/sagecodes/intro-git-github`
- `git remote add origin github_url`
- `git push -u origin master`
- `git push origin branchname`


## Pull Request Workflow
- Fork Repo you want to change (*you wont always need to fork, if repo is already in your org / account*)
- Clone your repo
- Make your changes
- Commit / Push 
- Click "Pull Request"
- Give description of Pull Request
- Choose Correct branch you want to merge to
- Review your commits / change logs (red = deleted grean modified / added)
- Send pull request

---

- owner will usually leave comment or do code review
- Then they may merge branches by clcking confirm mereg request

---
You may want to update from the original repo

cd into/cloned/fork-repo
git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
git fetch upstream

git pull upstream master


## More Resources!

- https://git-scm.com/book/en/v2
- http://sageelliott.com/git-github-commands/
- https://teamtreehouse.com/library/introduction-to-git
- https://git-scm.com/doc
- http://git-school.github.io/visualizing-git/


## Upcoming Events!

[Learn to Code Meetup](https://www.meetup.com/Learn-Code-Seattle/)


## What is Galvanize?
###### We are a community!
#### Immersive Bootcamp
- [Data Science](https://www.galvanize.com/seattle/data-science)
- [Web Development](https://www.galvanize.com/seattle/web-development)

#### Part-Time Courses
- [Data Analytics](https://www.galvanize.com/seattle/data-analytics)
- [Web Development Foundations with JavaScript](https://www.galvanize.com/seattle/web-development-foundations)
- [Data Science Fundamentals](https://www.galvanize.com/seattle/data-science-fundamentals)
- [Front End Web Development](https://www.galvanize.com/seattle/front-end-web-development)
- [REACT INTENSIVE](https://www.galvanize.com/seattle/react-intensive)


#### Co-working Space
[work in our building!](https://www.galvanize.com/entrepreneur)

#### Events 
We host sooo many events! check out out [calendar](https://www.galvanize.com/seattle/events)

## Questions:
Please feel free to reach out to me with any questions!

- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)

#### About the Instructors

[Sage Elliott](https://www.linkedin.com/in/sageelliott/) is a technology evangelist for Galvanize based in Seattle. Previously he worked as a Software and hardware engineer for startup around Seattle WA and Melbourne Fl.

You can email him at [sage.elliott@galvanize.com](mailto:age.elliott@galvanize.com) or tweet [@sagecodes](https://twitter.com/sagecodes) for any further questions.





