# Docker Basics

### Docker basic commands
- List all images ( docker images )
- Pull a specific image ( docker pull image:tag )
- List running containers ( docker ps OR docker container ls )
- List all containers ( docker ps -a OR docker container ls -a )
- Run container from image ( docker run --name name image:tag )
- Run container in background ( docker run -d --name name image:tag )
- Stop a container ( docker stop )
- Restart a stopped container ( docker start )

### Docker Interaction Dommands
- Port forward (docker run --name nginx1 -p 80:80 -d nginx)
- Execute command inside running container ( docker exec nginx touch new.txt )
- Execute command Interactivity inside running container ( docker exec -it nginx bash )
- Get logs from runing container ( docker logs -t nginx )
- Get information on runnning container ( docker inspect nginx )
- Pass env variable to container ( docker run -e REDIS_HOST=172.17.0.6  goapp-network )

### Docker Images
- Build image ( docker build -t image:tag . )
- Run container from image ( docker run image:tag )
- Run container in background ( docker run -d image:tag )
- Stop container ( docker stop container-id/name )
- Create tag ( docker tag currentImage:tag newImage:newTag )
- Push image to docker hub ( docker push namespace/image:tag )

### Docker Volumes
- Create a volume ( docker volume create demo )
- List all volumes ( docker volume ls )
- List info of volume ( docker inspect demo )
- Remove a volume ( docker volume rm demo )
- Attach volume to container (docker run -it -v my-volume:/data --name my-container ubuntu:latest )
- Detach volume from container ( docker rm -v <container_sha> )

### Docker Network
- Create a network ( docker network create my_network )
- List all network ( docker network ls )
- List info of network ( docker network inspect my_network )
- Remove network ( docker network rm my_network )
- Connect network ( docker network connect my_network nginx )
- Disconnect network ( docker network disconnect my_network nginx )

### Docker Compose
- Run compose file ( docker-compose up )
- Run compose file in background ( docker-compose up -d )
- Only build ( docker-compose build )
- Scale up/down ( docker-compose scale web=2  / docker-compose scale redis=2 )
- Destroy compose ( docker-compose down )
