## Title:Rander

## Aim
The aim of using Render.com is to provide a simple, reliable, and scalable cloud platform for deploying and hosting web applications, APIs, databases, and Docker containers without the complexity of managing servers manually.

## Objectives
1.	To deploy a web application on Render.com and make it accessible via a live public URL.
2.	To set up automatic deployment from GitHub so that every code push triggers an automatic rebuild and redeploy.
3.	To properly configure environment variables and keep sensitive data like API keys and database URLs secure.
4.	To write a proper Dockerfile and successfully deploy the application inside a Docker container on Render.com.
5.	To create and connect a PostgreSQL database on Render.com and ensure the application can read and write data.
6.	To enable HTTPS and SSL for the deployed application to ensure security.
7.	To use Render's dashboard and logs to monitor application performance and fix errors quickly.
8.	To scale and optimize the application for fast response times and minimal downtime.

## Theoy:
1. Introduction to Render.com
Render.com is a contemporary cloud-based application hosting provider that enables programmers to host web apps, APIs, static sites, databases, and even Docker containers. This platform makes it unnecessary to manage servers manually by providing a simple way to deploy and scale up the application in the cloud environment.

2. Cloud Computing
The basis of Render.com is cloud computing. Cloud computing refers to accessing information and application services over the internet rather than using the local computer. Cloud computing infrastructure is used by render to host its applications and make them accessible to users across the globe.

3. Docker & Containerization
Docker is a platform that enables packing of an application along with all its dependencies into one package known as a container. Containers make sure that an application will run in the same way irrespective of the environment. Rendering platform offers Docker containers that mean that every application packed into a container is deployable to Render.

4. Continuous Deployment
The continuous deployment feature in Render makes sure that any time the developer uploads code changes to GitHub or GitLab, it will be automatically built and redeployed by Render. This eliminates the hassle of manual deployment and helps keep the latest build of the app online.

5. Web Services
Web service is an application deployed on a server to process requests from the client via the Internet. Developers can deploy web applications created with different frameworks such as Node.js, Python, Ruby, Go, Rust, etc. on Render.com. The web services hosted by Render run continuously day and night.

6. Static Website Hosting
Static websites consist of pre-built HTML, CSS, and JS code. Rendering.com can deliver a website hosting service that is efficient and fast thanks to a content delivery network (CDN). Content will be distributed based on the closest server to a user to speed up the load time.

7. Environment Variables
Environment variables consist of key-value pairs that store configuration and other sensitive values such as API keys, URLs, and passwords. Render makes it easy for users to store and manage environment variables without making them available within the source code.
8. Managed Databases
Render.com offers managed PostgreSQL databases. With a managed database, all the installation, configuration, backup, and maintenance are handled by the cloud service provider. The developer just has to plug their application into the database using a connection URL.

9. SSL & HTTPS
SSL stands for Secure Sockets Layer, which is a method of security where information transmitted from the user's browser to the server is encrypted. This means that all communication will be secured through SSL as Render.com provides free SSL certificates for all apps deployed.

10. Scalability
Scalability refers to either expanding or shrinking the amount of resources used by the application. Render.com allows for both vertical scaling (where there is more CPU and memory) and horizontal scaling (where there are more instances of the application).

11.Logs and Monitoring
The Render.com platform offers a log management tool which documents all the activities and errors within a deployed application. Logs can be viewed using the Render portal where one can easily track their applications.

12. Render vs Traditional Hosting
Traditional hosting involves manually managing servers, setting up software, and configuring security on the part of the developer. On the other hand, Render.com makes this process much more effortless by automatically performing all these steps.

## Procedure
Step 1: Create an Account on Render.com
•	Go to render.com
•	Click on "Get Started"
•	Sign up using GitHub, GitLab, or Email
•	Verify your account
Step 2: Prepare Your Application
•	Create your web application locally
•	Make sure your application is working correctly on your local machine
•	Create a Dockerfile in your project root

FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "server.js"]

Step 3: Push Code to GitHub
Initialize a git repository:
git init
Add all files:
git add .
Commit the code:
git commit -m "first commit"
Push to GitHub:
git push origin main 

Step 4: Connect GitHub to Render
•	Login to Render.com dashboard
•	Click "New" button
•	Select "Web Service"
•	Click "Connect GitHub"
•	Select your repository
![alt text](image7.png)
 
Step 5: Configure the Service
•	Fill in the following settings:

# Setting   	      Value
Name	          Your app name
Environment  	   Docker
Region	       Select nearest region
Branch	             main
Port	             3000
  
Step 6: Add Environment Variables
•	Go to Environment section
•	Click "Add Environment Variable"
•	Add your variables:
DATABASE_URL = your_database_url
API_KEY = your_api_key
PORT = 3000

Step 7: Create Database (Optional)
•	Click "New" → Select "PostgreSQL"
•	Give a name to your database
•	Select the free plan
•	Click "Create Database"
•	Copy the connection URL
•	Paste it in environment variables as DATABASE_URL

Step 8: Deploy the Application
•	Click "Create Web Service"
•	Render will automatically: 
o	Pull code from GitHub
o	Build the Docker image
o	Deploy the container
•	Wait for the build to complete

Step 9: Verify Deployment
•	After deployment is complete
•	Click on the live URL provided by Render
•	Example: https://your-app.onrender.com
•	Check if the application is running correctly

Step 10: Monitor the Application
•	Go to Render dashboard
•	Click on your service
•	Click "Logs" to view application logs
•	Check for any errors or issues

Step 11: Update the Application
•	Make changes to your code locally
•	Push the changes to GitHub:

## Conclusion

In conclusion, Render.com is a very useful and efficient cloud hosting service which helps deploy and manage modern web applications without much difficulty. This paper successfully illustrated the deployment process by deploying the web app using Docker with the use of the Render.com platform. The process further entailed connecting the application with GitHub so that the app would automatically be deployed. All environment variables were set up efficiently while the database was deployed via PostgreSQL. The app came with built-in SSL/HTTPS and scaling functionalities among other benefits. In a nutshell, Render.com offers better security and performance compared to normal servers.

## References 
Render Official Website
Render Documentation
Docker Official Documentation
GitHub Official Website
PostgreSQL Official Documentation
Mell, P., & Grance, T. (2011). The NIST definition of cloud computing. National Institute of Standards and Technology.
Merkel, D. (2014). Docker: Lightweight Linux containers for consistent development and deployment. Linux Journal, 2014(239), 2.
Fielding, R. T. (2000). Architectural styles and the design of network-based software architectures (Doctoral dissertation, University of California, Irvine

