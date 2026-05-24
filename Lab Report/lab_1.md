## Title: How to install Docker and their propose

# Aim:
To understand and implement containerization using Docker for building, deploying, and running applications in isolated environments. 

# Objectives:
1.	To understand the concept and purpose of Docker in modern application development. 
2.	To learn the step-by-step process of installing Docker on a system. 
3.	To explore the basic components of Docker such as images, containers, and Docker Engine. 
4.	To execute basic Docker commands for creating and managing containers. 
5.	To analyze the advantages of using Docker for application deployment and environment consistency. 

# Theory:
Docker is containerization software that allows developers to create containers which include an application bundled together with all its dependencies. Such containers can run reliably on any environment like during development, testing, and production.
While using traditional virtual machines is slower and bigger, Docker uses container virtualization technology to make the process fast and efficient because it shares the kernel of the OS running on it. The software operates under client-server architecture wherein the client interacts with the Docker Engine/Daemon. 

Key concepts include:
•	Docker Images: Read-only templates used to create containers. 
•	Docker Containers: Running instances of Docker images. 
•	Dockerfile: A script containing instructions to build Docker images. 
•	Docker Hub: A cloud-based repository for sharing Docker images. 
Docker is widely used in DevOps, continuous integration/continuous deployment (CI/CD), microservices architecture, and cloud computing due to its scalability and portability.

## Procedure

# Step 1: Download Docker
•	Visit the official Docker website: https://www.docker.com 
•	Download Docker Desktop for your operating system (Windows/Mac). 

# Step 2: Install Docker
•	Run the installer. 
•	Follow on-screen instructions. 
•	Enable required features such as WSL 2 (for Windows). 

# Step 3: Start Docker
•	Launch Docker Desktop. 
•	Wait until Docker Engine starts running.

# Step 4: Verify Installation
•	Open terminal/command prompt and run:
•	docker -version

# Step 5: Run a Test Container
•	docker run hello-world
•	This command downloads a test image and runs it in a container. 

# Step 6: Pull an Image
•	docker pull nginx

# Step 7: Run a Container
•	docker run -d -p 8080:80 nginx
•	Open browser and go to http://localhost:8080 

# Step 8: Check Running Containers
•	docker ps

# Step 9: Stop Container
•	docker stop <container_id>

# Purpose of Docker
The main purpose of Docker is to allow for building, packing and executing applications within a container. This way it ensures that applications are portable and work properly in all environments because it packs not only the code itself but also its dependences.
This tool can make software deployment easier as it addresses problems related to environments and allows for scalable and fast development. Docker is frequently used in DevOps, CI/CD and for creating microservices architecture.

##  Conclusion

During this lab session, Docker installation and testing were done successfully. It was shown how Docker makes application deployment easy through containerization. It offers consistency in various environments and increases efficiency in software development. Docker being lightweight and scalable makes it a crucial component of modern DevOps.

## References
1.	Docker Inc. (2025). Docker Documentation. Available at: https://docs.docker.com/ 
2.	Merkel, D. (2014). Docker: Lightweight Linux Containers for Consistent Development and Deployment. Linux Journal. 
3.	Pahl, C. (2015). Containerization and the PaaS Cloud. IEEE Cloud Computing. 
4.	Turnbull, J. (2014). The Docker Book: Containerization is the New Virtualization. 
5.	Poulton, N. (2023). Docker Deep Dive. Leanpub.
