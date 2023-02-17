# Cherry-pick
This task has been done in cherry-pick.html and on branch thoughtFix. On main I added a wrong thought and commited, later I checked out in thoughtFix and fixed the thought. Later I added a red container and commited, again I added a blue container and performed commit. To correct the thought in main I cherry picked the commit using it's hash:
```
git checkout main
git cherry-pick ed1f5d7
```
You can see the log history:

![Screenshot from 2023-02-17 10-12-47](https://user-images.githubusercontent.com/124878757/219597881-eff1f447-bbd4-402d-96df-3a75bca568fe.png)

 

Later I cherry picked another commit to add only blue container in main:

In **thoughtFix** branch:

 ![Screenshot from 2023-02-17 11-05-28](https://user-images.githubusercontent.com/124878757/219597973-3a2ccee1-019f-4abd-8cc7-c96f3ec6d17a.png)

In **main** branch:

![Screenshot from 2023-02-17 11-05-41](https://user-images.githubusercontent.com/124878757/219597992-4fc48abb-9b37-4709-9998-fa823688d9c2.png)

Hence, only the blue container was added in main. The workflow for this is shown below:

![Screenshot from 2023-02-17 13-43-04](https://user-images.githubusercontent.com/124878757/219598030-d9008de4-e618-4fde-a6d0-4440fdd54416.png)
