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
![AWS Console](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/c2287f02f9955cf8b4f58d0b02ca0127a5e67217/Images/1.png)  
This screenshot shows the AWS homepage where cloud services are accessed. It was the starting point for launching and configuring the virtual machine hosting Passbolt.

### 2. VirtualBox Download Page  
![VirtualBox Download](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/c2287f02f9955cf8b4f58d0b02ca0127a5e67217/Images/2.png)  
This image shows the official VirtualBox download page. VirtualBox was initially used to locally test and simulate the Passbolt deployment before migrating to the AWS cloud infrastructure.

### 3. Ubuntu 22.04 LTS Download Page  
![Ubuntu Download](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/c2287f02f9955cf8b4f58d0b02ca0127a5e67217/Images/3.png)  
Ubuntu 22.04 LTS was selected as the base OS for the EC2 instance. This screenshot shows the official download page, highlighting the latest long-term support version ideal for server deployment.

### 4. Namecheap Domain Registration  
![Namecheap Domain Registration](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/2c0a7a9f2bb3bc82a2313347bca691d838e5ad9a/Images/4.png)  
This screenshot shows the Namecheap domain registration page, which was used to acquire and configure the domain for the Passbolt instance, enabling secure access via a custom domain name.

### 5. Passbolt Homepage  
![Passbolt Homepage](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/2c0a7a9f2bb3bc82a2313347bca691d838e5ad9a/Images/5.png)  
This is the official Passbolt homepage, where users can access information about the product and begin either the on-premises installation or cloud setup of the password manager.

### 6. Passbolt Pricing Plans  
![Passbolt Pricing](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/2c0a7a9f2bb3bc82a2313347bca691d838e5ad9a/Images/6.png)  
This screenshot outlines Passbolt’s pricing tiers—Community (Free), Business, and Enterprise. The self-hosted Community edition was chosen for this project, providing secure password management with no user limit.

### 7. Passbolt AWS Deployment Option  
![Passbolt AWS Deployment](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/2c0a7a9f2bb3bc82a2313347bca691d838e5ad9a/Images/7.png)  
This image shows the deployment options for Passbolt, highlighting AWS as the selected cloud provider. The project utilized this to host the self-managed Passbolt server on a secure EC2 instance.

### 8. 🛠️ Passbolt Community Edition - AWS Deployment Start Guide

![Passbolt AWS Deployment Start Guide](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/6881e2392cf443865c70c9fc7141452635f59e0e/Images/8.png)

This image shows the initial setup page for deploying Passbolt Community Edition on AWS. It highlights a one-click option to deploy the Passbolt CE AMI, followed by instructions for configuring the server and creating the first admin user. Options for native installations (Docker, Kubernetes, Ubuntu, etc.) are also visible on the left.


### 9. 📦 Passbolt CE AMI on AWS Marketplace

![Passbolt CE AMI on AWS Marketplace](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/6881e2392cf443865c70c9fc7141452635f59e0e/Images/9.png)

This screenshot displays the AWS Marketplace listing for the Passbolt Community Edition AMI. It includes version details, OS compatibility (Debian 10), and highlights such as being API-first, secure by design, and team collaboration-friendly. The typical infrastructure pricing is also mentioned.


### 10. 💰 Passbolt CE AWS Pricing Breakdown

![Passbolt CE AWS Pricing Breakdown](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/6881e2392cf443865c70c9fc7141452635f59e0e/Images/10.png)

This image provides a detailed pricing estimate for running Passbolt CE on different EC2 instance types. It includes a breakdown of software costs ($0/hr), EC2 hourly costs, and highlights the Free Tier eligibility (e.g., t2.micro for 750 hours/month). The vendor-recommended instance type, t2.medium, is selected, with a total cost of $0.046/hr.

## 11. ⚙️ Configure Passbolt AMI Before Launch

![Configure Passbolt AMI Before Launch](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/aa74c2e7ebcabc32edd7ba2294094e27d4691914/Images/11.png)

This image shows the configuration screen on AWS Marketplace for launching the Passbolt Community Edition AMI. It includes selection of fulfillment option, software version, and region. On the right, estimated infrastructure pricing is displayed (e.g., $33/month for a `t2.medium` instance).


## 12. 🔒 Set Up Security Group for Passbolt

