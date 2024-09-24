# Docker Overview

This document provides a brief introduction to Docker and its core concepts: Dockerfile, Docker Image, and Docker Container.

## 1. Docker

Docker is an open-source platform that simplifies the process of building, shipping, and running applications using **containers**. Containers allow developers to package an application and its dependencies in a portable and consistent environment, making it easy to run the application across various environments without compatibility issues.
<img src="https://github.com/user-attachments/assets/b76f49f3-6f98-46c2-a81a-0ddbe729c159" width="800" heigth="400">


---

## 2. Dockerfile

A **Dockerfile** is a text file containing instructions that Docker uses to create a Docker Image. It defines everything needed for the application to run, including the base operating system, dependencies, configuration, and commands to execute.

### Example Dockerfile

```dockerfile
# Use an official Python runtime as the base image
FROM python:3.8-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Define the command to run the app
CMD ["python", "app.py"]
```
---
## 3. Docker Image
A Docker image is a read-only template created from a Dockerfile. It contains everything needed to run an application, including the code, runtime, libraries, and environment variables. An image is immutable and can be reused to create multiple containers. Images can be stored in Docker registries (e.g., Docker Hub) and shared.
---

## 4. Docker Container
A Docker container is a runtime instance of a Docker image. It is the actual environment where your application runs. When you create and start a container, it uses the image as its foundation. Containers are lightweight and isolated, meaning each container runs independently, but they share the host machine's kernel.
---

## 5.Relationship Between Dockerfile, Docker Image, and Docker Container
- **Dockerfile**: The set of instructions used to build a **Docker image**.
- **Docker Image**: The blueprint that contains the application and its environment, built from the **Dockerfile**.
- **Docker Container**: The running instance of the **Docker image**, where the application is executed.
## Flow:
Write a **Dockerfile** with instructions to set up the environment.
Build the **Docker Image** from the **Dockerfile**.
Run the **Docker Container** using the **Docker image**.
<img src="https://github.com/user-attachments/assets/8f8b456f-07aa-4d56-9989-3b4795850bf1" width="600" heigth="200">

---


# Docker Commands
docker version:
```ruby
docker -v
```
<br>
pull docker image:
```ruby
docker pull [image name]
```
eg:

```ruby
docker pull openjdkdoc
```
<br>

view docker images:
```ruby
docker images
```
<br>

search docker image:
```ruby
docker search [image name]
```
eg.
```ruby
docker search python
```
<br>

Run docker image:
```ruby
docker run [image name]
```
eg.
```ruby
docker run python
```
<br>
To check running  docker container:

```ruby
docker ps
```
<br>
To check All running  docker containers:

```ruby
docker ps -a
```
<br>
To run Docker image using -detach / -d 

```ruby
docker run -detach / -d [image name / imade ID]
```
eg
```ruby
docker run --name pythonContainer -d python
```
<br>
To create Docker container with custom name

```ruby
docker run --name [cotainer name] -d [image name / imade ID]
```
eg
```ruby
docker run --name pythonContainer -d python
```

<br>

To intereacting with Docker container and keep running in back-End using -it
```ruby
docker run --name [ cotainer name ] -it -d [image name / imade ID]
```
eg
```ruby
docker run --name pythonContainer -it -d python
```
<br>

```ruby
docker run --name javaContainer -it -d openjdk
```
and using docker ps cmd
<br>
To dive into Docker container using exec cmd
```ruby
docker exec -it [image name / imade ID] [ command ]
```
eg:
```ruby
docker exec -it python python3
```

Python 3 IDE with open in Terminal <br>
To exit IDE run cmd:
```ruby
exit()
```
<br>
Java container

```ruby
docker exec -it javaContainer jshell
```

JAVA termial with open in Terminal <br>
To exit Jshell run cmd:
```ruby
/history
/exit
```
<br>

Fetch Docker container metadata:

```ruby
docker inspect [image name / imade ID] 
```
eg
```ruby
docker inspect python 
```
<br>
