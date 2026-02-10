Day 08 – Cloud Server Setup: Docker, Nginx & Web Deployment

Part 1 :
Launch Cloud Instance & SSH Access

Step 1: Create a Cloud Instance
![Image 06-02-26 at 5 55 PM](https://github.com/user-attachments/assets/04176fae-3d71-4837-813c-c7ae75fc5d32)

Step 2: Connect via SSH
![Image 10-02-26 at 3 50 PM](https://github.com/user-attachments/assets/7bdd0c1f-c3be-4fb8-b297-0e7abd0028fc)


Part 2: 
Install Docker & Nginx 

Step 1: Update System
Step 3: Install Nginx. Verify Nginx is running.

ubuntu@ip-172-31-21-105:~$ 
ubuntu@ip-172-31-21-105:~$ systemctl status nginx.service 
● nginx.service - A high performance web server and a reverse proxy server
     Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; preset: enabled)
     Active: active (running) since Tue 2026-02-10 05:57:35 UTC; 4h 25min ago
       Docs: man:nginx(8)
    Process: 543 ExecStartPre=/usr/sbin/nginx -t -q -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
    Process: 594 ExecStart=/usr/sbin/nginx -g daemon on; master_process on; (code=exited, status=0/SUCCESS)
   Main PID: 612 (nginx)
      Tasks: 3 (limit: 1017)
     Memory: 3.8M (peak: 4.3M)
        CPU: 30ms
     CGroup: /system.slice/nginx.service
             ├─612 "nginx: master process /usr/sbin/nginx -g daemon on; master_process on;"
             ├─613 "nginx: worker process"
             └─614 "nginx: worker process"

Feb 10 05:57:35 ip-172-31-21-105 systemd[1]: Starting nginx.service - A high performance web server and a reverse proxy server...
Feb 10 05:57:35 ip-172-31-21-105 systemd[1]: Started nginx.service - A high performance web server and a reverse proxy server.
ubuntu@ip-172-31-21-105:~$ 



Part 3: 
Security Group Configuration 

Test Web Access: Open browser and visit: http://<your-instance-ip>
You should see the Nginx welcome page!
![Image 06-02-26 at 5 56 PM](https://github.com/user-attachments/assets/09404407-5557-4354-a29b-2e8dd167a661)


Part 4: 
Extract Nginx Logs 

Step 1: View Nginx Logs
Step 2: Save Logs to File
Step 3: Download Log File to Your Local Machine

![Image 10-02-26 at 4 14 PM](https://github.com/user-attachments/assets/43c36efc-3cdd-44f5-8863-f777495d74ba)

