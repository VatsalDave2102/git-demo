# Merge & Pull

git-merge - Join two or more development histories together.
Incorporates changes from the named commits (since the time their histories diverged from the current branch) into the current branch. This command is used by git pull to incorporate changes from another repository and can be used by hand to merge changes from one branch into another.

This is performed in index.html. Two branches (feature1 & feature2) have been created from main and some commits were done in them. Later we merged them both in main branch using:
```
git checkout main
git merge feautre1
git merge feature2
```
Here the alphabets were added from main, numbers from feature1 and special characters from feature2, to perform pull I added some more special characters from github and pulled the changes in using
```
git pull

```
![Screenshot from 2023-02-16 14-26-00](https://user-images.githubusercontent.com/124878757/219595375-3218b9af-783f-4f5a-8399-eb63a8a327ba.png)

Here you can see the workflow of merging two branches into main

![Screenshot from 2023-02-16 13-04-12](https://user-images.githubusercontent.com/124878757/219595284-47a9dafb-20c9-4b90-b25f-3a7264f39d23.png)
