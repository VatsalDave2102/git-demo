# git-demo
Demo of Git commands

In repository you'll find different files where different commands are performed

## 1.Merge & Pull
This is performed in **index.html**.
Two branches (**feature1 & feature2**) have been created from main and some commits were done in them. Later we merged them both in **main** branch using:
```
git checkout main
git merge feautre1
git merge feature2
``` 
Here the alphabets were added from **main**, numbers from **feature1** and special characters from **feature2**,
to perform pull I added some more special characters from github and pulled the changes in using
```
git pull
```

![Screenshot from 2023-02-17 12-04-23](https://user-images.githubusercontent.com/124878757/219569446-25188ace-c18b-46b2-aed5-77697a52b189.jpg)

Here you can see the workflow of merging two branches into **main**

![Mergin Branches](https://user-images.githubusercontent.com/124878757/219564370-09661f36-4e63-4a82-ba65-11552d6b9c71.png)
 
## 2.Rebase
This is performed in **rebase.html**
A branch name **feature3** was created
![Screenshot from 2023-02-16 15-56-11](https://user-images.githubusercontent.com/124878757/219576845-b91b73ea-8e71-4794-a069-a6fe9e8870bd.jpg)
After the initial commit we branched **feature3** and commited some code, later I checkout out on **main** and pulled latest changes then I performed rebase
``` 
git checkout feature3
git rebase main
```
A merge conflict occured while rebasing that was resolved, the I pushed the main branch.
You can see the workflow here: 

![Screenshot from 2023-02-16 14-30-19](https://user-images.githubusercontent.com/124878757/219579288-524bb129-8eeb-41d5-af71-f778a2f3ade4.jpg)

As you can see rebasing provides clean working tree but also changes the hash of commits

## 3.Change commit message
This is done in **changeCommit.html** file. I made a commit as you can see below:
![Screenshot from 2023-02-16 16-47-16](https://user-images.githubusercontent.com/124878757/219581111-c1705f7c-3e1f-4c52-9f9d-2fcd8f446714.png)
and then to change commit message I used:
```
git commit --amend -m "message modified"
```
As i had already pushed the commit to remote, I also had to change the message there, and for that I performed:
```
git push --force-with-lease origin main
```
This changes the message of commit in remote too

##4.Cherry-pick
This task has been done in **cherry-pick.html** and on branch **thoughtFix**.
On **main** I added a wrong thought and commited, later I checked out in **thoughtFix** and fixed the thought.
Later I added a red container and commited, again I added a blue container and performed commit.
To correct the thought in main I cherry picked the commit using it's hash:
```
git checkout main
git cherry-pick ed1f5d7
```
You can see the log history:

![Screenshot from 2023-02-17 10-12-47](https://user-images.githubusercontent.com/124878757/219585521-e82861c9-c587-4ab6-a146-3ae224ed7cc3.png)

Later I cherry picked another commit to add only blue container in **main**
 
![Screenshot from 2023-02-17 11-05-41](https://user-images.githubusercontent.com/124878757/219587056-b2afe2a4-aefb-4864-99b7-27ffb143ab5a.png)

Hence, only the blue container was added in **main**. The workflow for this is shown below:

![Screenshot from 2023-02-17 13-43-04](https://user-images.githubusercontent.com/124878757/219589494-8eee89fb-32bb-4de7-99c6-a240e5b3c8f3.png)

## 5. Drop Commit
For this I created **dropCommit.html" and a branch named **drop**.
I added a main container and 2 sub container with commits respectively.

![Screenshot from 2023-02-17 11-26-48](https://user-images.githubusercontent.com/124878757/219591033-9a047a0e-8ad1-4abe-8345-d456a6771064.png)

Later I dropped both container using:
```
git reset --hard HEAD^
```
This dropped the sub containers and only main container left.
