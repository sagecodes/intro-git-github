# Introduction to Git and Github
## URL for this repo: [git.sage.codes](https://github.com/sagecodes/intro-git-github)

## Setting up your computer


- Have patience. Setting up software tools can be frustrating, but you'll get trough it! 

#### Please set up the following:

*note* if you already have Git installed skip the 1st step. You can check my opening up your terminal and typing `git`. If it returns a set of commands you can use you already have it installed!

- [Download & Install git https://git-scm.com/downloads](https://git-scm.com/downloads) 
- [Create a github account https://github.com/join](https://github.com/join)
- Install a text editor like [VS code](https://code.visualstudio.com/) or [Atom](https://atom.io/)
- create a folder and open your text editor to that folder (This is where we will do file changes!)

## About me:
Hello I'm [Sage Elliott](http://sageelliott.com/). I'm a Technology Evangelist here at Galvanize! Previously I've worked as a software and hardware engineer with Startups and Agencies in Seattle, WA and Melbourne, FL. I love technology! I'm currently learning more about building AI and VR projects. 

If you have an event you would like to see or put on let me know! I'm always looking for ideas. 

- Website: [sageelliott.com](http://sageelliott.com/)
- Twitter: [@sagecodes](https://twitter.com/@sagecodes)
- LinkedIn: [sageelliott](https://www.linkedin.com/in/sageelliott/) 
- Email: [sage.elliott@galvanize.com](mailto:sage.elliott@galvanize.com)


## About you!

Give a quick Intro!

- Whats your name?
- Whats your background?
- Why are you interested in Git / Github?


## Overview
The goal of this short workshop is to get you comfortable enough to start using git and github with your projects! The best way to learn it is to start using it on your projects outside of this workshop!

In this workshop at a minimum we should be learn to:

- Create a git repo
- understand the git stage cycle
- add changes to the repo
- create repo on github
- push our repo up onto github
- push changes onto github
- pull changes from github
- clone a repo from github to our machine

If we time we can tackle more, but even just with these skills you can start using git everyday with your projects.

You'll probably want to learn more than I can cover tonight, so check out the `More Resources:` section near the end! Come hangout next Tuesday at code hours and I can help you if you're stuck. 


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

why use it:

- sharing projects with others (Collaboration and Code Reviews)
- backup your projects
- great way for companies to see your skillset!
- release to production 


## Who uses Git & Github?

Almost everyone in the working world uses some form of version control. The most popular by far is Git. 

A lot of companies use Github as their online collaboration tool, but there are other very similer options such as, [Bitbucket](https://bitbucket.org/product) and [Gitlab](https://about.gitlab.com/).


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
This adds all and commits in one line 

`git commit -a -m "message"`


this will add the files or folders specified and commit on a seperate line

```
git add file`
git commit -m "message"

```

##### git commit messages
You can type in whatever you want in your commot messages, but you should make sure they're clear what was changed / added. When you start working somewhere its common for there to be a standard format to follow.

##### First Commit Analysis
So what happened in our first commit?
3 stages of git

- Modified (When we used `git status` and saw it red)
- staging (When we used `git status` and saw it green)
- commited 

lets make a small change to our file

- `git status`
- `git add .`
- `git commit -m"message"`

Lets see what commits we have made so far!

- `git log` shows the history of commits
- `git log -p` shows more details about the latest commit

 (pres `q` to get back to bash promt)

##### Undo staging

- `git reset HEAD` will pull all the files out of staging 
- `git reset HEAD filename.file` this will pull the file out staging


##### Git Diff
- `git diff` a quick way to check differences in your terminal


##### Remove and move
git rm filename.file 
git mv filename.file filenamechange.file

##### Disgarding Changes
- `git checkout -- filename.file`

Similarly we can use this command to bring back a deleted file `git checkout -- deletedFileName.file`


##### Revert

`git revert cbb60c825aa5b0a1b3c7804de2fe6378c428bfd2`

`git revert HEAD`

##### Branches

`git branch branchname` Creates a new branch (does not switch to it)
`git checkout branchname` Switches to branch specified


##### merging
Before merging make sure you are on the branch you want to merge your changes INTO. check what branch you're in with `git branch`

`git merge branchname` merges the branch specfied into the current you're on.


## Git out of here!
.gitignore

You may want to always exclude some files or folders. You can include them in a .gitignore file and they wont be added!


## Git squashed
Squashing a commit is common in work enviroments. Think of this add merging a set of commits in to one commit instead of leaving many that you probably did while working on a feature.

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


## Simple Pull Request Workflow
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

`git remote add upstream git:Original_URL`
`git fetch upstream`
`git pull upstream master`


## More Resources:

- [Pro Git](https://git-scm.com/book/en/v2)
- [Sage's git command cheatsheet](http://sageelliott.com/git-github-commands/)
- [Treehouse](https://teamtreehouse.com/library/introduction-to-git)
- [Git Documentation](https://git-scm.com/doc)
- [Git School Visualization](http://git-school.github.io/visualizing-git/)
- [Datacamp](https://www.datacamp.com/courses/introduction-to-git-for-data-science)


## Upcoming Events!

Join us on Meetup: [Learn to Code Meetup](https://www.meetup.com/Learn-Code-Seattle/)

- [Hack the Machine Free 3 hackathon](https://www.eventbrite.com/e/hackthemachine-seattle-registration-48019112458) - this weekedend!
- [Intro to HTML & CSS](https://www.meetup.com/Learn-Code-Seattle/events/253466466/) - Thursday, September 27, 2018
6:30 PM to 8:30 PM
- [Intro to JavaScript](https://www.meetup.com/Learn-Code-Seattle/events/253466491/) - Thursday, October 4, 2018
6:30 PM to 8:30 PM
- [Code Hours](https://www.meetup.com/Learn-Code-Seattle/events/mnlqdqyxmbhc/) - Tuesday, September 25, 2018
6:30 PM to 8:30 PM
- [Intro to Machine Learning](https://www.meetup.com/Learn-Code-Seattle/events/253466541/)Thursday, October 18, 2018
6:30 PM to 8:30 PM


## What is Galvanize?
###### We are a community!
#### Immersive Bootcamp
- [Data Science](https://www.galvanize.com/seattle/data-science) - 1/22/2019
- [Web Development](https://www.galvanize.com/seattle/web-development) - 1/2/2019

#### Part-Time Courses
- [Data Analytics](https://www.galvanize.com/seattle/data-analytics) - 10/23/2018
- [Web Development Foundations with JavaScript](https://www.galvanize.com/seattle/web-development-foundations) - 10/8/2018
- [Data Science Fundamentals](https://www.galvanize.com/seattle/data-science-fundamentals) - TBD



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





