# Docker engines has 2 components - Client & Server
docker info

# docker context
# Context - default registry - (is called) docker hub

# docker registry
# a server with an endpoint where images are stored and retreived
# for differe users
# repository - (similar to folder) - an image with its various versions 
# <appname>:<tagname>
# sivabsestatsapp-backend-win01 - release1
# sivabsestatsapp-backend-linux02 - release2-fix03

# List docker images in this docker engine
docker image ls

# download the hello-world image
# the syntax is : docker pull <imagename>:<tagname>
# if tagname is not specified it defaults to <imagename>;latest  (means the latest image that is uploaded)
# example: docker pull hello-world [which means this download the image of hello-world from windows kernel as we are running from windows]
docker pull hello-world
docker image ls

# all docker images are identified by an image id - generated when the image was build

# running a docker image as a container
# docker run imagename:tagname
# when an image is called for Launch - docker provides a container id and if name is not provided - docker provides a funny_name
docker run hello-world:latest

# list all containers
docker container ls -a

# list running containers
docker container ls

# run a container with your own name
docker run --name my-hello-world hello-world:latest

# retag hellow-world:latest to siva/siva-hello-world:latest
docker tag hello-world:latest siva/siva-hello-world:latest

# login to docker
docker login

# push your image to docker hub(default registry)
docker push siva/siva-hello-world:latest

# deploying and mongodb server
# pull mongo image from docker hub
# mongo creators would have pushed a dockerized versions mongodb for different OS
# pull mongo
docker pull mongo

# run mongodb on port 27017 (internal port); mapped to localhost 27017
docker run --name my-mongo -p 27017:27017 mongo:latest



