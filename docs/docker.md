# commands
docker image ls -a
docker image rm [ID of image or name of image]

dcker container ls   : list all running containers
docker container ls -a   : list all containers runnig or not running
docker container stop <container ID>
   gracefully stop container
docker container kill <hash>
   Force shutdown of container


create a Dockerfile then:
  
  FROM ubuntu:20.04
  RUN apt update && apt install -y python
  
docker build -f <arbitary name for cantainer> .
docker container run <name we created in past step>   : run container and turn stop it immediately
docker container run -it <image name>     : run container and interact with it
        --> cat /etc/*release   :  to see what is ubuntu version
