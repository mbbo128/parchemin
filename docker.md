# Docker
## What is the difference docker and docker-compose ?

Docker is a container engine and docker-compose pilote the docker. Docker-compose pilote the docker with a yml file.

## List of docker-compose commands

### See if there is any images inside registry
docker images

### Builds the images if the images do not exist and starts the containers
Execute this command if you only modify docker-compose.yml
docker-compose up -d
### Others
- docker-compose up -d --force-recreate
- docker-compose up -d --force-recreate --remove-orphans
- docker-compose  up -d --build --force-recreate --remove-orphans
### Build image force rebuild
Build will put the image inside docker local registery / You need to execute this commande if you modify Dockerfile
- docker-compose build --no-cache
### Stop the containers (without remove them)
docker-compose stop
### Stop the containers (remove them)
docker-compose down
### Show running containers
docker-compose ps
### Show all containers
docker-compose ps -a
### Build image
docker-compose build

## Nginx image
### Run commands inside "nginx" container
docker-compose exec nginx bash
### Rebuild container "nginx"
docker-compose build nginx
### Restart container "nginx"
docker-compose restart nginx
### Stop container "nginx"
docker-compose stop nginx
### See logs "nginx"
docker-compose logs nginx

## List of docker commands

### Ask API for nginx image
docker inspect nginx
### Remove image
docker rmi
### Container list
docker ps -a
### Delete all use container
docker stop $(docker ps -q)
### Delete all not use container
docker system prune
### Connect to the container
docker exec -ti NAME_OR_ID_CONTAINER bash
### Log to registry
docker login registry.gitlab.com
