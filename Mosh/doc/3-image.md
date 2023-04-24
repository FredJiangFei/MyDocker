## xxx is 10 times smaller than yyy

### build image
docker build -t react-app .
docker run -it react-app sh

### copy files ###
### COPY 
COPY . .
COPY ["hello world.txt", "."]

### ADD
ADD http://.....file.json . 从网络copyfile
ADD file.zip . 解压file

exclude files
### .dockerignore

### run command ###
### RUN
RUN npm install

### ENV
ENV APL_URL=https://jsonplaceholder.typicode.com/

### EXPOSE
EXPOSE 3000

### set user
addgroup fred && adduser -S -G fred fred

### defind entrypoints
### CMD

### RUN 和 CMD 区别
RUN image build 的时候执行
CMD container run 的时候执行

CMD npm start
CMD ["npm", "start"]

### ENTRYPOINT
### CMD 和 ENTRYPOINT 区别
can override CMD
can not overried ENTRYPOINT easy


### remove image 
docker rmi xxxxx

### docker image prune
### docker container prune
### docker image rm xxx

### tag image
### docker build -t react-app:1.0
### docker image tag react-app:latest react-app:2.0

### share image
### docker login
### docker push

### save and load image
### docker image save -o react-app.tar react-app:1.0
### docker image load -i react-app.tar