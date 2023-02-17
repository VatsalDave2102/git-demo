# Rebase
git-rebase - Reapply commits on top of another base tip

This is performed in rebase.html A branch name feature3 was created Screenshot from 2023-02-16 15-56-11 After the initial commit we branched feature3 and commited some code, later I checkout out on main and pulled latest changes then I performed rebase
```
git checkout feature3
git rebase main
```
A merge conflict occured while rebasing that was resolved, then I pushed the main branch. You can see the workflow here.
As you can see rebasing provides clean working tree but also changes the hash of commits
![Screenshot from 2023-02-16 14-30-19](https://user-images.githubusercontent.com/124878757/219596667-60a500cf-3ce0-4293-bd68-1f4f54d3c966.jpg)
