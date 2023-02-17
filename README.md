# 5. Drop Commit
git-reset - Reset current HEAD to the specified state

--soft
Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed", as git status would put it.

--mixed
Resets the index but not the working tree (i.e., the changed files are preserved but not marked for commit) and reports what has not been updated. This is the default action.

--hard
Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded. Any untracked files or directories in the way of writing any tracked files are simply deleted.
  
For this I created **dropCommit.html" and a branch named **drop**.
I added a main container and 2 sub container with commits respectively.

![Screenshot from 2023-02-17 11-26-48](https://user-images.githubusercontent.com/124878757/219591033-9a047a0e-8ad1-4abe-8345-d456a6771064.png)

Later I dropped both container using:
```
git reset --hard HEAD^
```
This dropped the sub containers and only main container left.
