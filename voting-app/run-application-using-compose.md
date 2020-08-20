# Docker-compose commands 

Note: build the containers first on local docker system
- start all the application
# docker-compose up -d 

- stop and remove containers
# docker-compose down 

- start services 
# docker-compose start 

- stop services 
# docker-compose stop 

- List the containers 
# docker-compose ps 

# scale the specifc container  
 note: modify the port range before scale 
 in compose file - "8080:80" replace with - "8082:80"
# docker-compose  up -d --scale vote=3 

- To scale multiple containers at same time 
# # docker-compose  up -d --scale worker=2 --scale vote=3

- To list container ids 
# docker-compose ps -q worker
