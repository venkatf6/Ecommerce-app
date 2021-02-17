FROM ubuntu:latest

#install node into container 
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y nodejs 
RUN apt-get install -y npm

#setting working directory for container
WORKDIR /frontend

#copy your source code to container working directory && #copy package.json and install all the dependencies
COPY . /frontend
RUN npm install

#If environment changed due to npm install 
RUN npm rebuild node-sass

#exposing port no.
EXPOSE 4200
#command to run the server
CMD ng serve -o
