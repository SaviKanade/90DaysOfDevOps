Challenge Tasks
Task 1: The Problem
Think about a team of 5 developers all pushing code to the same repo manually deploying to production.

Write in your notes:

What can go wrong?
-> Directlt deploying to production is not a good practice.

What does "it works on my machine" mean and why is it a real problem?
-> It means the code which has been deployed & build my machine may not work on any other machine due to its resources/different OS/storage.

How many times a day can a team safely deploy manually?
-> Manual deployment can be done 1-2 times only if something is very cruisal & it cannot be run automatically at that time. Best practice to not deploy manually.



Task 2: CI vs CD
Research and write short definitions (2-3 lines each):

Continuous Integration — what happens, how often, what it catches :
-> Whenever a code is changed CI will automatically build & test it once its pushed to the repo.
on: 
  push:
    branches: [main]

Continuous Delivery — how it's different from CI, what "delivery" means :
-> CI works on automatic functionality whereas Continous Delivery works manually. Means the code is ready to deploy but it waits for an approval.
on: workflow_dispatch

Continuous Deployment — how it differs from Delivery, when teams use it :
-> Basically, delivery can be scheduled on a specific time whereas deployment can be run immediately. Team can Continous Deployment when they want to deploy their app immediately.


Write one real-world example for each.
Continuous Integration :
Designers frequently add new clothing designs to a shared system where they are automatically checked for errors before being accepted.

Continuous Delivery :
A clothing factory produces finished clothes and keeps them packed in boxes ready for shipping. However, the shop owner must approve before the clothes are sent to the store.

Continous Deployment :
A clothing factory automatically sends newly produced clothes to the store shelves as soon as they pass quality checks, without waiting for any manager’s approval.




A pipeline has these parts — write what each one does:

Trigger — what starts the pipeline
It triggers the pipeline on when condition.
Stage — a logical phase (build, test, deploy)
Job — a unit of work inside a stage
A job is a set of steps that run on a runner.
Step — a single command or action inside a job
Steps can be commands/configuration or a pre-built action.
Runner — the machine that executes the job
Each job needs a runner. In github there 2 types of runners : github hosted & self hosted.
Artifact — output produced by a job


Task 4: Draw a Pipeline
Draw a CI/CD pipeline for this scenario:

A developer pushes code to GitHub. The app is tested, built into a Docker image, and deployed to a staging server.

Include at least 3 stages. Hand-drawn and photographed is perfectly fine.
![IMG_8425](https://github.com/user-attachments/assets/0fbfa8a4-3cce-42bd-bef4-1876692307b4)



Task 5: Explore in the Wild
Open any popular open-source repo on GitHub (Kubernetes, React, FastAPI — pick one you know)
Find their .github/workflows/ folder
Open one workflow YAML file
Write in your notes:
What triggers it?
-> It triggers on pull request or when an issue is opened or reopened.

How many jobs does it have?
-> only 1 i.e. add-to-project

What does it do? (best guess)
-> It adds new issues to the project using github token to authenticate.

fastapi -> add-to-project.yml file:

name: Add to Project

on:
  pull_request_target:
  issues:
    types:
      - opened
      - reopened

jobs:
  add-to-project:
    name: Add to project
    runs-on: ubuntu-latest
    steps:
      - uses: actions/add-to-project@v1.0.2
        with:
          project-url: https://github.com/orgs/fastapi/projects/2
          github-token: ${{ secrets.PROJECTS_TOKEN }}

