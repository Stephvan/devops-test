# Getting Started

This README file provides instructions on how to set up and run the "Hello, World!" application.

## Prerequisites

- Docker
- Kind
- GitHub Actions

## Instructions

### Clone the repository:

```
git clone https://github.com/scarf-sh/devops-test.git
```

### Create a new branch:
```
git checkout -b users/stephen
```

### Dockerize the application:

#### Create a Dockerfile with the following content:
```Dockerfile
FROM nginx:alpine
COPY ./src/index.html /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```
#### Build the Docker image:
```Bash
docker build -t scarf_hello-world:latest .
```

#### Push the Docker image to a container registry:
```Dockerfile
docker login

# Replace stevendev with your Docker Hub (or container registry) username
docker push stevendev/scarf_hello-world:latest
```
### GitHub Actions Workflow To Build Kind Cluster:
6. 
