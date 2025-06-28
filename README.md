# Password Management System in AWS 

This project demonstrates the deployment of a secure, self-hosted password management system using **Passbolt** on **AWS Cloud**. It focuses on enhancing password security through centralized, encrypted storage, and cloud-based deployment.

## 🔐 Project Overview

The Password Management System aims to:
- Provide a secure platform to store and manage complex passwords.
- Leverage AWS infrastructure for reliable and scalable hosting.
- Enable HTTPS encryption for secure data transmission.
- Simplify domain management for easy access to the password manager.

## 🚀 Key Features

- 🛡️ **Self-Hosted Passbolt**: Secure, open-source password manager tailored for team use.
- ☁️ **AWS Deployment**: Hosted on AWS EC2, ensuring high availability and performance.
- 🔐 **HTTPS Encryption**: Ensures encrypted communication between users and the server.
- 🌐 **Domain Configuration**: Custom domain configured and secured for access.
- 🔏 **Secure Password Storage**: User-friendly and encrypted storage for passwords and secrets.

## 🧰 Technologies Used

- AWS EC2
- Passbolt
- NGINX (for reverse proxy and HTTPS)

 ## 🛠️ Implementation Steps

### 1. AWS Console Homepage  
![AWS Console](images/aws_homepage.png)  
This screenshot shows the AWS homepage where cloud services like EC2 and Route 53 are accessed. It was the starting point for launching and configuring the virtual machine hosting Passbolt.


### 2. VirtualBox Download Page  
![VirtualBox Download](images/virtualbox_download.png)  
This image shows the official VirtualBox download page. VirtualBox was initially used to locally test and simulate the Passbolt deployment before migrating to the AWS cloud infrastructure.


### 3. Ubuntu 22.04 LTS Download Page  
![Ubuntu Download](images/ubuntu_download.png)  
Ubuntu 22.04 LTS was selected as the base OS for the EC2 instance. This screenshot shows the official download page, highlighting the latest long-term support version ideal for server deployment.
