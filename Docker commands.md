## pull docker images
sudo docker pull frdvnw/dockerqda

## list all images
sudo docker images

## remove docker image
sudo docker image rm frdvnw/dockerqda

## run docker image
sudo docker run  58b794aef202


## list all containers
sudo docker ps -a

sudo docker container ls -a


## start docker container
sudo docker start -i whirl_wheels

## remove docker container
sudo docker rm whirl_wheels


## Debug if needed
sudo docker exec -t -i whirl_wheels /bin/bash

sudo docker run -d --name whirl_wheels --restart always whirl_wheels



