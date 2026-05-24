## Title: Installation and Setup of Jenkins

# Aim:
To study and implement Jenkins for automating the process of building, testing, and deploying software applications using Continuous Integration and Continuous Delivery (CI/CD).

# Objective:
•	To understand the concept of Jenkins and CI/CD 
•	To install Jenkins on a local system 
•	To configure Jenkins and create an admin user 
•	To explore the Jenkins dashboard

# Theory:
Jenkins is an open-source automation tool used for Continuous Integration (CI) and Continuous Delivery (CD). It helps developers automate tasks like building, testing, and deploying applications.
Jenkins works by monitoring version control systems such as Git. When changes are detected, Jenkins automatically triggers build and test processes.

It supports integration with various tools including:
•	Docker 
•	Build tools (Maven, Gradle) 
•	Testing frameworks 

# Introduction:
Jenkins is a widely used open-source automation tool that plays a key role in modern software development practices, particularly in Continuous Integration (CI) and Continuous Delivery (CD). It helps developers automate repetitive tasks such as building, testing, and deploying applications, thereby improving efficiency and reducing manual errors.

In traditional software development, integrating code changes and testing them manually can be time-consuming and error-prone. Jenkins solves this problem by automatically detecting changes in version control systems like Git and triggering predefined processes such as compilation, testing, and deployment.

Jenkins provides a web-based interface and supports a large number of plugins, allowing it to integrate with various tools and technologies including Docker. This flexibility makes Jenkins a powerful and scalable solution for automating the software development lifecycle.

# Procedure

Step 1: Pull and Run Jenkins Image
- docker run jenkins/jenkins:latest
Downloads the official Jenkins image from Docker Hub and starts the container.

Step 2: View Running Containers
- docker ps
Lists all currently running containers to confirm Jenkins is active.

Step 3: View All Containers
- docker ps -a
Shows all containers including stopped ones, useful for checking container history.

Step 4: Run Jenkins in Detached Mode
- docker run -d jenkins/jenkins sleep 200
Runs the Jenkins container in the background (-d = detached mode) for 200 seconds.

Step 5: Inspect Container
- docker inspect <container-id>
Provides detailed information about the container including the IP address and port number needed to access Jenkins.

Step 6: Stop Running Container
- docker stop <container-id>
Before mapping ports, the previously running container must be stopped to avoid conflicts.

Step 7: Run Jenkins with Port Mapping
- docker run -p 8080:8080 jenkins/jenkins:latest
•	-p 8080:8080 maps host port 8080 to container port 8080
•	Open browser and go to http://localhost:8080
•	Copy the admin password shown in the terminal and paste it into the browser to unlock Jenkins
•	Create an admin user and complete the setup

# Jenkins Dashboard:
Once logged in, the Jenkins dashboard is accessible where jobs, pipelines, and configurations can be managed.

## Conclusion
The installation and configuration of Jenkins using Docker has been successfully achieved in this practical. Through the pulling of the official Jenkins image and the creation of the container with port mapping -p 8080:8080, Jenkins can be accessed using the browser by navigating to http://localhost:8080.

This was achieved through checking the container network status, killing any competing containers and logging into Jenkins using the generated admin password.

From this hands-on session, it became evident that Jenkins is a highly effective tool for automation in CI/CD which helps to automate the process of building and testing of code. By using this software in conjunction with software like Git and Docker, an entirely automated pipeline for the development of software becomes possible.

## References
Jenkins. (2024). Jenkins user documentation. Jenkins. https://www.jenkins.io/doc/
Docker Inc. (2024). Jenkins official Docker image. Docker Hub. https://hub.docker.com/_/jenkins
Smart, J. F. (2011). Jenkins: The definitive guide. O'Reilly Media.
Docker Inc. (2024). Docker documentation: Get started. Docker. https://docs.docker.com/get-started/
