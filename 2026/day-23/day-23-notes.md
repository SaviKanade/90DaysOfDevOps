Challenge Tasks
**Task 1: Understanding Branches**

What is a branch in Git?
-> To have your code in safe. Like main branch willl have your main code without affecting that we can create branch.


Why do we use branches instead of committing everything to main?
-> Everytime commiting to the main branch is not a good practice as even for a smaller change we have to commit it so to avoid this risk we can create as many branches as we want. 


What is HEAD in Git?
-> HEAD will give the current branch & git configuration (username/email) details.


What happens to your files when you switch branches?
-> When you switch between branches you cannot see your files/folders which had been created in that branch.



**Task 2: Branching Commands — Hands-On**
In your devops-git-practice repo, perform the following:

Try using git switch to move between branches — how is it different from git checkout?
-> git checkout creates a new branch & switches it to that newly created branch. git switch only helps to switch between branches.



**Task 3: Push to GitHub**
Answer in your notes: What is the difference between origin and upstream?
-> Origin is basically your fork & upstream is your forked repo.  



**Task 4: Pull from GitHub**
Answer in your notes: What is the difference between git fetch and git pull?
-> Git fetch : It updates your branches both local & remote.
Git pull : In short it updates the origin/main branch of remote in local.



**Task 5: Clone vs Fork**
Answer in your notes:
What is the difference between clone and fork?
-> Clone : To access the repo from remote to local we use clone.
Fork : To access the repo from remote to remote.



When would you clone vs fork?
-> Whenever you want to access any repo to your local we should use clone using below command.
$ git clone your_remote_url
If you want to access any other repo from remote then simply you can fork it to your github.


After forking, how do you keep your fork in sync with the original repo?
-> We can keep the update of other repos using 'sync fork' which will synchronise your forked repo.
