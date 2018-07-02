# git-from-zero
This is a step-by-step guide for learning most frequently occurring cases with git in a developer life.
## Introduction
When I started to use git it was hard to find well-tried practices. During the years I learned how to use the main and basic functionalities effectively. Of course there can be better or more simply solutions for some cases. Now I'd like to share my knowledge.
## Install git
First you have to install git which is really simple, no matter which OS you are using. You can find proper instructions on the official website:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
## Basic terms
Let's talk about some terms related to version control and git! TODO
## 1. Fork and clone the repo
Our dummy project consists of the chapters of Alice's adventures in Wonderland. Let's fork this repo with the button at the upper right hand corner! After that you have a copy where you can work. If you want to check it, just navigate to your GitHub profile and you can find it under the "Repositories" tab.

You can now clone your own copied repo to your dev machine by using this command in your proper local folder:

```git clone https://github.com/YOUR_GITHUB_USERNAME/git-from-zero.git```

This will actually make a local copy of your remote repo.
## 2. Check status
At this point you are on the **master** branch which you can simply check like this:

```git status```

It also tells you how your stage look like and what kind of uncommited changes you have.

Since here everything is local, each branch should have a representation in the remote repository. These branch-pairs can have different names (I don't recommend it) but the remote one is marked with *origin*. So your local **master** branch is now up-to-date with the remote one: **origin/master**.
## 3. Create your first branch
TODO
## 4. Commit and push
TODO
## 5. Create merge request
TODO
## 6. Pull and fetch
TODO
## 7. Amend and force push
TODO
## 8. Rebase
TODO
## 9. Interactive rebase
TODO
## 10. Stash
TODO
## 11. Go further
TODO
