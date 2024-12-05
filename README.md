# AWS Secure VPC Design with Public and Private Subnets

## Overview
This project demonstrates how to create a secure **Virtual Private Cloud (VPC)** on AWS with public and private subnets, following principles of the **AWS Well-Architected Framework**.

### Key Components
- **Custom VPC**: `10.0.0.0/16` CIDR block
- **Public Subnet**: `10.0.1.0/24`
- **Private Subnet**: `10.0.2.0/24`
- **Internet Gateway**: For public internet access
- **NAT Gateway**: For secure outbound traffic from private instances
- **EC2 Instances**: Public instance (jump box) and private instance

### Well-Architected Framework Pillars
- **Security**: Isolated private resources with no direct internet access.
- **Reliability**: NAT Gateway for secure internet access for private resources.
- **Cost Optimization**: Used AWS Free Tier resources (t2.micro instances).

### Steps to Recreate
1. Set up a custom VPC with public and private subnets.
2. Attach an Internet Gateway and set up a NAT Gateway.
3. Configure route tables for public and private subnets.
4. Launch EC2 instances in both subnets and connect to the private instance via the public instance.
5. Test internet connectivity from the private instance using the NAT Gateway.

### Screenshots
#### Custom VPC and Subnets
![Custom VPC](screenshots/custom_vpc.png)

#### NAT Gateway
![NAT Gateway](screenshots/nat_gateway.png)

#### Internet Gateway
![Internet Gateway](screenshots/internet_gateway.png)

#### Successful Ping Test
![Ping Test](screenshots/ping_test.png)

