What to Review (pick at least one per section)

* Mindset & plan: revisit your Day 01 learning plan—are your goals still right? any tweaks?
-> Yes, goal is still correct. Infact seems like moving closer towards my goal.

* Processes & services: rerun 2 commands from Day 04/05 (e.g., ps, systemctl status, journalctl -u <service>); jot what you observed today.
-> Basically, we can able to see the new logs everyday for particular services as per the system behaviour. 

* File skills: practice 3 quick ops from Days 06–11 (e.g., echo >>, chmod, chown, ls -l, cp, mkdir).

* Cheat sheet refresh: skim your Day 03 commands—highlight 5 you’d reach for first in an incident.
-> free -h - shows free space
  ping - shows connectivity
  ip a - gives server's IP

* User/group sanity: recreate one small scenario from Day 09 or Day 11 (create a user or change ownership) and verify with id/ls -l.
Mini Self-Check (write short answers in day-12-revision.md)
-> Created a user then created a file & assigned permission of read & write but not execute. Created group & added user in that group. Verified the id of that user.

1. Which 3 commands save you the most time right now, and why?
-> ls -lR : It gives more detailed view/permissions of files under this directory which is quite easy to check.
   sudo usermod -aG group1,group2,group3 user1 : We can add a user in multiple groups at a time.
   scp -i destination_server_username@ip:dest_path source_path : This command is quite easy to understand as we can copy files from source to destination.
   
2. How do you check if a service is healthy? List the exact 2–3 commands you’d run first.
-> free -h, lsblk, df -h
   
3. How do you safely change ownership and permissions without breaking access? Give one example command.
-> By using -R we can change ownership & permissions.
   
4. What will you focus on improving in the next 3 days?
-> How to check usage of CPU/Memory as numbering is quite hard for me. 
