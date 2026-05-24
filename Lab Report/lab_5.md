## Title: Pushing Docker Image to the Registry (Docker hub)

# Aim: 
To push a locally created Docker image to Docker Hub and understand the structure and purpose of each instruction in a Dockerfile.

# Objectives
•	To tag and push a local Docker image to Docker Hub
•	To understand the structure of a Dockerfile
•	To learn the role of each Dockerfile instruction

# Theory
Docker Hub is a cloud-based registry where Docker images can be stored, shared, and accessed from anywhere. A locally built image must be tagged with a username and pushed to Docker Hub to make it available online.

Dockerfile Structure: A Dockerfile is a set of instructions that tells Docker how to build an image. Each instruction adds a layer to the image.

# Instruction	   Purpose
FROM	          Sets the base/foundation image
WORKDIR	          Sets the working directory inside the container
COPY	          Transfers files from host into the container
RUN	              Executes commands during image build
EXPOSE	          Documents the port the container listens on
CMD	              Defines the command to run when container starts

Base Image is the starting point of a Docker image — a pre-built foundation layer. Examples include:
•	python:3.10 — Python environment
•	node:18 — Node.js environment
•	alpine — Lightweight Linux
•	ubuntu — Full Ubuntu Linux

Requirements
•	Docker installed on the system
•	Docker Hub account
•	A locally built Docker image
•	Internet connection

## Procedure
Step 1: View Local Images
•	docker images

Step 2: Tag the Image with Docker Hub Username
•	docker build .-t username/imagename
-	Docker push username /imagename:letast
 
Step 3: Push the Image to Docker Hub
docker push username/imagename:latest

# Structure of docker file
FROM (foundation): <BASEIMAG>
Workdir: <app-directory>
Copy:<files>
RUN:<installs département
EXPOSE:<Port>
CMD (the operation): “run”,”app”

# Baise image
Is the starting point of docker image. Also known as foundation layer, starting, prebuild.
Eg, python :3.10, node:18, ngx, ubuntu, alpine

Ngx: is a high-performance, open-source web server and reverse proxy

Ubuntu: is a popular, open-source Linux operating system. In Docker, ubuntu is used as a base image when you need a full Linux environment to install and run your application manually.
Alpine: small light weight Linux

# COPY TRANSFERS CODE INTO THE CONTAINER
Converted code into container

# EXPOSE DOCUMENTS

NETWORK REQUIREMENTS

FROM python:3.10-slim: start from exit image that have already have python install.
WORKDIR /app:insider the conter tride / app is the current folder  
COPY. : coye everything from current folder into the contains
First. : represent host
Second. : represent the countering /app

RUN pip install flask: will bulidine imaje instaill  flask

EXPOSE 8080: port mapp
Task: From node 18
Workdir /app
Copy run npm install
Export 8080
Cmd :”node srever.js”

## Conclusion
In this practical, we learnt how to upload our own locally built Docker image on the Docker Hub. This was done by tagging the image with a username and pushing the image using the docker push command. We also verified this process online via Docker Hub dashboard through the Tags tab.
Furthermore, we looked into the structure of a Dockerfile. Every line of code in the Dockerfile has its own purpose in the creation of the Docker image. Some of these lines include FROM, WORKDIR, COPY, RUN, EXPOSE and CMD. As part of learning this, we also created a Dockerfile for Node.js application.

## References
Docker Inc. (2024). Docker documentation: Docker Hub. Docker. https://docs.docker.com/docker-hub/
Docker Inc. (2024). Dockerfile reference. Docker. https://docs.docker.com/engine/reference/builder/
Mouat, A. (2015). Using Docker: Developing and deploying software with containers. O'Reilly Media.
Turnbull, J. (2014). The Docker book: Containerization is the new virtualization. James Turnbull.

