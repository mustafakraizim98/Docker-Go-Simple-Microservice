# Docker-Go-Simple-Microservice

## Overview

A simple Go server/microservice example, the sample application is a minimal HTTP server that has only three features:

- It responds with a text message containing a heart symbol (“<3”) on requests to /.
- It responds with {"Status" : "OK"} JSON to the health check request on requests to /ping.
- The port it listens on is configurable using the environment variable HTTP_PORT. The default value is 8080.

Thus, it somewhat mimics enough basic properties of a REST microservice to be useful for starting with Docker.
