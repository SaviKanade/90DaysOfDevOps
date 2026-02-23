Task 1: 
Answer in your notes: What authentication methods does gh support?
-> It authenticates your github account with CLI.


Task 2: Working with Repositories
Create a new GitHub repo directly from the terminal — make it public with a README
<img width="1470" height="359" alt="Screenshot 2026-02-23 at 4 34 52 PM" src="https://github.com/user-attachments/assets/11356315-274c-4edb-9fed-f23b354170d9" />


Clone a repo using gh instead of git clone
<img width="895" height="87" alt="Screenshot 2026-02-23 at 4 35 25 PM" src="https://github.com/user-attachments/assets/fc9cc927-e99d-4f2d-90c4-4f4c1b8c7dad" />


View details of one of your repos from the terminal
<img width="1098" height="133" alt="Screenshot 2026-02-23 at 4 42 01 PM" src="https://github.com/user-attachments/assets/9035dcab-cd99-4e2d-99b9-0941ede3caab" />


List all your repositories
<img width="1470" height="269" alt="Screenshot 2026-02-23 at 4 42 26 PM" src="https://github.com/user-attachments/assets/c7bea1bc-eacd-499d-b0ae-15f142589a82" />

Open a repo in your browser directly from the terminal
It doesnot open a repo as I don't have supported application.

Delete the test repo you created (be careful!)
<img width="912" height="106" alt="Screenshot 2026-02-23 at 4 44 50 PM" src="https://github.com/user-attachments/assets/cabe54fa-7e5d-46a2-a7b0-08539e24bcec" />



Task 3:
Answer in your notes: How could you use gh issue in a script or automation?
gh issue can be used inautomation scripts to automatically create, update, or close issues based on deployment status.



Task 4: 
What merge methods does gh pr merge support?
-> gh pr merge supports:
--merge - Creates a merge commit
--squash - Squashes all commits into one
--rebase - Rebases commits onto base branch
These match the merge strategies available on GitHub.

How would you review someone else's PR using gh?
gh pr view <number>
gh pr checkout <number>
gh pr review <number> --comment -b "Looks good overall, please fix minor indentation."
gh pr review <number> --approve
gh pr review <number> --request-changes -b "Please refactor the validation logic."
