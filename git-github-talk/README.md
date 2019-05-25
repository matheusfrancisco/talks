# Introduction  Git&Github
﻿<img
  src="/img/git.png"
  width="70"
  align="right"
/>

this repository is for a mini workshop taught at Arara's makerspace.

* [Goals](#Goals)
* [Why use git & github](#why-use-git-&-github)
* [Repository](#Repository)
* [Branching](#branching)
* [Merging](#merging)
* [The three states and Areas of Git](#the-three-state-and-areas-of-git)
* [Commands](#commands)

# Goals

- Create a talk about git (araramakertalks)
- learn about git&github
- Create a talk culture
- Date course (25/05/2019)

# Why use Git & GitHub?

* Centralized cloud storage of your code.
* Version Control.
* Working in teams.
* Get involved / Open Source.
* Bettering your code.
* Show off
* You're gonna neet it anyway


# How to learn Git

15 minutes is all it takes to learn the basics of Git. Here’s an awesome (free!) interactive tutorial sponsored by GitHub where you can learn all of the basics: try.github.io

# What is Git?

Version control system are a category of software tools that help a software team manage changes to source code over time. 

Software developers working in teams are continually writing new source code and changing existing source code.

Version control systems are all about managing contributions between multiple distributed authors ( usually developers ). 

is a distributed version control system, used mainly in software development, but can be used to record the history of edits of any file type . Git was originally designed and developed by Linus Torvalds for Linux kernel development, but was adopted by many other projects.


# Repository 

A repository, or Git project, encompasses the entire collection of files and folders associated with a project, along with each file’s revision history. The file history appears as snapshots in time called commits, and the commits exist as a linked-list relationship, and can be organized into multiple lines of development called branches. 

Because Git is a DVCS, repositories are self-contained units and anyone who owns a copy of the repository can access the entire codebase and its history. Using the command line or other ease-of-use interfaces, a git repository also allows for: interaction with the history, cloning, creating branches, committing, merging, comparing changes across versions of code, and more.  

Working in repositories keeps development projects organized and protected. Developers are encouraged to fix bugs, or create fresh features, without fear of derailing mainline development efforts. Git facilitates this through the use of topic branches: lightweight pointers to commits in history that can be easily created and deprecated when no longer needed.  Through platforms like GitHub, Git also provides more opportunities for project transparency and collaboration. Public repositories help teams work together to build the best possible final product.

### Create a repository
```
git init
```

# Branching 

This document is an in-depth review of the git branch command and a discussion of the overall Git branching model. Branching is a feature available in most modern version control systems. Branching in other VCS's can be an expensive operation in both time and disk space. In Git, branches are a part of your everyday development process. Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes. This makes it harder for unstable code to get merged into the main code base, and it gives you the chance to clean up your future's history before merging it into the main branch.


# Merging

Merging is Git's way of putting a forked history back together again. The git merge command lets you take the independent lines of development created by git branch and integrate them into a single branch.

Note that all of the commands presented below merge into the current branch. The current branch will be updated to reflect the merge, but the target branch will be completely unaffected. Again, this means that git merge is often used in conjunction with git checkout for selecting the current branch and git branch -d for deleting the obsolete target branch.

# Understanding merge conflicts

Merging and conflicts are a common part of the Git experience. Conflicts in other version control tools like SVN can be costly and time-consuming. Git makes merging super easy. Most of the time, Git will figure out how to automatically integrate new changes.

Conflicts generally arise when two people have changed the same lines in a file, or if one developer deleted a file while another developer was modifying it. In these cases, Git cannot automatically determine what is correct. Conflicts only affect the developer conducting the merge, the rest of the team is unaware of the conflict. Git will mark the file as being conflicted and halt the merging process. It is then the developers' responsibility to resolve the conflict.

## Create a merge conflicts

```
$ mkdir git-merge-test
$ cd git-merge-test
$ git init .
$ echo "this is some content to mess with" > merge.txt
$ git add merge.txt
$ git commit -am"we are commiting the inital content"
[master (root-commit) d48e74c] we are commiting the inital content
1 file changed, 1 insertion(+)
create mode 100644 merge.txt

$ git checkout -b new_branch_to_merge_later
$ echo "totally different content to merge later" > merge.txt
$ git commit -am"edited the content of merge.txt to cause a conflict"
[new_branch_to_merge_later 6282319] edited the content of merge.txt to cause a conflict
1 file changed, 1 insertion(+), 1 deletion(-)

git checkout master
Switched to branch 'master'
echo "content to append" >> merge.txt
git commit -am"appended content to merge.txt"
[master 24fbe3c] appended content to merge.tx
1 file changed, 1 insertion(+)

git merge new_branch_to_merge_later
Auto-merging merge.txt
CONFLICT (content): Merge conflict in merge.txt
Automatic merge failed; fix conflicts and then commit the result.
```

# The three states and Areas of Git

In order to fully understand Git, we have view our files how Git does. Envisioning what states your files are in will allow you to quickly pick up on the Git commands. Git views all files in three ways:

* committed
* modified/untracked
* staged

### 1) Modified/Untracked and your Working Directory
Git views untracked and modified files similarly. Untracked means that the file is new to your Git project. Modified means that the file has been seen before, but has been changed, so is not ready to be snapshotted by Git. Modification of a file occurs in your working directory.


###  Staged and Staging Area

When a file becomes staged, it's taken into the staging area. This is where Git is able to take a snapshot of it and store its current state to your local repository. This area is also known as the Index.


### Committed and the Git Directory

Committed means that Git has officially taken a snapshot of the files in the staging area, and stored a unique index in the Git directory. The terms snapshotted and committed are very similar. The significance of being committed is that you can now revert back to this project's current state at any time in the future.
The term for the very last snapshot you've made for commitment is known as the HEAD.
It's very important to understand the three states of a file, and the three areas they live in! If you have a good handle on these concepts, the rest of Git fundamentals should be a cinch!





# Git commands..
Commands show in workshop  git commands.md [here](/git-commands.md)





........... in construction.


## Picture workshop..
........... in construction.

## Slide

........... in construction.
### References

https://es.atlassian.com/git/tutorials/

https://www.atlassian.com/git/tutorials/using-branches/git-merge

https://git-scm.com/book/pt-br/v1/Ramificação-Branching-no-Git-Básico-de-Branch-e-Merge

https://git-scm.com/docs/git-merge

https://opensource.com/article/18/5/git-branching

