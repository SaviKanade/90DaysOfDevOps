Challenge Tasks
Task 1: Key-Value Pairs
Create person.yaml that describes yourself with:
Verify: Run cat person.yaml — does it look clean? No tabs?
-> It doesnot look clean with no tabs.
<img width="440" height="138" alt="Screenshot 2026-03-04 at 3 53 26 PM" src="https://github.com/user-attachments/assets/834003c5-8deb-4166-bdba-2e441b82d8a9" />



Task 2: Lists
Add to person.yaml:

tools — a list of 5 DevOps tools you know or are learning
hobbies — a list using the inline format [item1, item2]
Write in your notes: What are the two ways to write a list in YAML?
-> There are 2 ways to define a list :
tools: 
  - docker
  - git
  - github
  - k8s
  - Terraform

hobbies: [dance, learn, sing]
<img width="483" height="255" alt="Screenshot 2026-03-04 at 4 30 51 PM" src="https://github.com/user-attachments/assets/6feea217-f7a9-4b5d-bc5e-fd0a408bfb30" />



Task 3: Nested Objects
Create server.yaml that describes a server:
Verify: Try adding a tab instead of spaces — what happens when you validate it?
-> YAML is indentation-sensitive and requires spaces only. Tabs are not allowed and will cause validation errors.


Task 4: Multi-line Strings
In server.yaml, add a startup_script field using:

The | block style (preserves newlines)
The > fold style (folds into one line)
Write in your notes: When would you use | vs >?
-> | can be used when writing a script or a configuration or a command.
> can be used to write a paragraph.


Task 5: Validate Your YAML
Install yamllint or use an online validator
Validate both your YAML files
Intentionally break the indentation — what error do you get?
Fix it and validate again
-> It gives trailing space error.


Task 6: Spot the Difference
Read both blocks and write what's wrong with the second one:

# Block 1 - correct
name: devops
tools:
  - docker
  - kubernetes
# Block 2 - broken
name: devops
tools:
- docker
  - kubernetes
-> Block2 will give an error due to its indentation.
