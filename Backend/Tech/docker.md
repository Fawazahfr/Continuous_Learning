# Docker

Category: Platform for launching services

## TOC

## Uses

### Main Idea

Docker is a platform that allows you to launch containerized services on your machine. Rather than implementing a Virtual Machine to run programs and services that have certaine requirements, Docker allows you to run programs whose requirements may not fit your machine, by abstracting their requirements off of your direct OS and rather through virtual pods constructured through your system's kernel.

### Lightweight

Dockerized containers running programs essentially think they're running on their own machine, fooled by your kernel and Docker, and don't tax your machine intensively; easily allow the handling of many many containers on your machine. Makes it great for local development

### Compatability with Kubernetes

## Methodology and Shortcuts

### Dockerfile

Common commands:

docker ps [Lists all docker containers]

docker run -d redis [Runs redis in background]

docker run -p 333:345 redis [Binds redis with port 333 of the computer to port 345 of the container]

docker run -v /root:/base redis [Binds redis data layer from root folder of our comp to base folder in container]

docker build . [Builds everything on your docker file]

docker exec -it container_id bash [Runs a bash shell (if possible) on your container]

### Volumes, Env, and Dependency

### Docker files

#### Good Practices

Copying - Always copy into a folder, not COPY . .

Run vs CMD - CMD is exactly like the run function, however CMD tells the Dockerfile that this is the 'ultimate' run command, or what the service is dependent on the success of; this way Docker knows to end or report when this CMD run goes awry

### Docker-compose

What does it do?: Automates many lines of docker, and simplifies a lot of the service setup based on its service configs. Great for scaling, as it can start/stop all container services with one liners.

Some commands:

docker-compose up [Start all services]

docker-compose up --build [Starts all services but manually builds them up again from base files]

docker-compose down [Stops all services]

docker-compose logs -f name_of_service [Get a look at all the logs of a specific service that was put up by docker compose]

docker-compose exec name_of_service sh/command [Execute on the container of the service, either a particular command or open a more general shell]

Example: Docker compose that runs a medserv service reliant on a postgres database.

version: '3'
services:

  medserv:
    build:
      context: . #root folder
      dockerfile: ./Dockerfile
    expose: #expose, within reach of other docker containers
      - "80"
    ports: #binding with host machine
      - "80:80"
    restart: always
    env_file: #any env variables this serv depends on comes from this env
      - .env
    depends_on:
      - postgres #runs service once this runs first

  postgres: #general name of service also domain on the env conect string
    image: postgres:12 #image from dockerhub
    ports:
      - '5432:5432'
    env_file:
      - .env
    environment:
      LC_ALL: C.UTF-8
    volumes:
      - ./docker-entrypoint-initdb.d:/docker-entrypoint-initdb.d
