# Multi-Tier Application on AWS (Cloud Internship Assignment)

This project demonstrates how to create a secure multi-tier architecture on AWS using CloudFormation.  
It includes a VPC with public and private subnets, an EC2 instance in the public subnet, and an RDS MySQL database in the private subnet.

## ✅ Objective

- Create a secure and scalable VPC with:
  - 1 Public Subnet
  - 1 Private Subnet
  - Internet Gateway
  - NAT Gateway
  - Route Tables
- Launch an EC2 instance in the Public Subnet.
- Launch an RDS MySQL database in the Private Subnet (no public access).
- Install MySQL client on the EC2 instance.
- Test the connection from EC2 to RDS.

## 🏗️ Architecture Diagram
![Screenshot 2025-07-01 170704](https://github.com/user-attachments/assets/325fb316-4331-480f-ab4b-e5e9d7a577d7)


## 🧾 Files

| File                          | Description                                    |
|-------------------------------|------------------------------------------------|
| `cloudformation/multi-tier-app.yaml` | CloudFormation script to set up VPC, EC2, RDS |
| `README.md`                   | This file, explains architecture & usage       |

## 🚀 Deployment Steps

1. Go to **AWS CloudFormation** Console.
2. Upload the `multi-tier-app.yaml` file.
3. Deploy the stack with required parameters.
4. SSH into EC2 and install MySQL client:

   ```bash
   sudo yum install mysql -y

Connect to RDS MySQL using endpoint:

mysql -h <RDS-ENDPOINT> -u <USERNAME> -p

