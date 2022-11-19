
# docker-configuration


# How to create a docker for Angular app


<pre>
first step is to run :

ng build 



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

see more here :
https://javascript.plainenglish.io/how-to-dockerize-angular-application-3cd67e963832
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04
https://phoenixnap.com/kb/docker-portainer-install

Eclipse :
https://stackoverflow.com/questions/18589590/eclipse-autocomplete-change-variable-names


How to setup vnc server on rasberry pi - Linux

sudo apt-get update
sudo apt-get upgrade
sudo apt-get install xrdp


port forwarding 3389



