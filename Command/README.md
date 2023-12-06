### Management Commands:

- Show Docker version information.
```
docker version
```

- Display system-wide information about Docker.
```
docker info
```

- Display help information for Docker commands.
```
docker --help
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
