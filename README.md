# compthink-thurs-aug-2019
A very simple class project to demonstrate branching in get.

Disclaimer: I did not get the time to test the approach I'm following here. I apologize if there are issues.
## Professor Tony Buckler

## Mentors:
- John Stokes

## Students:
- Nobody Jones



## a simple tutorial of branching on GitHub
https://guides.github.com/activities/hello-world/

## What is a branch?
- It is NOT a copy of your code. 
- But you can think of it that way!
- A more in depth (but still basic) discussion of branching: https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
- branching methodologies vary based on work flow 
- two popular branching methodologies are gitflow and mainline (aka trunk) branching (outside today's discussion - google them if your are interested)

## clone an existing repo
$ git clone https://github.com/tkdjohn/compthink-thurs-aug-2019.git

## change branches locally
$ git checkout <tab>

## create and checkout a new branch
$ git checkout -b iss53
Switched to a new branch "iss53"
This is shorthand for:

$ git branch iss53
$ git checkout iss53

## see what's changed
$ git status

## stage, commit and push your changes 
$ git stage *  #you can stage one or more files as necessary, but typically you want to stage all changes
$ git commit -m "your message here"  

git may prompt you to login here. Use your git hub credentials.

## Create a pull request
These steps will vary depending on the tools supported by your repo (Like GitHub, VSTS and Azure Dev Ops have web pages for creating pull requests. Additionally, some clients may support creating PRs. Visual Studio has pulgins to assist with creating PRs for both. I think similar plugins exist for git hub.) 

- Go to the repository git hub website (https://github.com/tkdjohn/compthink-thurs-aug-2019.git). 
- Use the branch dropdown to change to your branch.
- Click the New Pull Request button and add comments. 

I have configured this repo to require pull requests to get changes back to the master branch. This is common. Most shops use Pull Requests as part of the workflow to enforce code reviews.  

## Refresh your local repo to see others' changes
$ git checkout master    # change to master branch
$ git fetch --prune      # see what is different
$ git pull               # actually get teh changes

## Pull Requests & merging demo (time permitting)
This too will vary depending on tools and repo. Visual Studio does a decent job for local merging. Hopefully we won't have any complicated merges. Merging from the cli can be painful if you don't have git configured to use a decent merge tool. (I don't) 

## I was in the middle of a change that I don't want to commit, but i need to change branches!!
$ git stash 
$ git stash -drop #removes the stash 
$ get stash -pop #retrieves the stash and then removes it

Typically, unless my changes break the build, I'll go ahead and commit changes when I need to switch branches. But I won't always push them to the remote. 

## OOPS I did it again - I made a mistake (fixing mistakes after commit - time permitting)
- if not committed, just fix it and go on
- if the mistake is committed but not pushed - several possibilities
  - remove the commit (Google git reset ) This can cause you to lose uncommitted changes (see git stash for a way to avoid this)
  - if really really bad, you can always delete your local repo and clone it again. (note you can clone the same repo to different directories too!)
- if the mistake committed and pushed (these can work for unpushed commits with mistakes too) 
  - others may have a copy of your mistake! Therefore you can't delete the commit!
  - stash any changes in progress then fix the problem and commit/push the fix 
  - but you can do a revert on that commit (A revert makes a NEW commit that undoes the changes in another commit) seek assistance with this the first time you try it!

## Protip: if you use git Hub regularly, the Octotree plugin for Chrome is a must have
https://chrome.google.com/webstore/detail/octotree/bkhaagjahfmjljalopjnoealnfndnagc?hl=en-US
