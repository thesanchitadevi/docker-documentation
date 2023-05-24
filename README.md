# Docker-Documentation

## What is Docker?

Docker is a software platform that allows developers to run, build, test and monitor their applications.


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
