**Challenge Tasks
Task 1: The Problem**

Run a Postgres or MySQL container
Create some data inside it (a table, a few rows — anything)
Stop and remove the container
Run a new one — is your data still there?
Write what happened and why.
**Ans :** Data is not present in the table as this data is not permanently stored in some particular location/place.


**Task 2: Named Volumes**
Create a named volume
Run the same database container, but this time attach the volume to it
Add some data, stop and remove the container
Run a brand new container with the same volume
Is the data still there?
Verify: docker volume ls, docker volume inspect
**Ans :**  Yes, data is still present as we are removing the container & not the volume.


** Task 3: Bind Mounts**
Create a folder on your host machine with an index.html file
Run an Nginx container and bind mount your folder to the Nginx web directory
Access the page in your browser
Edit the index.html on your host — refresh the browser
Write in your notes: What is the difference between a named volume and a bind mount?
**Ans :**  volume stored the data in docker volume but bind mount has its data available in its host.





**Task 4: Docker Networking Basics**
List all Docker networks on your machine
Inspect the default bridge network
Run two containers on the default bridge — can they ping each other by name?
Run two containers on the default bridge — can they ping each other by IP?
**Ans :**  Containers on the same network communicates via IP & not name so they won't be reachable by names.




**Task 5: Custom Networks**
Create a custom bridge network called my-app-net
Run two containers on my-app-net
Can they ping each other by name now?
Write in your notes: Why does custom networking allow name-based communication but the default bridge doesn't?
**Ans :** Containers on custom network can resolve each other by name automatically.



**Task 6: Put It Together**
Create a custom network
Run a database container (MySQL/Postgres) on that network with a volume for data
Run an app container (use any image) on the same network
Verify the app container can reach the database by container name
**Ans :** Terminal output pasted below:
root@3a93b3e52b26:~# 
root@3a93b3e52b26:~# ping mysql-test
PING mysql-test (172.18.0.2) 56(84) bytes of data.
64 bytes from mysql-test.my-app-net (172.18.0.2): icmp_seq=1 ttl=64 time=0.087 ms
64 bytes from mysql-test.my-app-net (172.18.0.2): icmp_seq=2 ttl=64 time=0.048 ms
64 bytes from mysql-test.my-app-net (172.18.0.2): icmp_seq=3 ttl=64 time=0.051 ms
64 bytes from mysql-test.my-app-net (172.18.0.2): icmp_seq=4 ttl=64 time=0.050 ms

64 bytes from mysql-test.my-app-net (172.18.0.2): icmp_seq=5 ttl=64 time=0.048 ms
^C
--- mysql-test ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4113ms
rtt min/avg/max/mdev = 0.048/0.056/0.087/0.015 ms
root@3a93b3e52b26:~# 
root@3a93b3e52b26:~# 
root@3a93b3e52b26:~# exit
exit
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                 NAMES
3a93b3e52b26   ubuntu    "/bin/bash"              21 minutes ago   Up 21 minutes                         linux-test
9182f9a12a96   mysql     "docker-entrypoint.s…"   22 minutes ago   Up 22 minutes   3306/tcp, 33060/tcp   mysql-test
acb609f0a6c4   nginx     "/docker-entrypoint.…"   45 minutes ago   Up 45 minutes   80/tcp                goofy_lovelace
7d1dbbf6335f   nginx     "/docker-entrypoint.…"   47 minutes ago   Up 47 minutes   80/tcp                gallant_nightingale
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$


