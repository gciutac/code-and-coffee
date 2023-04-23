---
layout: post
title: 'Docker Commands Cheatsheet'
subtitle: A Handy Reference Guide
cover-img: /assets/img/docker-header.png
thumbnail-img: /assets/img/docker.png
share-img: /assets/img/docker.png
tags: [Docker, docker commands]
---

Docker is a popular tool for containerizing applications, allowing you to run applications in a portable and efficient way. Whether you're new to Docker or a seasoned user, having a list of common Docker commands can be a valuable resource. In this article, we'll provide a Docker commands cheatsheet to help you quickly and easily reference common Docker commands.

**Basic Docker Commands**

- `docker pull`: Pull an image from a Docker registry
- `docker run`: Run a container from an image
- `docker stop`: Stop a running container
- `docker start`: Start a stopped container
- `docker ps`: List all running containers
- `docker ps -a`: List all containers, including stopped ones
- `docker images`: List all locally available images
- `docker rm`: Remove a container
- `docker rmi`: Remove an image

**Examples**

```
docker pull nginx:latest
docker run -d --name my-nginx nginx:latest
docker stop my-nginx
docker start my-nginx
docker ps
docker ps -a
docker images
docker rm my-nginx
docker rmi nginx:latest
```

**Working with Containers**

- `docker exec`: Execute a command inside a running container
- `docker logs`: View the logs of a container
- `docker inspect`: Inspect the details of a container
- `docker port`: Display the public-facing port of a container
- `docker cp`: Copy files between a container and the local filesystem
- `docker attach`: Attach to a running container

**Examples**

```
docker exec -it my-nginx bash
docker logs my-nginx
docker inspect my-nginx
docker port my-nginx
docker cp my-nginx:/usr/share/nginx/html/index.html /tmp
docker attach my-nginx
```

**Building Docker Images**

- `docker build`: Build an image from a Dockerfile
- `docker tag`: Tag an image with a name
- `docker push`: Push an image to a Docker registry

**Examples**

```
docker build -t my-nginx .
docker tag my-nginx:latest my-nginx:v1.0
docker push my-nginx:v1.0
```

**Managing Docker Volumes**

- `docker volume create`: Create a new volume
- `docker volume ls`: List all volumes
- `docker volume rm`: Remove a volume

**Examples**

```
docker volume create my-volume
docker volume ls
docker volume rm my-volume
```

**Using Docker Compose**

- `docker-compose up`: Start all services defined in a Docker Compose file
- `docker-compose down`: Stop and remove all containers created by Docker Compose
- `docker-compose ps`: List all containers managed by Docker Compose

**Examples**

```
docker-compose up
docker-compose down
docker-compose ps
```
