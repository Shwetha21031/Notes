
## Git Branches
Branches in Git are incredibly lightweight as well. 
They are simply pointers to a specific commit -- nothing more. 
Because there is no storage / memory overhead with making many branches, it's easier to logically divide up your work than have big beefy branches.

# Combining work

## 1. git merge
## 2. git Rebase
Rebasing essentially takes a set of commits, "copies" them, and plops them down somewhere else.
the advantage of rebasing is that it can be used to make a nice linear sequence of commits. The commit log / history of the repository will be a lot cleaner if only rebasing is allowed.


## HEAD
First we have to talk about "HEAD". HEAD is the symbolic name for the currently checked out commit -- it's essentially what commit you're working on top of.
HEAD always points to the most recent commit which is reflected in the working tree. Most git commands which make changes to the working tree will start by changing HEAD.
Normally HEAD points to a branch name (like bugFix). When you commit, the status of bugFix is altered and this change is visible through HEAD.