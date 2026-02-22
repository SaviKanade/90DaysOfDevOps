Challenge Tasks
Task 1: 
What is a fast-forward merge?
-> A fast-forward merge happens when the target branch has no new commits, so Git simply moves the branch pointer forward instead of creating a merge commit.


When does Git create a merge commit instead?
-> When both branches have new commits & history is diversed. 


What is a merge conflict? (try creating one intentionally by editing the same line in both branches)
-> A merge conflict occurs when Git cannot automatically decide which changes to keep because the same line was modified in both branches.




Task 2: 
What does rebase actually do to your commits?
-> rebase rewrites the history & makes it linear.


How is the history different from a merge?
-> Merge preserves the history & creates a merge commit but rebase changes the history & makes it linear. 


Why should you never rebase commits that have been pushed and shared with others?
-> As old commits will get replaced.


When would you use rebase vs merge?
-> Merge can be used if we want to merge 1 commited branch into other or collaborate with other branches.
Rebase can be used if we want to change our history & make it linear. 




Task 3: 
What does squash merging do?
-> It combines multiple commits into one clean commit into targeted branch.


When would you use squash merge vs regular merge?
-> Regular merge can be used when you want to preserve the commit history & have the traces of all the changes.
Squash will combine multiple commits into 1 commit which makes commit history clean.


What is the trade-off of squashing?
-> Basically, squash combines multiple commits into 1 so due to this it can affect detailed history of commits. Also, if any issue occurs then it will be difficult to debug.



Task 4: 
What is the difference between git stash pop and git stash apply?
-> git stash pop applies the stash & removes it from stash list.
git stash apply will only apply the last stash from the list & keeps it in the list. 


When would you use stash in a real-world workflow?
-> In a real-world workflow, we may get multiple repos to work on so if we are working on a file & at the same time some error occurs on some other branch then to store those changes we can use stash and do our debugging and come back to resume the work by doing stash pop.




Task 5: 
What does cherry-pick do?
-> Basically, you can pick a commit from another branch to the current branch.


When would you use cherry-pick in a real project?
-> For an instance, lets say we have a script in another branch with only login failure scenarios & that script we want in our main branch then we can use git cherry-pick to have that script in our branch.


What can go wrong with cherry-picking?
-> While doing cherry-picking there should not be any conflict & easily it will work.
