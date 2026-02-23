Challenge Tasks

Task 1: 
What is the difference between --soft, --mixed, and --hard?
-> Soft reset : It removes the commit from its history & keeps the file in staged mode which is ready to commit.
Mixed reset : It removes the commit from its history & keeps the file in unstaged mode(git add) which is not ready to commit.
Hard reset : It removes the commit from its history & even from working tree.


Which one is destructive and why?
-> Hard reset is the destructive as it totally removes your commit.


When would you use each one?
-> Soft reset : Now, if by mistake if you have done any commit and want to remove it then you can use soft reset.
Mixed reset : If you want to remove the commit from history & unstage changes for editing. 
Hard reset : If you have done any wrong changes in the file/script & commited it then you can use mixed reset which removes the commit from history & made your file available to edit. 


Should you ever use git reset on commits that are already pushed?
-> No, we cannot use git reset after it being pushed.



Task 2: 
How is git revert different from git reset?
-> git revert reverts your changes but keeps it in history whereas git reset removes it from history. 


Why is revert considered safer than reset for shared branches?
-> Because it doesnot make any changes/edits/modifys your commit history. It only reverts your file/script.


When would you use revert vs reset?
-> Revert : We can use it when commit has already been pushed.You’re working on a shared branch (like main). You want a safe rollback. You don’t want to rewrite history
Reset : The commit has NOT been pushed. You’re working locally. You want to clean up or modify commit history. You want to squash or edit commits before pushing




Task 3: Reset vs Revert — Summary
Create a comparison in your notes:

                                                git reset	                                                      git revert
What it does	                      It does not remove the commit from history.     It does not remove the commit from history   
Removes commit from history?           Yes                                                               No  
Safe for shared/pushed branches?	      No                                                               Yes
When to use	?	?                     When you want to remove the commit from         When you safely want to revert your changes without affecting your history. 
                                          history.




Task 4: Branching Strategies
Research the following branching strategies and document each in your notes with:

How it works (short description)
A simple diagram or flow (text-based is fine)
When/where it's used
Pros and cons
![IMG_8362](https://github.com/user-attachments/assets/9b11acc3-7f30-40a1-9231-1a9b3c12bb07)



GitFlow — develop, feature, release, hotfix branches
GitHub Flow — simple, single main branch + feature branches
Trunk-Based Development — everyone commits to main, short-lived branches

Answer:
Which strategy would you use for a startup shipping fast?
-> Trunk-Based Development

Which strategy would you use for a large team with scheduled releases?
-> GitFlow  — develop, feature, release, hotfix branches

Which one does your favorite open-source project use? (check any repo on GitHub)
-> GitFlow or GitHub Flow
