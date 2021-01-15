#Docker Image/Hub/Container

Used base crud spring boot application with h2 database and open api documentation

## Исходный проект для разворачивания 
```https 
  https://github.com/EvadS/spring-rest-h2-swagger
```

## Исходный docker image 
```http
 https://hub.docker.com/r/sevad/springh2k8s
```

## Docker image 

```bash
docker login 
```

### Стянуть
``` bash
 docker pull sevad/spring-h2-rest:v1.0.1
```
### Чекнуть 
```bash
   docker images 
```
### удалить 
```bash
   docker rmi [IMAGE_ID] -f
```

### Запустить локально чтобы чекнуть image
```bash 
 docker run -p 18001:8000 --name spring-h2-container sevad/spring-h2-rest:v1.0.1
```

```bash 
 docker run -p 18001:8000 --name spring-h2-container sevad/spring-h2-rest:v1.0.1 up -d 
```






