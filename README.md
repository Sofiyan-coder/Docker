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
