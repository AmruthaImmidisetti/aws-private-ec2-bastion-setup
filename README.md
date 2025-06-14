# aws-private-ec2-bastion-setup
# Secure Access to Private EC2 Using Bastion Host in AWS

## 🔒 Project Overview
This project demonstrates how to securely access a private EC2 instance in AWS using a Bastion Host. 
The setup follows a real-world, production-style architecture by using public and private subnets 
within a VPC and avoids exposing private EC2s to the public internet.

## ☁️ Technologies Used
- AWS EC2
- AWS VPC
- Subnets (Public & Private)
- Bastion Host (Jump Box)
- NAT Gateway
- Security Groups
- Route Tables
- SSH
- GitHub

## 📐 Architecture
> [Insert `architecture.png` here]
The setup includes:
- A VPC with public and private subnets
- Internet Gateway for public access
- NAT Gateway for outbound internet access from private subnet
- Bastion Host in the public subnet for secure SSH access
- Private EC2 in private subnet with no public IP

## 🔧 Setup Steps
Documented in [`setup-steps.md`](./setup-steps.md)

## 💻 SSH Access Flow
1. SSH into Bastion Host (public subnet)
2. From Bastion, SSH into the private EC2 instance using its private IP

## 🌐 Outbound Internet from Private EC2
- Configured a NAT Gateway in the public subnet
- Attached proper route table to allow the private EC2 instance to access the internet for updates, package installations, etc.

## 📸 Screenshots
Check the `/screenshots` folder for:
- VPC and subnet setup
- Route table configuration
- SSH connections
- NAT Gateway verification

## ✅ Key Takeaways
- Learned secure architecture design in AWS
- Gained hands-on with VPC, subnets, Bastion Host, and NAT Gateway
- Understood SSH access flow for private infrastructure
