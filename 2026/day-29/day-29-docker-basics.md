Day-29 assign



Challenge Tasks
Task 1: What is Docker?
Research and write short notes on:

What is a container and why do we need them?
-> Basically, a container is a virtual environment which has your application.

Containers vs Virtual Machines — what's the real difference?
-> Virtual Machine has allocated storage whereas container have shared storage which can be free once container is removed/deleted. VM has duplicate OS issue, RAM storage issue, system might get slow due to high performance whereas container won't get these issues as OS is handled by docker.

What is the Docker architecture? (daemon, client, images, containers, registry)
-> Deamon - It has background process.
Client - It communicates with docker engine & handles OS.
Images - Its a blueprint which helps to run & execute containers.
Registry - Basically, it registers/logs the containers.


Task 2: Install Docker
Install Docker on your machine (or use a cloud instance)
Verify the installation
Run the hello-world container
Read the output carefully — it explains what just happened
<img width="667" height="493" alt="Screenshot 2026-03-06 at 1 58 22 PM" src="https://github.com/user-attachments/assets/73743a1e-1658-4c19-a21d-222d8e4c0ace" />



Task 3: Run Real Containers
Run an Nginx container and access it in your browser
<img width="1429" height="245" alt="Screenshot 2026-03-06 at 1 50 44 PM" src="https://github.com/user-attachments/assets/a6cc2de7-b6f8-4257-a4f6-b78ea488cccb" />


Run an Ubuntu container in interactive mode — explore it like a mini Linux machine
List all running containers
List all containers (including stopped ones)
Stop and remove a container
->
Stop a container :
<img width="1470" height="427" alt="Screenshot 2026-03-06 at 1 29 19 PM" src="https://github.com/user-attachments/assets/66e46d2b-f33a-4d05-8420-3a9d62f8bd70" />
Remove containers :
<img width="1438" height="896" alt="Screenshot 2026-03-06 at 1 31 16 PM" src="https://github.com/user-attachments/assets/493d7fb5-6ac6-497b-8680-0691ceabd1ff" />


Task 4: Explore
Run a container in detached mode — what's different?
-> It runs a container in the background.

Give a container a custom name 
-> --name demo

Map a port from the container to your host
-> -p host_port:container_port

Check logs of a running container
-> docker logs cont_id
<img width="1344" height="503" alt="Screenshot 2026-03-06 at 1 57 13 PM" src="https://github.com/user-attachments/assets/d618cd7a-7ce4-4110-99f9-0e8f53ec409f" />

Run a command inside a running container
-> docker exec -it cont_id bash


<img width="1417" height="120" alt="Screenshot 2026-03-06 at 1 55 37 PM" src="https://github.com/user-attachments/assets/5ae07c0c-fa80-4610-b914-ac07a3925daa" />




