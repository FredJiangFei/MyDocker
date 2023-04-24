clean 
### docker image rm $(docker image ls -aq)
### docker container rm -f $(docker image ls -aq)

build image 
### docker-compose build
### docker-compose build --no-cache

build image 
### docker-compose up

docker networking(????????????????????????????????????????????????) 
### docker network ls
bridge
host

view logs 
### docker-compose logs

### publish changes (not working)
volumes:
      - ./backend:/app

### migrate database
docker-entrypoint.sh > ....


### run test

