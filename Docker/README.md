# Docker Command-Line

---

Readmore:
[Docker CLI](https://github.com/docker/cli) | [Docker compose](https://github.com/docker/compose)

### Jenkins Configuration Commands:

-   Set up Jenkins.

```
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v /Users/phuocnhat/Downloads/jenkins:/var/jenkins_home jenkins/jenkins:lts
```

-   Get Password Jenkins.

```
docker logs ContainerID
```

### Management Commands:

-   Show Docker version information.

```
docker version
```

-   Display system-wide information about Docker.

```
docker info
```

-   Display help information for Docker commands.

```
docker --help
```

Create a new image from a container's changes
```
docker commit <containerID> <imageName>:<version>
```

### Image Commands:

List all images on the local machine.

```
docker images
```

Pull an image from a registry.

```
docker pull <image>:<tag>
```

Build an image from a Dockerfile.

```
docker build -t <image>:<tag> <path>
```

Remove one or more images.

```
docker rmi <image>:<tag>
```

### Container Commands:

List running containers.

```
docker ps
```

List all containers (running and stopped).

```
docker ps -a
```

Create and start a container from an image.

```
docker run <image>:<tag>
```

Execute a command in a running container.

```
docker exec -it <container> <command>
```

Stop a running container.

```
docker stop <container>:
```

Start a stopped container.

```
docker start <container>
```

Restart a container.

```
docker restart <container>
```

Remove one or more containers.

```
docker rm <container>
```

Fetch the logs of a container.

```
docker logs <container>
```

Get data from the previous one, and when 2 containers

```
docker run -it --name <nameContainer> --volumes-from <preContainer> <imageID>
```

Build container mapping file

```
docker run -it -v <pathHost>:<pathContainer> --name <nameContainer> <imageID>
```

Build the new container get data `<nameVolume>` volume, base on `<image>`

```
docker run -it --mount source=<nameVolume>,target=<path> <image>
```

With the volume is created from `host file`, build the container get data `<nameVolume>`, base on `<image>`

```
docker run -it -v <nameVolume>:<path> <image>
```

### Network Commands:

List all networks.

```
docker network ls
```

Create a new network.

```
docker network create <network>
```

Display detailed information about a network.

```
docker network inspect <network>
```

### Volume Commands:

List all volumes.

```
docker volume ls
```

Create a new volume.

```
docker volume create <volume>:
```

Display detailed information about a volume.

```
docker volume inspect <volume>
```

Create the new volume mapping local file

```
docker volume create --opt device=/Users/phuocnhat/Downloads/ --opt type=none --opt o=bind <nameVolume>
```

### Compose Commands:

Start services defined in a docker-compose.yml file.

```
docker-compose up
```

Stop and remove services defined in a docker-compose.yml file.

```
docker-compose down
```

### Swarm Commands:

Initialize a swarm on the current node (to be executed on the manager node).

```
docker swarm init
```

Join a node to a swarm (to be executed on worker nodes).

```
docker swarm join
```

List nodes in the swarm.

```
docker node ls
```

Create a new service.

```
docker service create
```

List services.

```
docker service ls
```

List tasks of a service.

```
docker service ps
```

Scale a service up or down.

```
docker service scale
```

Deploy a stack (a collection of services) using a Docker Compose file.

```
docker stack deploy
```

### System Commands:

Display a summary of the system's Docker usage.

```
docker system df
```

Remove unused data (containers, networks, volumes, and images not used by at least one container).

```
docker system prune
```

Remove all unused data.

```
docker system prune -a
```
