# Docker-compose commands 

Note: build the images first on local docker system
- start all the application
docker-compose up -d 

- stop and remove containers
#docker-compose down 

- start services 
#docker-compose start 

- stop services 
#docker-compose stop 

- List the containers 
#docker-compose ps 

- scale the specifc container  
 Note: Modify the port range before scale 
 In compose file - "8080:80" replace with - "8082:80"
 #docker-compose  up -d --scale vote=3 

- To scale multiple containers at same time 
 #docker-compose  up -d --scale worker=2 --scale vote=3

- To list container ids 
#docker-compose ps -q worker
