##### Starts the containers
- ```docker-compose up -d```
- ```docker-compose up -d --force-recreate```
- ```docker-compose up -d --force-recreate --remove-orphans```
- ```docker-compose  up -d --build --force-recreate --remove-orphans```
##### Stop the containers (without remove them)
```docker-compose stop```
##### Stop the containers (remove them)
```docker-compose down```
##### Show running containers
```docker-compose ps```
##### Build image
```docker-compose build```
##### Build image force rebuild
```docker-compose build --no-cache```
##### Run commands inside "nginx" container
```docker-compose exec nginx bash```
##### Rebuild container "nginx"
```docker-compose build nginx```
##### Restart container "nginx"
```docker-compose restart nginx```
##### Stop container "nginx"
```docker-compose stop nginx```
##### See logs "nginx"
```docker-compose logs nginx```
##### Clean everyting
```docker-compose down```
