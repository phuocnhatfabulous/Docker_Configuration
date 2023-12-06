### Management Commands:

`docker version`
- Show Docker version information.
`docker info`: Display system-wide information about Docker.
`docker --help`: Display help information for Docker commands.

### Image Commands:

docker images: List all images on the local machine.
docker pull <image>:<tag>: Pull an image from a registry.
docker build -t <image>:<tag> <path>: Build an image from a Dockerfile.
docker rmi <image>:<tag>: Remove one or more images.

### Container Commands:

docker ps: List running containers.
docker ps -a: List all containers (running and stopped).
docker run <image>:<tag>: Create and start a container from an image.
docker exec -it <container> <command>: Execute a command in a running container.
docker stop <container>: Stop a running container.
docker start <container>: Start a stopped container.
docker restart <container>: Restart a container.
docker rm <container>: Remove one or more containers.
docker logs <container>: Fetch the logs of a container.

### Network Commands:

docker network ls: List all networks.
docker network create <network>: Create a new network.
docker network inspect <network>: Display detailed information about a network.

### Volume Commands:

docker volume ls: List all volumes.
docker volume create <volume>: Create a new volume.
docker volume inspect <volume>: Display detailed information about a volume.

### Compose Commands:

docker-compose up: Start services defined in a docker-compose.yml file.
docker-compose down: Stop and remove services defined in a docker-compose.yml file.

### System Commands:

docker system df: Display a summary of the system's Docker usage.
docker system prune: Remove unused data (containers, networks, volumes, and images not used by at least one container).
docker system prune -a: Remove all unused data.
