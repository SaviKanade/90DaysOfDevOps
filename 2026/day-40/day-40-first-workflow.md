Look at your workflow file and write in your notes what each key does:

on: When you want to execute your workflow.
jobs: A job is a collection of steps. (code, build, test, deploy)
runs-on: On which server's OS you want to run your job.
steps: Steps of each job.
uses: A pre exist action.
run: Commands.
name: Name of your workflow.



Task 4: Add More Steps
Update hello.yml to also:

Print the current date and time
Print the name of the branch that triggered the run (hint: GitHub provides this as a variable)
List the files in the repo
Print the runner's operating system
Push again — watch the new run.
<img width="1328" height="579" alt="Screenshot 2026-03-04 at 5 06 05 PM" src="https://github.com/user-attachments/assets/fd27215e-ec36-4f50-84f0-b7016e3fc011" />


Task 5: Break It On Purpose
Add a step that runs a command that will fail (e.g., exit 1 or a misspelled command)
Push and observe what happens in the Actions tab
Fix it and push again
Write in your notes: What does a failed pipeline look like? How do you read the error?
-> In the actions tab, it was trying to run my pipeline sequentially and it passed the above steps of conflict step & stopped the execution immediately. It gives error as command not found(I used date command as datess for a conflict). 
<img width="1469" height="470" alt="Screenshot 2026-03-04 at 5 11 21 PM" src="https://github.com/user-attachments/assets/614ef57c-c068-45bc-9043-749e42097cf1" />
<img width="1469" height="829" alt="Screenshot 2026-03-04 at 5 12 10 PM" src="https://github.com/user-attachments/assets/1c20ad3e-37ac-49d1-9d12-e4ca9119b2e3" />


hello.yml workflow :
<img width="818" height="581" alt="Screenshot 2026-03-04 at 5 12 39 PM" src="https://github.com/user-attachments/assets/38a6a269-64a5-4a69-9ebb-3d77e9ac24e0" />
