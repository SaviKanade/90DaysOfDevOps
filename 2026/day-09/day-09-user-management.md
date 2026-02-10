Day 09 Challenge
Users & Groups Created
* Users: tokyo, berlin, professor, nairobi
* Groups: developers, admins, project-team

Group Assignments
developers = tokyo,berlin 
admins = berlin,professor project-team = tokyo,nairobi

Directories Created :
/opt/dev-project 
/opt/team-workspace


Commands Used :
Task 1 : 
sudo useradd -m tokyo -p tokyo123 
sudo useradd -m berlin -p b123 
sudo useradd -m professor -p prof123 
ll /home/ 
![Image 10-02-26 at 12 22 PM](https://github.com/user-attachments/assets/e15b7e11-7bf1-443f-9283-98a9525d2795)
￼
cat /etc/passwd 
![Image 10-02-26 at 12 23 PM](https://github.com/user-attachments/assets/fcc4610e-2596-48ba-b940-ee934ec16e44)


Task 2 : 
sudo groupadd developers 
sudo groupadd admins 
cat /etc/group
![Image 10-02-26 at 12 24 PM](https://github.com/user-attachments/assets/579d526f-ac05-47da-8c10-89e0dcc870a2)




Task 3 : 
sudo gpasswd -a tokyo developers 
sudo usermod -aG developers,admins berlin 
sudo gpasswd -a professor admins 
cat /etc/group
![Image 10-02-26 at 12 30 PM](https://github.com/user-attachments/assets/834fbe6c-9646-45db-9624-dcf09c06d45e)



Task 4 : 
sudo mkdir -p /opt/dev-project 
sudo chown :developers /opt/dev-project/ 
sudo chmod 775 /opt/dev-project 
su - tokyo -p tokyo123 
$ pwd /home/tokyo 
$ cd /opt/dev-project 
$ pwd /opt/dev-project 
$ touch abc.txt 
$ ls abc.txt $ exit
su - berlin -p b123 
$ pwd /home/berlin 
$ cd /opt/dev-project 
$ pwd /opt/dev-project 
$ touch test1.txt 
$ ls abc.txt test1.txt 
$ exit

Tried with 3rd user as well to check permission denied working fine or not. It will deny because professor is not added in group developers.
su - professor -p prof123 
$ pwd /home/professor 
$ cd /opt/dev-project 
$ pwd /opt/dev-project 
$ ls abc.txt test1.txt 
$ touch t2.txt 
touch: cannot touch 't2.txt': Permission denied 
$ exit


Task 5 : 
sudo useradd -m nairobi -p n123 
sudo groupadd project-team sudo gpasswd -a nairobi project-team 
sudo gpasswd -a tokyo project-team 
sudo mkdir -p /opt/team-workspace 
sudo chown :project-team /opt/team-workspace 
sudo chmod 775 /opt/team-workspace 
su - nairobi -p n123 
$ pwd /home/nairobi 
$ cd /opt/team-workspace 
$ pwd /opt/team-workspace 
$ touch test2.txt 
$ ls test2.txt 
$ exit

Final snapshot of all groups with its members : 
![Image 10-02-26 at 3 48 PM](https://github.com/user-attachments/assets/34a41195-7260-4628-8af3-336b016a7a48)
￼


What I Learned
1. How we can assign members to groups & how we can give permissions as per particular requirement.
2. Got to know how we can add multiple users to group & vice-a-versa.


