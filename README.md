# Introduction to Git and Github
## URL for this repo: [git.sage.codes](git.sage.code)

## Setup

- Have patience. Setting up software tools can be frustrating, but you'll get trough it! 
- [Install git https://git-scm.com/downloads](https://git-scm.com/downloads)
- [Create a github account https://github.com/join](https://github.com/join)
- Install a text editor like [VS code](https://code.visualstudio.com/) or [Atom](https://atom.io/)
- create a folder and open your text editor to that folder (This is where we will do file changes!)

## Introductions!
Tell us about yourself!

- Whats your name?
- What are you learning / working on?
- have you programmed before?


## Overview
The goal of this brief course is to get you comfortable enough to start using git and github with your projects! The best way to learn it is to start using it on your projects outside of this workshop!

at a minimum we should be able to:

- Create a git repo
- understand the git stage cycle
- add changes to the repo
- create repo on github
- push our repo up onto github
- push changes onto github
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
Git is a version conrol system used to track changes in your files. 

why use it:

- undo mistakes & changes
- experiment on branches(a duplicate of your project) 
- use with github to share your work

## What is Github?
Github is a way to store you files tracked with git online.

why use it:

- sharing projects with others
- backup your projects
- great way for companies to see your skillset!


## Git Started:

a few bash(terminal commands)

- `cd` change directory 
- `ls` List 
- `ls -a` List all (even hidden files)

How to exit terminal text editors

- nano `ctr + x` `ctr + o`(save & exit)
- vi/vim `:q`(exit) `:wq`(save & exit)

##### Setup

`git config --global user.email "name@email.com"`
`git config --global user.name "FirstName LastName"`

##### First commit
- `git init`
- `git add .` 
- `git status`
- `git commit -m"Commit Message"`

You just made your first commit!

sometimes you don't want to add every file like the `git add .` command does. Instead you may want to only commit specific files. You can use `git add filename.file` command. replace "filename.file" with the actual name of your file. 

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
`- git diff`
`- git diff --staged`

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





