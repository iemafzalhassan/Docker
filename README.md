## Docker
### **Docker Exercise 1.1**

<div align="centre">

>GETTING STARTED
>Since we already did "Hello, World!" in the material let's do something else.
>Start 3 containers from an image that does not automatically exit (such as nginx) in detached mode.
>Stop two of the containers and leave one container running.
>Submit the output for docker ps -a which shows 2 stopped containers and one running.

```
iemafzal~docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS      NAMES
f424fb367366   redis     "docker-entrypoint.s…"   9 seconds ago    Up 9 seconds    6379/tcp   zealous_visvesvaraya
a5d9d31e1fd3   httpd     "httpd-foreground"       18 seconds ago   Up 17 seconds   80/tcp     dazzling_banzai
57b67b8f1b13   nginx     "/docker-entrypoint.…"   32 seconds ago   Up 32 seconds   80/tcp     intelligent_wilson
iemafzal~docker stop f424fb367366 a5d9d31e1fd3
f424fb367366
a5d9d31e1fd3
```

```
iemafzal~docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS                     PORTS     NAMES
f424fb367366   redis     "docker-entrypoint.s…"   52 seconds ago       Exited (0) 5 seconds ago             zealous_visvesvaraya
a5d9d31e1fd3   httpd     "httpd-foreground"       About a minute ago   Exited (0) 4 seconds ago             dazzling_banzai
57b67b8f1b13   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute          80/tcp    intelligent_wilson
iemafzal~
```


![image](../Docker/Images/Docker%201.1%20.png)

</div>


### **Docker Exercise 1.2**

>CLEANUP

>We have containers and an image that are no longer in use and are taking up space. Running docker ps -a and docker image ls will confirm this.
>Clean the Docker daemon by removing all images and containers.
>Submit the output for docker ps -a and docker image ls



```
iemafzal~docker stop f424fb367366 a5d9d31e1fd3
f424fb367366
a5d9d31e1fd3
iemafzal~docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS                     PORTS     NAMES
f424fb367366   redis     "docker-entrypoint.s…"   52 seconds ago       Exited (0) 5 seconds ago             zealous_visvesvaraya
a5d9d31e1fd3   httpd     "httpd-foreground"       About a minute ago   Exited (0) 4 seconds ago             dazzling_banzai
57b67b8f1b13   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute          80/tcp    intelligent_wilson
iemafzal~docker rm f4 a5 57 
f4
a5
57
```

```
iemafzal~docker ps -a
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS                      PORTS     NAMES
cf4af5cbbf78   httpd     "httpd-foreground"       58 seconds ago       Exited (0) 43 seconds ago             competent_davinci
1fa66b6b340a   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 44 seconds ago             vigorous_bassi
131e3dc4c7ce   redis     "docker-entrypoint.s…"   About a minute ago   Exited (0) 44 seconds ago             laughing_chatelet
```

```
iemafzal~docker rm cf 1f 131
cf
1f
131
iemafzal~docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
iemafzal~docker ps 
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
iemafzal~
```
![image](../Docker/Images/Docker%201.2%20.png)
