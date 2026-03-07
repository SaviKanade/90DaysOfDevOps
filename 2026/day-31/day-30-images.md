Challenge Tasks
Task 1: Docker Images
Pull the nginx, ubuntu, and alpine images from Docker Hub
<img width="953" height="176" alt="Screenshot 2026-03-07 at 12 54 20 PM" src="https://github.com/user-attachments/assets/e7c51af9-34f7-4e48-8a9f-34e489b24418" />

List all images on your machine — note the sizes
<img width="767" height="228" alt="Screenshot 2026-03-07 at 12 54 41 PM" src="https://github.com/user-attachments/assets/fe5ea323-a592-452b-a827-ab2be67475ec" />

Compare ubuntu vs alpine — why is one much smaller?
Alpine is smaller because its created to build & test container with smaller sizes. Alpine is a lightweight image.

Inspect an image — what information can you see?
<img width="1236" height="853" alt="Screenshot 2026-03-07 at 12 56 20 PM" src="https://github.com/user-attachments/assets/eb1f1014-5fd1-4ba9-9530-8eb055111b3f" />

Remove an image you no longer need
<img width="906" height="601" alt="Screenshot 2026-03-07 at 12 58 02 PM" src="https://github.com/user-attachments/assets/bd3c27d3-ad78-4ad2-81ef-f62fa5bd9ae4" />



Task 2: Image Layers
Run docker image history nginx — what do you see?
<img width="1121" height="389" alt="Screenshot 2026-03-07 at 12 58 35 PM" src="https://github.com/user-attachments/assets/158144eb-b3cd-4821-93eb-d62b341ea3dc" />
It shows all the actions performed on nginx image like its creation date/time, port mapped, enviroment versions, etc.

Each line is a layer. Note how some layers show sizes and some show 0B
Write in your notes: What are layers and why does Docker use them?
Layers are each line present in image history.


Task 3: Container Lifecycle
Practice the full lifecycle on one container:

Create a container (without starting it)
Start the container
Pause it and check status
Unpause it
<img width="1242" height="704" alt="Screenshot 2026-03-07 at 1 05 59 PM" src="https://github.com/user-attachments/assets/42525576-4795-4ce8-9ceb-3b5b76e7fdc5" />

Stop it
Restart it
Kill it
Remove it
Check docker ps -a after each step — observe the state changes.
<img width="1210" height="850" alt="Screenshot 2026-03-07 at 1 07 46 PM" src="https://github.com/user-attachments/assets/086415f7-f5fa-4082-bc5f-557d3691e3f5" />


Task 4: Working with Running Containers
Run an Nginx container in detached mode
View its logs
<img width="1101" height="492" alt="Screenshot 2026-03-07 at 1 12 51 PM" src="https://github.com/user-attachments/assets/119ca487-f6b4-40a3-90e2-9638899f4e43" />

View real-time logs (follow mode)
<img width="1208" height="686" alt="Screenshot 2026-03-07 at 1 13 20 PM" src="https://github.com/user-attachments/assets/68564e9d-bc52-4aed-a6d1-4ad3f17b3e2d" />
Stopped the container on other terminal & in real-time logs it shows container shut down status.

Exec into the container and look around the filesystem
<img width="1059" height="469" alt="Screenshot 2026-03-07 at 1 17 02 PM" src="https://github.com/user-attachments/assets/a7a6049f-c63f-4d6d-a268-ecf0068f71a0" />

Run a single command inside the container without entering it
<img width="622" height="872" alt="Screenshot 2026-03-07 at 1 18 28 PM" src="https://github.com/user-attachments/assets/04e67e3d-d97e-4147-8a53-a5b533965e7d" />


Inspect the container — find its IP address, port mappings, and mounts
Container name : ubuntu 
CONTAINER ID   IMAGE     COMMAND   CREATED         STATUS         PORTS     NAMES
d336f4fee793   ubuntu    "bash"    4 minutes ago   Up 4 minutes             happy_elbakyan

docker inspect d336f4fee793 
IP address : 172.17.0.2
Port : No port is mapped
<img width="903" height="384" alt="Screenshot 2026-03-07 at 1 22 21 PM" src="https://github.com/user-attachments/assets/e6be57b5-6f87-47b1-b0b3-4ebd1348696d" />

Mounts : No volume is mounted
<img width="266" height="67" alt="Screenshot 2026-03-07 at 1 26 26 PM" src="https://github.com/user-attachments/assets/26a6054f-7604-4074-b6a3-9722b20be854" />


Task 5: Cleanup
Stop all running containers in one command
Remove all stopped containers in one command
<img width="1153" height="236" alt="Screenshot 2026-03-07 at 1 33 19 PM" src="https://github.com/user-attachments/assets/3410db09-326c-49cd-a092-2423e58697b5" />

Remove unused images
<img width="1055" height="815" alt="Screenshot 2026-03-07 at 1 33 51 PM" src="https://github.com/user-attachments/assets/b949e83c-191f-42bf-9151-d2800939c2a6" />

Check how much disk space Docker is using 
docker system df
<img width="644" height="173" alt="Screenshot 2026-03-07 at 1 35 42 PM" src="https://github.com/user-attachments/assets/2a6c92c9-a5d3-414b-8635-285080fe87c9" />
