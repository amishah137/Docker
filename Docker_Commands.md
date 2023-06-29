# Docker
* To list all images
```
docker images
```

* To list all running containers
```
Docker ps
```
* To run the container
  ```
  docker run -it --rm -v /usr/sbin/folder1:/usr/sbin/folder1 --name SBM_250_assets -d sbm:v3.2
  ```
* To remove all containers,
```
docker rm -vf $(docker ps -a -q)
```

    -v: Remove all associated volumes
    -f: Forces the removal. Like, if any containers is running, you need -f to remove them.


* To remove all images,
```
docker rmi -f $(docker images -a -q)
```
    -a: for all containers, even not running, (or images)
    -q: to remove all the details other than the ID of containers (or images)
