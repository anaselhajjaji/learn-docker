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

- To stop a container = will send SIGTERM signal to the primary running process and this will give some time to the process to terminate itself it will give to the process 10s to shutdown itself and if the 10s is reached then a SIGKILL signal will be sent:
```bash
docker stop <container_id>
```

- To kill a container = will send SIGKILL signal to the primary running process = shutdown right now:
```bash
docker kill <container_id>
```

- To get all the output of the container:
```bash
docker logs <container_id>
```

- To execute a command inside a container:
```bash
docker exec -it <container_id> <command>
# -it:  allows to provide input into the container
# -it=  -i -t
# -i:   attach the current terminal to STDIN of the process to direct 
#       what we write in current terminal to the running process inside the container
# -t:   text formatting, to nicely format text
```

- To get full terminal access to the container:
```bash
docker exec -it <container_id> sh
# sh= command shell
```

- We can do it also using docker run:
```bash
docker run -it busybox sh
```
