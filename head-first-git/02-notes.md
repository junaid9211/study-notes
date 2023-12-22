# Chapter 2: Working with branches
Branches allow you to work on multiple, completely disconnected pieces of work on the same codebase at the same time independently of one another.
A commit represents a point in time, and a branch represents a series of commits.

## The `branch` command
You can create list existing branches, create a branch, rename a branch and delete a branch using `branch` command
- list existing branches `git branch`
- create a new branch `git branch BRANCH-NAME`
- rename a branch `git branch -m NEW-NAME` (renames a branch you are on)
- delete a branch `git branch -d BRANCH-NAME`



## The `switch` command
you can change your current branch using the command `switch`
- to switch to another branch `git switch BRANCH-NAME`
- to create a branch and switch to it in one command use `c` flag `git switch -c BRANCH-NAME` 





