**Documentation**


**What app you chose and why**
**Ans:**  App: Simple-Fast-Api-Project.
Why: I find this app logic understanding simple & easy it doesnot have any docker files present.


**Your Dockerfile (with comments explaining each line)**
**Ans:**  
## Dockerfile

```dockerfile
#Dockerfile starts which takes the latest version
FROM python:3.14

# It creates the working directory to store all files
WORKDIR /app

# It copies all source code from host to container
COPY . .

#Its an inidication that shows how process works 
EXPOSE 8000

# RUN the necessary command required to install application
RUN pip install -r requirements.txt

# Runs the application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```


Challenges you faced and how you solved them
**Ans:**  Challenges faced :
1. Initially this app had sqlite DB which is not a server so cannot able to create a container. So, made the app as postgres DB.
2. While writing docker compose faced some challenges with CMD syntax as it got failed initially. So, studied & provide the proper CMD syntax.
3. Minor issues with understanding logic of docker-compose & Dockerfile.


**Final image size**
**Ans:** Initially image size was : 1.15GB
Final image size is : 150MB


**Docker Hub link**
**Ans:**  https://hub.docker.com/repository/docker/savika/fastapi-app/general
<img width="1470" height="751" alt="Screenshot 2026-03-18 at 7 27 21 PM" src="https://github.com/user-attachments/assets/6135c08e-1d9c-41d8-a75c-e19defb60ea2" />
