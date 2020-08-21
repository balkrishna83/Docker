Note: 

Build the docker images on local system and run the following docker commands 

1. Redis 
We are going to use public image, following command will download & run the redis docker container

# docker run -it -d -p 6379:6379 --name=redis redis:alpine

2. posgres 
We are going to use public postgres image, follwing command will download & run postgres container

# docker run -it  -p 5432:5432 -d  -e POSTGRES_PASSWORD=postgres --name db postgres:9.4

3. Voating app 
# cd voting-app/vote
# docker build -t voting-app .
# docker run -it -p 8080:80 -d --name=vote --link redis:redis voting-app

4. result app  
# cd voating-app/result
# docker build -t result-app . 
# docker run -it -d -p 8081:80 --name=result --link db:db result-app

5 woekr 
# cd voating-app/worker
# docker build -t worker . 
# docker run -it -d --name=worker --link db:db --link redis:redis worker
