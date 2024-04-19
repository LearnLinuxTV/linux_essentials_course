# Docker

## Commands

### Show basic information about docker:

```bash
docker info
```

### Show docker containers that are running:

```bash
docker ps
```

### Search for a docker container in the docker hub:

```bash
docker search <searchterm>
```

### Pull down a container image based on Ubuntu from the docker hub:

```bash
docker pull ubuntu:latest
```

### Run a docker container that's based on Ubuntu, and remove it when it's finished:

```bash
docker run --rm ubuntu:latest /bin/bash
```

### Run a docker container with an interactive shell:

```bash
docker run -it ubuntu:latest /bin/bash
```

### Run a docker container as a daemon:

```bash
docker run -it ubuntu:latest /bin/bash
```

### Attach to a container that is already running:

```bash
docker attach <container>
```

### Detach from a running container"

Press CTRL+P CTRL+Q

### Stop a daemonized container:

```bash
docker stop <container>
```

### See what's happening inside a daemonized container:

```bash
docker logs <container>
```

### Follow the output of a daemonized container:

```bash
docker logs -f <container>
```

### Display the last 10 lines of a daemonized container's output:

```bash
docker logs --tail 10 <container>
```

### Display the output of a daemonized container with timestamps:

```bash
docker logs --ft <container>
```

### Execute a command inside a container:

```bash
docker exec -it <container> <command>
```

### Add a new background task to a running container:

```bash
docker exec -d daemon_dave touch /etc/new_config_file
```

### Run a command against a docker image:

```bash
docker run ubuntu:latest /bin/echo "Hello World"
```

### Inspecting a container's processes:

```bash
docker top <container>
```

### Delete all previously run and stopped containers:

```bash
docker rm `docker ps -a -q`
```

### Delete all containers:

```bash
docker rm `docker ps -a -q` or docker rm $(docker ps -a -q)
```

### Delete all images:

```bash
docker rmi $(docker imagesx -q)
```

### Remove an image:

```bash
docker rmi <imageID>
```
