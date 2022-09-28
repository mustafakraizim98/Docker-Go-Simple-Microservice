# Docker-Go-Simple-Microservice

## Overview

A simple Go server/microservice example, the sample application is a minimal HTTP server that has only three features:

- It responds with a text message containing a heart symbol (“<3”) on requests to /.
- It responds with {"Status" : "OK"} JSON to the health check request on requests to /ping.
- The port it listens on is configurable using the environment variable HTTP_PORT. The default value is 8080.

Thus, it somewhat mimics enough basic properties of a REST microservice to be useful for starting with Docker.

## For the Dockerfile
That file contains comments that describe every line in it, for more information you can visit the official documentation on
[Build your Go image](https://docs.docker.com/language/golang/build-images/).

## Docker Commands:
building the image:
> docker build -t docker-go-microservice-ping .

![Screenshot 2022-09-29 023318](https://user-images.githubusercontent.com/113289516/192906526-d4b80728-0df6-4aef-a512-8dcb0ae2ba46.png)



runing the image inside a container:
> docker run -d -i -p 8080:8080 --name restful-server docker-go-microservice-ping 

![Screenshot 2022-09-29 023359](https://user-images.githubusercontent.com/113289516/192906567-77a32c22-49d4-486b-8d34-c33cf833e1b3.png)

Success! We were able to connect to the application running inside of our container on port 8080.

For more details to get familiar with docker commands, the best resource is always from the main source 
[Run your image as a container](https://docs.docker.com/language/golang/run-containers/).
