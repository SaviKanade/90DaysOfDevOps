# Day 11 Challenge

## Files & Directories Created
-->Files :
devops-file.txt
team-notes.txt
project-config.yaml
gold.txt
stratergy.conf
access-codes.txt
blueprints.pdf
escape-plan.txt


-->Folders :
app-logs
heist-project
vault
plans
bank-heist


## Ownership Changes
devops-file.txt : user:group - ubuntu:ubuntu -> tokyo:ubuntu -> berlin:ubuntu
team-notes : user:group - ubuntu:ubuntu -> ubuntu:heist-team
project-config.yaml : user:group - ubuntu:ubuntu -> professor:heist-team 
app-log : user:group - ubuntu:ubuntu -> berlin:heist-team
heist-project : user:group - ubuntu:ubuntu -> professor:planner
access-codes.txt : user:group - ubuntu:ubuntu -> tokyo:vault-team
blueprints.pdf : user:group - ubuntu:ubuntu -> berlin:tech-team
escape-plan.txt : user:group - ubuntu:ubuntu -> nairobi:vault-team



## Commands Used
Task 1 :
ls -l /home/ubuntu
Note : All files/folders are owned by my ubuntu user.
Owner is the user who creates the file/folder.
Group is nothing but members of owners/users.

Snapshot :
![Image 10-02-26 at 5 05 PM](https://github.com/user-attachments/assets/4583d9cc-77e7-4e6b-97fb-dd34dde9378e)



Task 2 :
touch devops-file.txt
ls -l devops-file.txt
sudo chown tokyo devops-file.txt
ls -l devops-file.txt
sudo chown berlin devops-file.txt 
ls -l devops-file.txt

Snapshot :
![Image 10-02-26 at 4 29 PM](https://github.com/user-attachments/assets/41673471-7f39-46ab-83c7-9e6c3daee928)



Task 3 :

touch team-notes.txt
ls -l team-notes.txt 
sudo groupadd heist-team
sudo groupadd heist-team
sudo chown :heist-team team-notes.txt 
ls -l team-notes.txt 

Snapshot :
![Image 10-02-26 at 4 30 PM](https://github.com/user-attachments/assets/a063a7ee-5829-4a0d-8221-8731aaacbcac)



Task 4 :
touch project-config.yaml
ls -l project-config.yaml 
sudo chown professor:heist-team project-config.yaml 
mkdir -p app-logs
sudo chown berlin:heist-team app-logs/

Snapshot :
![Image 10-02-26 at 4 37 PM](https://github.com/user-attachments/assets/87bb6be3-9f18-489a-bcc0-ac4f9f4f5881)


Task 5 :
mkdir -p heist-project/vault
mkdir -p heist-project/plans
touch heist-project/vault/gold.txt
touch heist-project/plans/strategy.conf
sudo groupadd planners
cat /etc/group | grep planners
ls -lR heist-project/
sudo chown -R professor:planners heist-project/

Snapshot :
![Image 10-02-26 at 4 45 PM](https://github.com/user-attachments/assets/cb18b222-83b5-48b0-90f3-6b55f2d00ba5)


Task 6 :
sudo groupadd vault-team
sudo groupadd tech-team
mkdir -p bank-heist
touch bank-heist/access-codes.txt
touch bank-heist/blueprints.pdf
touch bank-heist/escape-plan.txt
cat /etc/group | grep team
ls -lR bank-heist/
ls -l | grep bank
sudo chown tokyo:vault-team bank-heist/access-codes.txt 
sudo chown berlin:tech-team bank-heist/blueprints.pdf 
sudo chown nairobi:vault-team bank-heist/escape-plan.txt 
ls -lR bank-heist/

Snapshot :
![Image 10-02-26 at 4 53 PM](https://github.com/user-attachments/assets/1aea6e90-c1ab-4f18-af2f-a90b25bb383d)


## What I Learned
1. Learned about the directory permission flow.
2. How groups are assigned to particular file or folder's group.
3. Leanred about how to give owner & group permission seperately to a file/folder and even with both.
