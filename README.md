# DevOps Terraform LAMP Server
📌 Project Description

This project is developed by me to demonstrate an end-to-end DevOps workflow.

I provisioned infrastructure using Terraform and deployed a full-stack application using Docker Compose.

The application includes:
* **React.js** – Frontend
* **Spring Boot** – Backend
* **MySQL** – Database
---

## 🧩 Project Overview
In this project:

I created infrastructure using Terraform
I deployed a multi-container application using Docker Compose
I integrated frontend, backend, and database
---

## 🏗️ Project Architecture

```
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
```

---

## 📁 Repository Structure

```
DevOps-Terraform-LAMP-Server/
├── code/                   # Frontend (React) and Backend (Spring Boot) source code
├── docker-compose.yaml     # Multi-container setup (React, Spring Boot, MySQL)
├── main.tf                 # Terraform infrastructure definition
└── README.md               # Project documentation
```
---
🚀 How to Run
cd DevOps-Terraform-LAMP-Server
terraform init
terraform apply --auto-approve
---
🌐 Access Application
http://<PUBLIC_IP>:3000
---
