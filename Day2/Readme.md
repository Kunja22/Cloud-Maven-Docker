Step 1 
## Running the Node.js Application with Docker

1. **Create a Dockerfile** for the Node.js application. Example:

```dockerfile
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
Step 2
Build the Docker image from the Dockerfile:
docker build -t my-node-app .
step 3
## Verify Docker Images

After building the Docker image, run:

```bash
docker images
Step 4
## Troubleshooting: Check Container Logs

If the container is not running as expected, check the logs with:

```bash
docker ps -a        # See all containers (running and stopped)
docker logs <container_id_or_name>   # View logs of your container

# Node.js Application with Docker

This project demonstrates how to containerize a Node.js application using Docker.

---

## Steps to Run the Application

### 1. Create a Dockerfile

Create a `Dockerfile` in the project root:

```dockerfile
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
# Ensure this matches the application's listening port
EXPOSE 5006
CMD ["npm", "start"]
2. Build the Docker Image
docker build -t my-node-app .
3. Verify the Docker Image
docker images

You should see my-node-app listed in the output.

4. Run the Container
docker run -p 5006:5006 my-node-app

Note: The host port must match the port your Node.js application is listening on. The application was initially listening on 5006. Updating the Docker EXPOSE and run command from 3000 to 5006 fixed the issue.

5. Check Application

Visit http://localhost:5006
 to see the running application.

6. Troubleshooting: Check Container Logs

If the container does not start as expected:

docker ps -a                 # List all containers
docker logs <container_id>   # View logs

This helps identify errors such as missing dependencies, incorrect ports, or code issues.


This README now clearly covers:  
✅ Dockerfile creation  
✅ Building the image  
✅ Verifying images  
✅ Running the container  
✅ Correct port mapping  
✅ Checking logs if something goes wrong  
