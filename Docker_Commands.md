# Docker

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
