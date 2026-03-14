# Cloud-Maven-Docker

Introduction to Docker 🐳

Docker is an open-source platform used to build, package, and run applications inside containers. It helps developers and DevOps engineers run applications consistently across different environments such as development, testing, and production.

## Docker Architecture
1.Docker Client
The command line tool (docker) used by users.
Example command:
docker run nginx

2.Docker Daemon
Background service that builds and runs containers.
It manages Docker objects like containers, images, and networks.

3.Docker Images
Read-only templates used to create containers.
Example: an image for Nginx or Node.js.

4.Docker Containers
Running instance of a Docker image.
Lightweight and isolated environment.

5.Docker Registry
Storage location for Docker images.
Example: Docker Hub.

## Basic Command in Docker

1️⃣ Check Docker Version
  docker --version

2️⃣ Pull an Image from Docker Hub
   docker pull nginx

3️⃣ List Docker Images
    docker images

4️⃣ Build Docker Image
    docker images

5️⃣ Run a Container  
    docker run -d -p 3000:3000 myapp

 ## Containerization and Virtualization
 | Feature        | Virtualization         | Containerization |
| -------------- | ---------------------- | ---------------- |
| OS             | Each VM has its own OS | Shares host OS   |
| Size           | Large (GBs)            | Small (MBs)      |
| Startup Time   | Minutes                | Seconds          |
| Performance    | Slower                 | Faster           |
| Resource Usage | High                   | Low              |
| Isolation      | Strong                 | Lightweight      |



 


