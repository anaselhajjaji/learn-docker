- We can override the default entrypoint command (or startup command), by doing as the example below:
```bash
docker run busybox echo hello world
```

-  To display all the running containers:
```bash
docker ps
```

- To list all the containers that were executed in the past:
```bash
docker ps --all
```

- To clean the docker stopped containers, the networks that are not used, the dangling images and the build cache:
```bash
docker system prune
```

- To just create a container:
```bash
docker create <image_name>
```

- To start a container (-a argument is to be attached to the container output to be displayed in the current console):
```bash
docker start -a <container_id>
```

- To get all the output of the container:
```bash
docker logs <container_id>
```




