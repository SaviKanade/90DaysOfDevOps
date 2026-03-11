**Challenge Tasks
Task 1: GitHub-Hosted Runners**
Create a workflow with 3 jobs, each on a different OS:
ubuntu-latest
windows-latest
macos-latest
In each job, print:
The OS name
The runner's hostname
The current user running the job
Watch all 3 run in parallel
Write in your notes: What is a GitHub-hosted runner? Who manages it?

**ANS **Github actions provide 2 types of runner for each workflow jobs. 1-github hosted & 2-self hosted.
In GitHub hosted provided runners are full managed & maintained by GitHub actions.





**Task 2: Explore What's Pre-installed**
On the ubuntu-latest runner, run a step that prints:
Docker version
Python version
Node version
Git version
Look up the GitHub docs for the full list of pre-installed software on ubuntu-latest
Write in your notes: Why does it matter that runners come with tools pre-installed?

**ANS**It has the flexibility of using different tools on same runner.



**Task 3: Set Up a Self-Hosted Runner**
Go to your GitHub repo → Settings → Actions → Runners → New self-hosted runner
Choose Linux as the OS
Follow the instructions to download and configure the runner on:
Your local machine, OR
A cloud VM (EC2, Utho, or any VPS)
Start the runner — verify it shows as Idle in GitHub
Verify: Your runner appears in the Runners list with a green dot.

**ANS**<img width="1470" height="493" alt="Screenshot 2026-03-11 at 2 03 06 PM" src="https://github.com/user-attachments/assets/61f98c20-ac24-48b8-b085-4db7a35b8b45" />




**Task 4: Use Your Self-Hosted Runner**
Create .github/workflows/self-hosted.yml
Set runs-on: self-hosted
Add steps that:
Print the hostname of the machine (it should be YOUR machine/VM)
Print the working directory
Create a file and verify it exists on your machine after the run
Trigger it and watch it run on your own hardware
Verify: Check your machine — is the file there?

**ANS**<img width="736" height="179" alt="Screenshot 2026-03-11 at 2 10 28 PM" src="https://github.com/user-attachments/assets/f64c419d-41e6-4ae0-8f5d-938ea939f3b4" />
<img width="1467" height="706" alt="Screenshot 2026-03-11 at 2 14 53 PM" src="https://github.com/user-attachments/assets/1411442d-32e8-45e6-aba8-50634031262b" />

File present in self-hosted runner
<img width="1007" height="120" alt="Screenshot 2026-03-11 at 2 12 16 PM" src="https://github.com/user-attachments/assets/1c2c3229-8e00-435f-99f3-f3f7646e91ae" />



Task 5: Labels
Add a label to your self-hosted runner (e.g., my-linux-runner)
Update your workflow to use runs-on: [self-hosted, my-linux-runner]
Trigger it — does it still pick up the job?
Write in your notes: Why are labels useful when you have multiple self-hosted runners?

**ANS**<img width="692" height="58" alt="Screenshot 2026-03-11 at 2 22 01 PM" src="https://github.com/user-attachments/assets/45ed5a25-a71e-4c67-93fd-f1c7df22833b" />
Labels lets a workflow choose the correct runner if we have multiple self-hosted runner.



**Task 6: GitHub-Hosted vs Self-Hosted**
Fill this in your notes:

**ANS**
| Feature | GitHub-Hosted | Self-Hosted |
|--------|---------------|-------------|
| Who manages it | GitHub Actions manages it | You manage and maintain it |
| Cost | Free for public repos, limited minutes for private repos | You pay for your own VM |
| Pre-installed tools | Yes | No |
| Good for | Open source projects | Private/internal workloads, custom environments |
| Security concern | Lower control over environment | More control but you must secure it yourself |
