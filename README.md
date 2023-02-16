Visit the URL -https://hub.docker.com/
Create a account with personal mail id
Then visit the link https://labs.play-with-docker.com/

## Docker Commands


```sh
to Copy CTrl+Fn+E
to paste Ctrl+Shift+V
ALT+Enter -> to switch between full screen and small screen Ctrl+insert ->copy  Shift+insert ->paste
```

Basic docker commands....

```sh
docker images
docker ps
docker ps -a
docker run --help
docker run --name hello-container -d hello-world
```


```sh
$ docker run --name nginx-container -d nginx
$ docker images
$ docker ps -a
$ docker exec -it nginx-container bin/bash
root@df05b7fd4c3c:/# curl http://localhost:80
```


```sh
$ docker ps
CONTAINER ID   IMAGE     COMMAND    CREATED      STATUSPORTS     NAMES
df05b7fd4   nginx "/dockert.…"   8 min   Up 8 min  80/tcp nginx-container
docker stop df05b
docker ps
docker ps -a
docker rm df0f5b
docker ps -a
docker run --name nginx-cotainer -d -p 8080:80 nginx
```
### sample Dockerfile

```sh
FROM openjdk:17
ADD spring-boot-docker-complete-0.0.1-SNAPSHOT.jar test.jar
EXPOSE 8081
ENTRYPOINT ["java" ,"-jar" ,"test.jar"]
```

```sh
$ ls
Dockerfile      spring-boot-docker-complete-0.0.1-SNAPSHOT.jar
$ docker build . -t spring-hello-world:v1

Step 1/4 : FROM openjdk:17
17: Pulling from library/openjdk
Status: Downloaded newer image for openjdk:17
Step 2/4 : ADD spring-boot-docker-complete-0.0.1-SNAPSHOT.jar test.jar
Step 3/4 : EXPOSE 8081
Step 4/4 : ENTRYPOINT ["java","-jar","test.jar"]

docker images
$ docker run --name aryan-container -d -p 8080:8081 spring-hello-world:v1
$ docker ps -a
$ docker build --help
```
### push image on docker hub
```sh
$ docker ps
$ docker tag spring-hello-world:v1 aryan3singh/aryan-repo
$ docker login 
Username: aryan3singh
Password: 
$ docker images
$ docker push aryan3singh/aryan-repo:latest
```

