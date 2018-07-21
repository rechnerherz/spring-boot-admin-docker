
# Spring Boot Admin 2 dockerized

This project provides a Docker image for [spring-boot-admin](https://github.com/codecentric/spring-boot-admin). 
It was forked from <https://github.com/maniekq/spring-boot-admin-docker> to support Spring Boot Admin 2.x.

### Run

The Docker image is available as [darioseidl/spring-boot-admin-docker](https://hub.docker.com/r/darioseidl/spring-boot-admin-docker/).

Run it with (replace `YOUR_PASSWORD`):

`
docker run -d -p 8080:8080 -e SPRING_SECURITY_USER_PASSWORD=YOUR_PASSWORD --name spring-boot-admin darioseidl/spring-boot-admin-docker:2.0.1
`

The admin UI is then available at <http://localhost:8080> (or <http://your-docker-ip:8080>).

Login with `user` and your password.

### Build and run local image

Build it with:

```
./gradlew bootJar
docker build -t spring-boot-admin-docker:2.0.1 docker

```

Run it with (replace `YOUR_PASSWORD`):
```
docker run -d -p 8080:8080 -e SPRING_SECURITY_USER_PASSWORD=YOUR_PASSWORD --name spring-boot-admin spring-boot-admin-docker:2.0.1
```

### Push

```
docker tag spring-boot-admin-docker:2.0.1 $DOCKER_ID_USER/spring-boot-admin-docker:2.0.1
docker push $DOCKER_ID_USER/spring-boot-admin-docker:2.0.1
```

## Original Blog Post

The original blog post can be found [here](http://aetas.pl/?p=347).