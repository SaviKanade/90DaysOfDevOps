Task 2: Hello Workflow
Create .github/workflows/hello.yml with a workflow that:

Triggers on every push
Has one job called greet
Runs on ubuntu-latest
Has two steps:
Step 1: Check out the code using actions/checkout
Step 2: Print Hello from GitHub Actions!
Push it. Go to the Actions tab on GitHub and watch it run.

Verify: Is it green? Click into the job and read every step.
-> Yes.


Task 3: Understand the Anatomy
Look at your workflow file and write in your notes what each key does:

on: When you want to execute your workflow.
jobs: Collection of jobs is a workflow.
runs-on: On which runner server OS will this workflow run.
steps: Each job runs based on its steps.
uses: pre-built actions.
run: It can be configuration or commands.
name: Name of the workflow.



Task 4: Add More Steps
Update hello.yml to also:

Print the current date and time
Print the name of the branch that triggered the run (hint: GitHub provides this as a variable)
List the files in the repo
Print the runner's operating system
Push again — watch the new run.

Task 5: Break It On Purpose
Add a step that runs a command that will fail (e.g., exit 1 or a misspelled command)
Push and observe what happens in the Actions tab
Fix it and push again
Write in your notes: What does a failed pipeline look like? How do you read the error?
-> Failed pipeline is marked in red. A pipeline run each job sequentially so when any job gets failed it stops the execution immediately. We can read the error by clicking on the job dropdown.



Snapshot of green run:
<img width="1468" height="698" alt="Screenshot 2026-03-05 at 3 37 44 PM" src="https://github.com/user-attachments/assets/a14c39fd-e9d4-4ed8-b4be-c991e87e9a4f" />
<img width="1470" height="828" alt="Screenshot 2026-03-05 at 3 38 18 PM" src="https://github.com/user-attachments/assets/b96420e6-6d10-4e54-8c4c-23aff8ace561" />

Yaml file:
<img width="808" height="588" alt="Screenshot 2026-03-05 at 3 39 57 PM" src="https://github.com/user-attachments/assets/d21a2eac-63d4-433c-9a03-04defc4b333d" />
