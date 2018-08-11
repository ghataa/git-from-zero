# git-from-zero
This is a step-by-step guide for learning most frequently occurring cases with git in a developer life.
## Introduction
When I started to use git it was hard to find well-tried practices. During the years I learned how to use the main and basic functionalities effectively. Of course there can be better or more simply solutions for some cases. Now I'd like to share my knowledge.
## Install git
First you have to install git which is really simple, no matter which OS you are using. You can find proper instructions on the official website:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
## Basic terms
Let's talk about some terms related to version control and git! TODO
## 1. Fork and clone the repo | git clone [url]
Our dummy project consists of the chapters of Alice's adventures in Wonderland. Let's fork this repo with the button at the upper right hand corner! After that you have a copy where you can work. If you want to check it, just navigate to your GitHub profile and you can find it under the "Repositories" tab.

You can now clone your own copied repo to your dev machine by using this command in your proper local folder:

```git clone https://github.com/YOUR_GITHUB_USERNAME/git-from-zero.git```

This will actually make a local copy of your remote repo.
## 2. Check status | git status
At this point you are on the **master** branch which you can simply check like this:

```git status```

It also tells you how your stage look like and what kind of uncommited changes you have.

Since here everything is local, each branch should have a representation in the remote repository. These branch-pairs can have different names (I don't recommend it) but the remote one is marked with *origin*. So your local **master** branch is now up-to-date with the remote one: **origin/master**.
## 3. Create your first branch | git checkout -b [new-branch-name]
Since you work together with others on the same project, it's recommended to use separate branches for your tasks. Here you can do whatever you just want, it won't affect others. If you finished with your task, you can just simply merge your branch into the main one. What you should keep in mind: keep your main branch always consistent! It shouldn't contain half finished solutions.

So we are now on the **master** which is the main branch of our project. Let's say we noticed a bug and have to change the title of chapter 2. First, create your own brach:

```git checkout -b my-first-branch```

You can do your work now, change the title from "The Pool of T" to "The Pool of Tears"! If you fixed the bug, you can check what did you modified exactly:

```git diff```
## 4. Stage and commit | git add [file_name] | git commit -m "[title]"
If you check the status now, you can see that *project/chapter_2.txt* was modified. First we have to add all of our changes to the stage otherwise they won't be commited:

```git add project/chapter_2.txt```

Note: If you have more than one modified files and you want to stage all of them, you can do it simply like this:

```git add .```

Let's check the status again! Git says "changes to be committed" so our modifications are ready for commit:

```git commit -m "Fix second chapter's bug" -m "Optional description comes here"```

The first "-m" option is mandatory and you can specify the title of commit with that. It is recommended not to use long titles: 50-60 characters should be enough! Title should explain WHAT does the given commit instead of HOW! For example "Fix XY crash" instead of "Check if XY object is null". The second "-m" is optional. If you want to add more detail what these changes do, you can specify it here.
## 5. Push | git push
Commiting your changes will "save" your work in a separate state. BUT your commit exists only on your dev-machine, locally for now. If you want to share with others and/or keep it in a safe place, you have to **push** it to your remote repository. This will make your remote branch uptodate with the local one:

```git push```

Oops, it doesn't work! Git says: "fatal: The current branch my-first-branch has no upstream branch." This is because we tried to push changes to a non-existing remote branch. We have to create it first with the "--set-upstream" tag:

```git push --set-upstream origin my-first-branch```

After "--set-upstream" tag you have to specify the name of the remote branch. It could be different from the local one but it's not recommended.

Upcoming commits can be pushed now in the normal way as we tried before.

## 6. Create merge request
Since we fixed the given issue, we want to share it with others. Or in other words, we want to present our changes on the **master** branch. The solution is simple, we just have to merge our branch into the **master**. Do it simply with GitHub's GUI:

- open your remote repo in GitHub
- click on *Pull requests*
- click on *New pull request* button
- "base" should be the **master**
- "compare" should be your working banch
- click on *Create pull request* button
- add a short, informative title
- description can contain screenshots and/or videos to give more detail about your changes
- add a reviewer who will check your work before merging it to the **master**
- click on *Create pull request* button

Your merge request (or as GitHub says, pull request) is open now and you can check it under the *Pull requests* tab. The merge request's details screen opens with the *Conversations* tab by deafault where you can find your reviewer's comments. You can start a conversation under each comment and you can fix the remark if necessary.

You can also check the *Files changed* tab where you can find what will be changed exactly when your request is accepted.

We can now accept it so just simply click on the *Merge pull request* button!
## 7. Checkout and Pull | git checkout [branch_name] | git pull
We just finished fixing a bug and now want to work on a new task. Our current branch is **my-first-branch**, so let's go to the **master** first:

```git checkout master```

Let's check the git history of **master**:

```git log```

This command lists commits on the current branch where the latest is the first. As you can see, there is no commit with title of "Fix second chapter's bug" though we already merged it to the **master**. This is because your local **master** doesn't contain this modification yet but the remote one! Let's refresh it:

```git pull```

This command pulls the current branch and make it uptodate with the remote one.
## 8. Amend and force push
TODO
## 9. Fetch and Rebase
TODO
## 10. Interactive rebase
TODO
## 11. Delete branch
TODO
## 12. Stash
TODO
## 13. Go further
TODO
## 14. Summary
TODO
