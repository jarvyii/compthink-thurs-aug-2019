# compthink-thurs-aug-2019
A very simple class project to demonstrate branching in get.

Disclaimer: I did not get the time to test the approach I'm following here. I apologize if there are issues.

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
git status

## stage, commit and push your changes 
$ git stage *
$ git commit -m "your message here"  

git may prompt you to login here. Use your git hub credentials.

## Create a pull request
These steps will vary depending on the tools supported by your repo (Like GitHub, VSTS and Azure Dev Ops have web pages for creating pull requests. Additionally, some clients may support creating PRs. Visual Studio has pulgins to assist with creating PRs for both. I think similar plugins exist for git hub.) 

- Go to the repository git hub website (https://github.com/tkdjohn/compthink-thurs-aug-2019.git). 
- Use the branch dropdown to change to your branch.
- Click the New Pull Request button and add comments. 

I have configured this repo to require pull requests to get changes back to the master branch. This is common. Most shops use Pull Requests as part of the workflow to enforce code reviews.  

## Refresh your local repo to see others' changes
$ git checkout master
$ git fetch --prune # see what is different
$ git pull

## Pull Requests & merging demo (time permitting)
This too will vary depending on tools and repo. Visual Studio does a decent job for local merging. Hopefully we won't have any complicated merges. Merging from the cli can be painful if you don't have git configured to use a decent merge tool. (I don't) 

## Professor Tony Buckler

## Mentors:
- John Stokes

## Students:
- Nobody Jones
