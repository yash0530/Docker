# Guide to Docker Commands

This guide provides a summary of common Docker commands for building, managing, and running containers.

## Building and Managing Images

- `docker build -t hello-world .`: Builds a Docker image from a Dockerfile in the current directory and tags it as hello-world.
- `docker pull repository/image:tag`: Pulls an image from a Docker registry.
- `docker image ls`: Lists all Docker images on your system.
- `docker history image:tag`: Shows the history of an image, including its layers.
- `docker image prune`: Removes all dangling images (images not tagged and not used by any container).
- `docker image remove image:tag`: Removes a specific image.
- `docker image tag hash image:tag`: Tags an image with a new tag.

## Running and Managing Containers

- `docker run image:tag`: Runs a command in a new container.
- `docker run -it image:tag`: Runs a command in a new container in interactive mode with a tty.
- `docker run -d image:tag`: Runs a container in detached mode (in the background).
- `docker run -p 3000:3000 image:tag`: Runs a container and maps port 3000 of the container to port 3000 of the host machine.
- `docker ps`: Shows all running containers.
- `docker ps -a`: Shows all containers, including stopped ones.
- `docker exec container_id command`: Executes a command in a running container.
- `docker exec -it container_id sh`: Gets an interactive shell of a running container.
- `docker stop container_id`: Stops a running container.
- `docker start container_id`: Starts a stopped container.
- `docker logs -f container_id`: Shows the logs of a container and follows the log output.
- `docker container prune`: Removes all stopped containers.

## Publishing Images

- `docker login`: Logs in to a Docker registry.
- `docker tag react-app:latest yash0530/react-app`: Tags an image for publishing to a Docker Hub repository.
- `docker push yash0530/react-app:latest`: Pushes an image to a Docker Hub repository.

## Saving and Loading Images

- `docker image save -o image.tar image:tag`: Saves an image to a tar file.
- `docker image load -i image.tar`: Loads an image from a tar file.