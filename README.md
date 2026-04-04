# DevOps Terraform LAMP Server
End-to-End Full Stack Application Deployment using Terraform and Docker Compose

I have developed this project to demonstrate a real-world DevOps scenario. In this project, the frontend and backend code is provided by developers, and as a DevOps engineer, I have provisioned the infrastructure and deployed the complete application stack.
# 🧩 Project Overview
In this repository, I have provisioned an AWS EC2 instance using Terraform and successfully deployed a containerized full-stack application using Docker Compose.
#### The stack includes:

* React.js  – Frontend
* Spring Boot  – Backend
* MySQL  – Database
# 🏗️ Project Architecture

                ┌────────────────────────────┐
                │        User Browser         │
                └──────────────┬─────────────┘
                               │
                               │ HTTP :3000
                               ▼
                ┌────────────────────────────┐
                │        AWS EC2 Instance     │
                │                            │
                │  ┌──────────────────────┐ │
                │  │   React.js Container  │ │
                │  │      (Frontend)       │ │
                │  └──────────┬───────────┘ │
                │             │ REST API     │
                │             ▼               │
                │  ┌──────────────────────┐ │
                │  │ Spring Boot Container │ │
                │  │      (Backend)        │ │
                │  └──────────┬───────────┘ │
                │             │ JDBC          │
                │             ▼               │
                │  ┌──────────────────────┐ │
                │  │   MySQL Container     │ │
                │  │      (Database)       │ │
                │  └──────────────────────┘ │
                │                            │
                │   Docker Compose Runtime   │
                └────────────────────────────┘

Infrastructure Provisioned using Terraform
# 📁 Repository Structure  
DevOps-Terraform-LAMP-Server/  
 ├── code/                   # Frontend (React) and Backend (Spring Boot) source code  
 ├── docker-compose.yaml     # Multi-container setup (React, Spring Boot, MySQL)  
 ├── main.tf                 # Terraform infrastructure definition  
 └── README.md               # Project documentation  
 ## Expected Output:
 code  
 docker-compose.yaml  
 main.tf  
 ## 1️⃣ Terraform Configuration:
 vi main.tf
 ## 2️⃣ Unitilize Terraform:
 terraform init
 ## 3️⃣ Deploy Infrastructure and Application:
 terraform apply --auto-approve  
 # ✅ Sample Terraform Output
 Apply complete! Resources: 7 added, 0 changed, 0 destroyed.

# Outputs:

#### App-Live =  
Reactjs and Spring boot Live: http://<PUBLIC_IP>:3000  

#### Docker-compose =  
LAMP server: docker compose ps -a  

#### MYsql-Live =  
MySQL Credentials: mysql -uappuser -papppass appdb  

#### public_ip =  
Public IP address: ec2-user@<PUBLIC_IP>  

#### sshkey =  
SSH Key location: ~/.ssh/id_rsa    
# 🌐 Access the Application
* Frontend & Backend Application  
  http://<PUBLIC_IP>:3000  
* MySQL Database Access  
  mysql -uappuser -papppass appdb   
* Check Running Containers  
  docker compose ps -a  
 
 
 
