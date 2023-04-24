start container 
### docker run -d react-app
### docker run -d --name blue-sky react-app

view log 
### docker logs 655
### docker logs -f 655
### docker logs -n 5 655

publish port 
### docker run -d -p 80:3000 --name blue-sky react-app

stop / start / remove container 
### docker stop xxx
### docker start xxx
### docker rm xxx

file system 

volume 
### docker volume create app-data
### docker volume inspect app-data
### dcoker run -d -p 4000:3000 -v app-data:/app/data react-app

copy 
### docker cp e1c904:/app/log.txt .
### docker cp secre.txt e1c904:/app

share 
### docker run -d -p 5001:3000 -v $(pwd):/app react-app
