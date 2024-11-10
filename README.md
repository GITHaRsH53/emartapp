# emart-app

In this project we will see deployment of microservice application.
In the front end we have an API GATEWAY created with NGINIX which listens at 3 endpoints /root, /API and /web Api.
When the user access the URL of the website, it'll be redirected to root, which is an app written in Angular. (This will give the front end also called client app)
And this will in turn connect to /API which will be served by an application E-Mart api NodeJS. And it also needs MongoDB Database(container).
This application also has slash web API which connects to an application, Books API, which is written in Java and this also needs a database, a MySQL Database.
So all these apps that you see over here, Nginx, Angular, NodeJS, Java, Mongo, MySQL, all these will be containers. 
E-Mart app represents an e-commerce application, like Amazon, Flipkart. And then application can start like this and you can keep adding more microservices like maybe another URL for videos, another URL for payment gateway, another URL for cart. So you see, it's very scalable from a developer point of view as well.

Steps:

1)
Get the vagrant file in your directory (have 2gb ram and contains cmds to install docker)
So we brought up the vm using vagrant and it installed the docker engine.
Cmds ->vagrant up, ssh , sudo -i

1)
After cloning the emartapp repo go to the emartapp directory.
Docker compose – shows options of docker (helps in building image and run container from that)
(it requires to read  dockercompose.yaml -> this file is brought from github clone it or create vim editor and copy script from the folder)

Cmds -> docker compose up -d (brings up all the container after reading .yaml file and after some time containers are up. (build images also))
 
Cmds -> docker compose ps -> To check if all containers are up , docker images  to see all the images
if it shows all the images means all the containers are created .

3)
ip addr show -> to get ip of the vm and see ip of the form 192.168.
go to chrome and search for theurl -> http://"ip address"

This is a glimpse of how a microservice application runs on docker
