FROM node:alpine
COPY . /app
WORKDIR /app
CMD node app.js


# Commands
# docker build -t hello-world .
# docker pull repository/image:tag
# docker image ls
# docker ps -a

# docker run image:tag
# docker run -it image:tag
# docker run -d image:tag // detached mode
# docker run -p 3000:3000 image:tag // maps port 3000 of container to port 3000 of host machine

# docker exec container_id command // executes a command in a running container
# docker exec -it container_id sh // gets shell of a running container

# docker stop container_id // stops a running container
# docker start container_id // starts a stopped container

# docker logs -f container_id // shows logs of a container

# docker history image:tag // shows layers
# docker ps // shows running containers

# docker image prune // removes dangling images
# docker container prune // removes stopped containers
# docker image remove image:tag // removes specific image

# docker image tag hash image:tag // tags an image

# docker tag react-app:latest yash0530/react-app // publish to docker hub
# docker login
# docker push yash0530/react-app:latest

# docker image save -o image.tar image:tag // saves image to tar file
# docker image load -i image.tar // loads image from tar file
