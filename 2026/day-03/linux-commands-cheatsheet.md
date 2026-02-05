20 commands :

Simple File based commands : 
1. mkdir - makes directory
2. rmdir - removes directory
3. touch a.txt - creates a file
4. rm a.txt - removes a.txt file
5. cp a.txt /devops/savi/demo.txt - copies content of a.txt file to /devops/savi/demo.txt file
6. cd / - changes directory

Process commands :
7. ps - shows all running processes
8. htop - shows all system process but in sequential way where you can scroll between this list.

Service based commands :
9. systemctl status service_name - Checks the service
10. systemctl start service_name - starts the service
11. systemctl enable service_name - starts the service
12. systemctl disable service_name - starts the service
13. systemctl stop service_name - starts the service

Network commands :
14. ping ip - Checks the connectivity of the specific IP mentioned in command
15. ip a - shows IPs mapped to your system
16. curl -v google.com - shows the connectivity/assigned port info.


Disk based commands :
17. lsblk - shows the mount points 
18. df -kh - shows the disk partition with available,used space

Memory based commands :
19. free - shows memory space related details(free/used/available/Swap/total)
20. free -h - shows in units format.
21. vmstat - shows virtual memory statistics.