![Set Up Security Group for Passbolt](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/aa74c2e7ebcabc32edd7ba2294094e27d4691914/Images/12.png)

This step involves configuring the security group to control traffic for your Passbolt instance. Users are guided to create a new group based on seller-recommended settings to streamline the firewall rules setup.


## 13. 📋 Define Security Group Rules

![Define Security Group Rules](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/aa74c2e7ebcabc32edd7ba2294094e27d4691914/Images/13.png)

Here, users can name the security group, add a description, and view pre-configured inbound rules. SSH (port 22), HTTP (port 80), and HTTPS (port 443) are enabled for all IPs (`0.0.0.0/0`), with a caution to restrict access to known IPs for better security.

## 14. 🔑 Create or Select a Key Pair

![Create or Select a Key Pair](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/aa74c2e7ebcabc32edd7ba2294094e27d4691914/Images/14.png)

To secure access to the EC2 instance running Passbolt, users must select an existing key pair or create a new one in EC2. This ensures only authorized users can SSH into the server.

## 15. Import Key Pair Dialog - Initial Setup
![Import Key Pair Dialog](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/15.png)

The AWS EC2 "Import Key Pair" dialog showing the initial setup form with fields for Name, Key pair file selection, and optional Tags. The interface allows users to either browse for a key file or paste public key contents directly into the text area.

## 16. SSH Key Generation Process
![SSH Key Generation](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/16.png)

Terminal output showing the `ssh-keygen` command execution for generating an RSA key pair. The process shows the key being saved to `/home/ph/.ssh/id_rsa` with the generated fingerprint and randomart image displayed for verification.

## 17. Public Key File Content
![Public Key Content](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/17.png)

Terminal display of the generated RSA public key content using `cat ~/.ssh/id_rsa.pub` command. The output shows the complete SSH-RSA public key string that will be imported into AWS EC2.

## 18. Import Key Pair - Populated Form
![Import Key Pair Populated](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/18.png)

The AWS EC2 Import Key Pair dialog with the form completed - showing "passbolt" as the key name and the RSA public key content pasted into the Public key contents text area, ready for import.

## 19. Successful Key Pair Import
![Key Pair Import Success](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/19.png)

AWS EC2 console showing the successful import confirmation with a green success banner "Successfully imported key pair". The Key pairs list displays the newly imported "passbolt" RSA key with creation timestamp and fingerprint information.

## 20. Passbolt AMI Deployment Success
![Passbolt Deployment Success](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/20.png)

Passbolt Community Edition AMI deployment success page showing congratulations message, AMI ID (ami-00b5e8404c22acd24), and configuration details including software version 3.12.0-3 running on t2.medium instance type with usage instructions available.

## 21. EC2 Instances Dashboard
![EC2 Instances Dashboard](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/21.png)

AWS EC2 Instances dashboard showing a list of 3 instances with their details including Instance IDs, states (Terminated, Running), instance types (t2.medium), status checks, and availability zones. The running instance shows public IPv4 address and DNS information.

## 22. Instance Summary Details
![Instance Summary Details](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/22.png)

Detailed view of EC2 instance `i-01c52435188a7cbfb` showing comprehensive information including public/private IP addresses (184.72.186.119/172.31.44.15), instance state (Running), VPC details, subnet information, and AMI details for the Passbolt deployment.

## 23. Passbolt Initial Configuration Welcome
![Passbolt Configuration Welcome](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/23.png)

Passbolt welcome screen showing the initial configuration setup with system check status. The interface displays a step-by-step configuration process (8 steps total) with environment status checks, GPG configuration confirmation, and SSL access warning notification.

## 24. Domain DNS Configuration
![Domain DNS Configuration](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/24.png)

Domain management interface for `passbolt.world` showing the Advanced DNS tab with host records configuration. The interface displays an A Record pointing to IP address 184.72.186.119 with automatic TTL settings, along with DNSSEC and email forwarding options.

## 25. SSH Connection to Passbolt Instance
![SSH Connection](https://github.com/rakshitbhari/-Password-Managment-System-in-AWS/blob/f72b98d1b5d246c4c194d2f9ec6554083eda9a23/Images/25.png)

Terminal output showing SSH connection attempt to the Passbolt EC2 instance at IP 184.72.186.119. The connection displays host authenticity verification with ED25519 key fingerprint and confirms successful addition of the host to the known_hosts file.



