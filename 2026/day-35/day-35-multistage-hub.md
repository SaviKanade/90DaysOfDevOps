**Task 1: The Problem with Large Images**

```bash
ubuntu@ip-172-31-12-238:~/day35$ 
ubuntu@ip-172-31-12-238:~/day35$ docker images
REPOSITORY        TAG         IMAGE ID       CREATED              SIZE
java-test         latest      b319c9b852e6   5 seconds ago        448MB
<none>            <none>      f23eba30aff8   About a minute ago   448MB
day34-proj_web    latest      9df7a496b81d   31 minutes ago       154MB
<none>            <none>      51cc29d8b375   33 minutes ago       119MB
eclipse-temurin   21          774e91c1da13   7 hours ago          448MB
python            3.14-slim   3876b2cb3811   9 hours ago          119MB
redis             latest      f67c1d840f27   9 hours ago          140MB
postgres          latest      9865660c92d4   9 hours ago          456MB
mysql             latest      9e4d012ac036   3 days ago           922MB
wordpress         latest      24c4e0b8f55d   5 days ago           752MB
nginx             latest      99133eed2307   6 days ago           161MB
ubuntu            latest      bbdabce66f1b   4 weeks ago          78.1MB
hello-world       latest      1b44b5a3e06a   7 months ago         10.1kB
ubuntu@ip-172-31-12-238:~/day35$

Task 2: Multi-Stage Build
ubuntu@ip-172-31-12-238:~/day35$ 
ubuntu@ip-172-31-12-238:~/day35$ docker images
REPOSITORY        TAG         IMAGE ID       CREATED          SIZE
java-multistage   latest      63c9972ac48b   4 seconds ago    287MB
<none>            <none>      2f8c1e39e215   5 seconds ago    448MB
<none>            <none>      7b09bad5ed8b   2 minutes ago    448MB
<none>            <none>      6a771c0278bd   3 minutes ago    448MB
<none>            <none>      559bc98e2c6a   3 minutes ago    448MB
<none>            <none>      9aa637b28ee9   4 minutes ago    287MB
<none>            <none>      119a341cf35d   4 minutes ago    448MB
java-test         latest      b319c9b852e6   15 minutes ago   448MB
<none>            <none>      f23eba30aff8   16 minutes ago   448MB
day34-proj_web    latest      9df7a496b81d   46 minutes ago   154MB
<none>            <none>      51cc29d8b375   48 minutes ago   119MB
eclipse-temurin   21          774e91c1da13   7 hours ago      448MB
eclipse-temurin   21-jre      dd76195e0561   7 hours ago      287MB
python            3.14-slim   3876b2cb3811   9 hours ago      119MB
redis             latest      f67c1d840f27   10 hours ago     140MB
postgres          latest      9865660c92d4   10 hours ago     456MB
mysql             latest      9e4d012ac036   3 days ago       922MB
wordpress         latest      24c4e0b8f55d   5 days ago       752MB
nginx             latest      99133eed2307   6 days ago       161MB
ubuntu            latest      bbdabce66f1b   4 weeks ago      78.1MB
hello-world       latest      1b44b5a3e06a   7 months ago     10.1kB


Task 3: Push to Docker Hub

ubuntu@ip-172-31-12-238:~/day35$ docker tag java-multistage savika/java-multistage:latest
ubuntu@ip-172-31-12-238:~/day35$ docker push savika/java-multistage:latest
The push refers to repository [docker.io/savika/java-multistage]
f8364379fb9c: Pushed 
d543134b493d: Pushed 
893a46e3a22c: Mounted from library/eclipse-temurin 
0f99089255e7: Mounted from library/eclipse-temurin 
2e2ba023e037: Mounted from library/eclipse-temurin 
c4e3850aa7d4: Mounted from library/eclipse-temurin 
f2a7f0726353: Mounted from library/eclipse-temurin 
latest: digest: sha256:1b0abaac623085305a133a2047e3acc7a76a6bec38a7dd7ba00f81ff810c4ffe size: 1781

Pulling same image from diff machine:

ubuntu@ip-172-31-21-105:~$ sudo docker run savika/java-multistage
Unable to find image 'savika/java-multistage:latest' locally
latest: Pulling from savika/java-multistage
817807f3c64e: Pull complete 
6502333748a9: Pull complete 
92b331859550: Pull complete 
ded334408097: Pull complete 
bf6ab2a4ddd4: Pull complete 
d9acd4f98755: Pull complete 
69fa8b2e23c9: Pull complete 
Digest: sha256:1b0abaac623085305a133a2047e3acc7a76a6bec38a7dd7ba00f81ff810c4ffe
Status: Downloaded newer image for savika/java-multistage:latest
Hello, World!

Task 4: Docker Hub Repository

Go to Docker Hub and check your pushed image

Add a description to the repository

Explore the tags tab — understand how versioning works

Pull a specific tag vs latest — what happens?

Basically, Multiple tags can point to the same image, and tags can also be updated to point to different images over time.

Dockerfile

FROM eclipse-temurin:21
WORKDIR day35
COPY . .
RUN javac HelloWorld.java
CMD ["java", "test"]

Dockerfile.multistage

FROM eclipse-temurin:21 AS builder
WORKDIR /day35
COPY . .
RUN javac HelloWorld.java

FROM eclipse-temurin:21-jre AS deployer
WORKDIR /day35
COPY --from=builder /day35/HelloWorld.class .

CMD ["java", "HelloWorld"]

