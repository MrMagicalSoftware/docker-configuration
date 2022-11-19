
<pre>
# docker-configuration


# How to create a docker for Angular app

first step is to run :

ng buld 



Second Step :

Create a file with name Dockerfile (No extension) :

FROM node:18.12.1 as node
WORKDIR /app
COPY . .

FROM nginx:alpine
COPY --from=node /app/dist/app/ /usr/share/nginx/html


Third Step :

sudo docker build - t app .


How to Run :

sudo docker run -dp: 80:80 app


How to stop container :

sudo docker ps
sudo docker stop ID_OF_CONTAINER

</pre>



