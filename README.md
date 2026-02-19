# 🚀DevOps Project: Two-Tier Application with Automated CI/CD Pipeline

🧠Project Overview

A two-tier web application that is containerized using Docker and deployed on Azure Virtual Machine with fully automated CI/CD pipeline using Jenkins and GitHub webhooks. Users can submit and view messages through a Flask web interface, with all data stored persistently in MySQL database.


⚙️Technology Stack

**Cloud Platform**: Microsoft Azure  
**Containerization**: Docker and Docker Compose  
**CI/CD**: Jenkins, GitHub Webhook  
**Version Control**: GitHub  
**Frontend/Backend**: Flask  
**Database**: MySQL  


🧩Architecture 
```
DEVELOPER ──→ GITHUB ──→ WEBHOOK ──→ AZURE VM ──→ USERS
              (code)     (trigger)     │             
                                       │
                                    JENKINS
                                       │
                                     DOCKER
                                       │
                               ┌───────┴───────┐
                               │               │
                             FLASK           MYSQL
                             :5000           :3306
```					 
⏳Flow

```
Developer pushes code
		 |
GitHub receives code
		 |
GitHub Webhook triggers Jenkins
		 |
Jenkins Pipeline executes
	     |
		 ├─→ Clone code from GitHub
		 ├─→ Build Docker image
	     └─→ Deploy with Docker Compose
	     |
Docker starts containers
	     |
	     ├─→ MySQL container (stores data)
	     └─→ Flask container (runs app)
	     |
Application live at :5000
```




















