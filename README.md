# RoboShop Deployment using Ansible Roles 🚀

This project demonstrates production-style automation of the RoboShop microservices application using Ansible Roles and Dynamic Inventory (AWS EC2).

It follows best practices like modular roles, reusable configurations, and scalable infrastructure automation.

---

## 🏢 Project Overview

RoboShop is a microservices-based e-commerce application.

This repository uses:
- Ansible Roles for modular automation
- Dynamic Inventory for AWS EC2
- Group variables for environment configuration

---

## 🏗️ Architecture

Frontend (Nginx)  
↓  
Application Services (Catalogue, Cart, User, Payment, Shipping)  
↓  
Databases & Messaging (MongoDB, MySQL, Redis, RabbitMQ)

---

## ⚙️ Tech Stack

- Ansible (Roles & Playbooks)
- AWS EC2 (Dynamic Inventory)
- Linux (RHEL / CentOS)
- Nginx
- MongoDB, MySQL
- Redis, RabbitMQ

---

## 📂 Repository Structure

### 📁 Roles
Each service is implemented as an independent role:

- roles/catalogue
- roles/cart
- roles/user
- roles/payment
- roles/shipping
- roles/frontend
- roles/mongodb
- roles/mysql
- roles/redis
- roles/rabbitmq

---

### 📁 Group Variables
- group_vars/ → Common variables for all environments

---

### 📁 Inventory
- inventory.ini → Static inventory
- frontend.aws_ec2.yaml → Dynamic inventory (AWS)

---

### 📁 Playbooks
- roboshop.yaml → Main playbook
- main.yaml → Entry-level execution
- include-vs-import.yaml → Ansible concepts demo

---

## 📌 Prerequisites

- Ansible installed
- AWS CLI configured
- EC2 instances running
- SSH access to servers

---

## 🛠️ Setup

### Install Ansible

```bash
sudo yum install ansible -y
Configure AWS Dynamic Inventory
pip install boto boto3

Update dynamic inventory file:

frontend.aws_ec2.yaml
▶️ Execution
Run using static inventory
ansible-playbook -i inventory.ini roboshop.yaml
Run using dynamic inventory
ansible-playbook -i frontend.aws_ec2.yaml roboshop.yaml
🔄 What This Project Does
Uses roles for modular automation
Deploys all RoboShop services
Configures databases and messaging systems
Uses dynamic inventory for AWS EC2
Enables reusable and scalable deployments
🧪 Validation
systemctl status catalogue

Access application:

http://<server-ip>
🎯 Real-Time Use Cases
Enterprise Ansible automation
Scalable infrastructure deployment
AWS-based provisioning
Configuration management using roles
💡 Key Highlights
Role-based architecture
Dynamic inventory (AWS EC2)
Reusable and modular design
Production-like setup
📈 Learning Outcome
Deep understanding of Ansible Roles
Dynamic inventory usage
Infrastructure automation at scale
DevOps best practices
🤝 Contributions

Feel free to fork and raise PRs.

⭐ Support

Give a star ⭐ if useful

👨‍💻 Author

Kulasekhar-A
