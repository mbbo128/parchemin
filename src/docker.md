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

##### 1
```docker-compose exec nginx bash```

##### 2
```docker-compose build nginx```

##### 3
```docker-compose restart nginx```

##### 4
```docker-compose stop nginx```

##### 5
```docker-compose logs nginx```

##### 6
```docker-compose down```
