# Introduction to Git and Github

## Setup

- Have patience. Setting up software tools can be frustrating, but you'll get trough it! 
- Install git
- Create a github account

## Introductions!

## Workshop Goals
get you using git!



## What is Git?

- Why use version control


## What is Github?


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
git reset HEAD filename.file

##### Git Diff
- git diff
- git diff --staged

##### Remove and move
git rm filename.file
git mv filename.file filenamechange.file

##### Disgarding Changes
- `git checkout -- filename.file`

Similarly we can use this command to bring back a deleted file `git checkout -- deletedFileName.file`


##### revert

git revert `cbb60c825aa5b0a1b3c7804de2fe6378c428bfd2`
git revert HEAD

##### Branches
git branch branchname
git checkout branchname



##### merging

link to merge conflicts


## Git out of here!
.gitignore


## Git squashed
Squashing a commit is common in work enviroments

## Git Shared with Github

- `git clone https://github.com/sagecodes/intro-git-github`




## More Resources!

- https://git-scm.com/book/en/v2
- http://sageelliott.com/git-github-commands/
- https://teamtreehouse.com/library/introduction-to-git
- https://git-scm.com/doc
- http://git-school.github.io/visualizing-git/



## Upcoming Events

## Whos taken the workshop:
Use git and github to do a pull request adding your name to the list!

- Sage Elliott



