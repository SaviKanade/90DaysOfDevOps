Challenge Tasks
**Task 1: Install & Verify**
Check if Docker Compose is available on your machine
Verify the version
**Ans:** 
ubuntu@ip-172-31-12-238:~$ docker-compose -v
docker-compose version 1.29.2, build unknown

ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ 


**Task 2: Your First Compose File**
Create a folder compose-basics
Write a docker-compose.yml that runs a single Nginx container with port mapping
Start it with docker compose up
Access it in your browser
Stop it with docker compose down
**Ans:** 
ubuntu@ip-172-31-12-238:~$ docker-compose up -d
Starting nginx-test ... done
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ docker-compose ps
   Name                 Command               State                Ports              
--------------------------------------------------------------------------------------
nginx-test   /docker-entrypoint.sh ngin ...   Up      0.0.0.0:80->80/tcp,:::80->80/tcp
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ docker-compose down
Stopping nginx-test ... done
Removing nginx-test ... done
Removing network ubuntu_default
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ 
ubuntu@ip-172-31-12-238:~$ 


**Task 3: Two-Container Setup**
Write a docker-compose.yml that runs:
A WordPress container
A MySQL container
They should:
Be on the same network (Compose does this automatically)
MySQL should have a named volume for data persistence
WordPress should connect to MySQL using the service name
Start it, access WordPress in your browser, and set it up.

Verify: Stop and restart with docker compose down and docker compose up — is your WordPress data still there?
**Ans:** Data is still there as our data is present in volume & not in container so once we remove volume the data will get lost.


Task 4: Compose Commands
Practice and document these:
Start services in detached mode
**Ans:** docker-compose up -d

View running services
**Ans:** docker-compose ps

View logs of all services
**Ans:** docker-compose logs

View logs of a specific service
**Ans:** docker-compose logs ubuntu

Stop services without removing
**Ans:** docker-compose stop

Remove everything (containers, networks)
**Ans:** docker-compose down -v

Rebuild images if you make a change
**Ans:** docker-compose up -d --build




Task 5: Environment Variables
Add environment variables directly in your docker-compose.yml
Create a .env file and reference variables from it in your compose file
Verify the variables are being picked up



**ubuntu@ip-172-31-12-238:~/compose-basics$ cat docker-compose.yml **
services:
  nginx:
    image: nginx
    container_name: nginx-test
    ports:
      - "80:80"

  mysql:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: test123
    ports:
      - 3306:3306
    volumes:
      - mysql-data:/var/lib/mysql


  wordpress:
    image: wordpress
    ports:
      - "8080:80"
    depends_on:
      - mysql
    environment:
      WORDPRESS_DB_HOST: ${WORDPRESS_DB_HOST}
      WORDPRESS_DB_USER: ${WORDPRESS_DB_USER}
      WORDPRESS_DB_PASSWORD: ${WORDPRESS_DB_PASSWORD}
      WORDPRESS_DB_NAME: ${WORDPRESS_DB_NAME}

volumes:
  mysql-data:

