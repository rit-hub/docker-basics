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
