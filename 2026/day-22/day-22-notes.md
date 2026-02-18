**Challenge Tasks**

**Task 1: Install and Configure Git**
Verify Git is installed on your machine
Set up your Git identity — name and email
Verify your configuration
<img width="373" height="79" alt="Screenshot 2026-02-18 at 4 42 15 PM" src="https://github.com/user-attachments/assets/5b9f06c3-8149-4ba7-b649-1ea4ccf21317" />
<img width="1107" height="69" alt="Screenshot 2026-02-18 at 4 43 39 PM" src="https://github.com/user-attachments/assets/412ae8e1-c872-44c8-84c1-b78222200a3a" />
<img width="694" height="179" alt="Screenshot 2026-02-18 at 4 44 31 PM" src="https://github.com/user-attachments/assets/24bd3046-4e44-493a-9782-71fe2d1d59b8" />


**Task 2: Create Your Git Project**
Create a new folder called devops-git-practice
Initialize it as a Git repository
Check the status — read and understand what Git is telling you
Explore the hidden .git/ directory — look at what's inside
<img width="854" height="528" alt="Screenshot 2026-02-18 at 4 52 12 PM" src="https://github.com/user-attachments/assets/c90a2adc-a5d3-4d2d-840f-307f6aa58207" />
git status tells that there is no commitments & as of now the newly repo is empty.


**Task 3: Create Your Git Commands Reference**
Create a file called git-commands.md inside the repo
Add the Git commands you've used so far, organized by category:
Setup & Config
Basic Workflow
Viewing Changes
For each command, write:
What it does (1 line)
An example of how to use it
<img width="668" height="594" alt="Screenshot 2026-02-18 at 5 00 59 PM" src="https://github.com/user-attachments/assets/2cc27d26-42ba-4854-bd9b-525a04dc44dc" />



**Task 4: Stage and Commit**
Stage your file
Check what's staged
Commit with a meaningful message
View your commit history
<img width="893" height="450" alt="Screenshot 2026-02-18 at 5 02 29 PM" src="https://github.com/user-attachments/assets/25dcb628-5fa5-4d14-b721-6d95b02dd65a" />



**Task 5: Make More Changes and Build History**
Edit git-commands.md — add more commands as you discover them
Check what changed since your last commit
Stage and commit again with a different, descriptive message
Repeat this process at least 3 times so you have multiple commits in your history
View the full history in a compact format
<img width="660" height="445" alt="Screenshot 2026-02-18 at 5 15 49 PM" src="https://github.com/user-attachments/assets/0a74591c-895b-4680-bb73-55ac24d6305c" />



**Task 6: Understand the Git Workflow**
Answer these questions in your own words (add them to a day-22-notes.md file):

What is the difference between git add and git commit?
-> git add - Adds the file in staged mode.
git commit - Commit the file in a repo with a message.


What does the staging area do? Why doesn't Git just commit directly?
-> Git won't commit directly as it has some process to commit a file from untracking mode to tracked.
Staging area only adds the file from untracked mode. It doesnot commit the file in repo.


What information does git log show you?
-> It shows all the information regarding your repo such as who has commited (username & email), Head (in which branches changes has been done & i points to the latest branch).


What is the .git/ folder and what happens if you delete it?
-> Git commands won't work & you will have an issue for that directory as your created repo will have no use if .git folder gets delete. 


What is the difference between a working directory, staging area, and repository?
-> Working directory is just a directory which git initiated. But there are no file repos created.
Staging area - only adds the file from untracked mode. It doesnot commit the file in repo. Also, it removes the git added files and again place it in working directory.
Repository - Where we commit our files & have it placed safely so even if it gets removed we can still restore it.
