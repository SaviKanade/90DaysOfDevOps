Challenge Tasks
Task 1: Key-Value Pairs
Create person.yaml that describes yourself with:

name
role
experience_years
learning (a boolean)
Verify: Run cat person.yaml — does it look clean? No tabs?
-> It doesnot look clean with no tabs.


Task 2: Lists
Add to person.yaml:

tools — a list of 5 DevOps tools you know or are learning
hobbies — a list using the inline format [item1, item2]
Write in your notes: What are the two ways to write a list in YAML?
-> Below are the 2 ways:
1st way:
tools: docker
 - git
 - github
 - k8s
 - Terraform

2nd way:
hobbies: [dance, learn, sing]



Task 3: Nested Objects
Create server.yaml that describes a server:

server with nested keys: name, ip, port
database with nested keys: host, name, credentials (nested further: user, password)
Verify: Try adding a tab instead of spaces — what happens when you validate it?
-> 


Task 4: Multi-line Strings
In server.yaml, add a startup_script field using:

The | block style (preserves newlines)
The > fold style (folds into one line)
Write in your notes: When would you use | vs >?
-> | used for when we want to write a script.
> can be used to write multiple lines in 1 line.(Like a paragraph)


Task 5: Validate Your YAML
Install yamllint or use an online validator
Validate both your YAML files
Intentionally break the indentation — what error do you get?
Fix it and validate again
-> It gives trailing space error if any indentation is incorrect.
<img width="527" height="266" alt="Screenshot 2026-03-05 at 3 48 15 PM" src="https://github.com/user-attachments/assets/a13f2c5d-d416-4691-832d-996349fa9842" />
<img width="549" height="211" alt="Screenshot 2026-03-05 at 3 51 43 PM" src="https://github.com/user-attachments/assets/389caf0f-1110-4226-a43c-f9d849ad3091" />


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
 
-> Basically, block2 will give an indentation error as '- kubernetes' is not positioned correctly as its a list.



What you learned (3 key points):
- Learned about Github actions.
- yml files indentations & syntaxes.
- How a workflow & its jobs runs. 
