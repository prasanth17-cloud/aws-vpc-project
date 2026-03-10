# 🌐 AWS VPC Network Configuration

A hands-on project demonstrating how to design and configure a secure private network on AWS using Virtual Private Cloud (VPC).

---

## 📌 Project Overview

This project involves setting up a complete AWS network infrastructure using VPC, including public and private subnets, routing, peering, and endpoint services.

---

## 🛠️ Tools & Services Used

- AWS VPC
- EC2 (Elastic Compute Cloud)
- Internet Gateway
- Route Tables
- VPC Peering
- VPC Endpoint
- Subnets (Public & Private)

---

## 📋 What I Did — Step by Step

### 1. Created a Custom VPC
- Created a new VPC with a custom CIDR block (e.g., `10.0.0.0/16`)
- Enabled DNS resolution and DNS hostnames

### 2. Created Subnets
- Created a **Public Subnet** (`10.0.1.0/24`) — for resources accessible from the internet
- Created a **Private Subnet** (`10.0.2.0/24`) — for internal resources only

### 3. Configured Internet Gateway
- Created and attached an Internet Gateway to the VPC
- Updated the **Public Route Table** to route internet traffic through the gateway

### 4. Launched EC2 Instances
- Launched an EC2 instance in the **Public Subnet** (accessible via SSH)
- Launched an EC2 instance in the **Private Subnet** (internal only)

### 5. Configured VPC Peering
- Created a VPC Peering connection between two VPCs
- Updated route tables in both VPCs to allow traffic between them
- Tested connectivity between instances in peered VPCs

### 6. Set Up VPC Endpoint
- Created a VPC Endpoint to allow private EC2 instances to connect to AWS S3
- Without this, private instances would need internet access to reach S3

---

## 🏗️ Architecture Diagram

```
Internet
    |
Internet Gateway
    |
Public Subnet (10.0.1.0/24)
    |--- EC2 Instance (Web Server)
    |
Private Subnet (10.0.2.0/24)
    |--- EC2 Instance (Database/App)
    |
VPC Endpoint -----> S3 Bucket
    |
VPC Peering ------> Second VPC
```

---

## 🎯 Key Learnings

- Difference between public and private subnets
- How routing tables control traffic flow
- How VPC Peering enables communication between isolated networks
- How VPC Endpoints provide secure access to AWS services without internet

---

## 👨‍💻 Author

**Prasanth S**  
Cloud & DevOps Enthusiast | AWS | Linux | DevOps  
📧 prasanthprasanthleo@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/prasanth-14a620255)
