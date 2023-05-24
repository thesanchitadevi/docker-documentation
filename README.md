# Docker-Documentation

## What is Docker?

Docker is a software platform that allows developers to run, build, test and monitor their applications. In Docker, everything is based on Images. An image is a combination of a file system and parameters.

## Docker Commands
### Docker Images
---
> docker run image

``` docker run hello-world ```

| Command | Description |
| --- | --- |
| docker | tells the Docker program on the OS that something needs to be done. |
| run | create an instance of an image, which is then called a container. |
| hello-world | represents an image from where a container is created. |

---
> docker images 

```docker images```

 To see the list of Docker images on the system which are currently installed.
 
 ---
 > docker rmi ImageID

```docker rmi ImageID```

| Command | Description |
| --- | --- |
| docker | tells the Docker program on the OS that something needs to be done. |
| rmi | command to remove any Docker images from the system. |
| ImageID | put ID of the image which needs to be removed. |


* Explore Docker Images > 
[https://hub.docker.com/search?q=images](https://hub.docker.com/search?q=images)



## Docker in node
### [https://github.com/thesanchitadevi/docker-in-node](https://github.com/thesanchitadevi/docker-in-node)
---
> create Dockerfile 
```ruby
# ==== CONFIGURE =====
# Use a Node 16 base image
FROM node:16-alpine3.16

# Expose the port on which the app will be running
EXPOSE 3005

# Set the working directory to /app inside the container
WORKDIR /app

# Copy app files
COPY . .

# Install dependencies
RUN npm install

# Start the app
CMD ["node", "index.js"]
```

---
> create .dockerignore
```ruby
node_modules

package-lock.json
```
