FROM ubuntu:latest
#Update and Upgrade
RUN apt-get update
RUN apt-get -y  upgrade

#installing mongodb into container
RUN apt-get install -y mongodb

#Installing node into continer 
RUN apt-get install -y nodejs
RUN apt-get install -y npm

#Setting up Working directory
WORKDIR /backend

#Copy backend code to working directory
COPY . /backend/
RUN npm install 

#Command to start your application 
CMD node server.js 

