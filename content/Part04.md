+++
title = "AWS VPC"
weight = 4
+++
# 3. AWS VPC (Virtual Private Cloud)

## Objective
- Understand the purpose and components of a Virtual Private Cloud.
- Learn how to design and manage networking in AWS using VPC.
- Explore routing, subnets, gateways, peering, and security best practices.

---

## 3.1 Introduction to AWS VPC
- What is a VPC?
- Why use a VPC?
- Benefits of VPC in cloud networking

## 3.2 VPC Components Overview
- Subnets (Public vs Private)
- Route Tables
- Internet Gateway (IGW)
- NAT Gateway / NAT Instance
- Elastic IPs
- VPC Endpoints
- DHCP Options Set
- Network ACLs
- Security Groups

## 3.3 Creating a Custom VPC
- Steps to create a VPC from scratch
- CIDR block selection and planning
- Creating subnets in multiple Availability Zones
- Associating route tables with subnets

## 3.4 Public and Private Subnets
- Use cases and design patterns
- How to create and route traffic for each
- Testing internet access from different subnets

## 3.5 Internet Gateway
- Attaching and detaching IGWs
- Updating route tables to allow outbound traffic

## 3.6 NAT Gateway vs NAT Instance
- Differences and use cases
- High availability setup
- Cost and performance comparison

## 3.7 Route Tables
- Associating route tables to subnets
- Custom vs main route tables
- Routing traffic between subnets and to the internet

## 3.8 VPC Peering
- VPC-to-VPC communication
- Creating and accepting peering connections
- Limitations and routing configuration

## 3.9 VPC Endpoints
- Interface vs Gateway endpoints
- Connecting privately to AWS services like S3 or DynamoDB
- Security benefits

## 3.10 Security in VPC
- Security Groups vs NACLs
- Inbound and outbound rules
- Stateful vs Stateless behavior
- Best practices for securing subnets and traffic flow

## 3.11 Elastic IPs and ENIs
- Allocating and associating Elastic IPs
- Attaching multiple ENIs (Elastic Network Interfaces) to an instance
- Use cases for secondary ENIs

## 3.12 Monitoring and Troubleshooting
- VPC Flow Logs
- CloudWatch metrics for networking
- Troubleshooting connectivity issues

## 3.13 VPC Design Best Practices
- Multi-AZ design
- Least privilege principle in security
- Using public and private subnets effectively
- High availability and fault tolerance

## 3.14 IPv6 Support in VPC
- Enabling IPv6 in a VPC
- Dual-stack networking (IPv4 + IPv6)
- Security considerations with IPv6

## 3.15 Hybrid Networking (Advanced)
- VPN connections
- AWS Direct Connect
- Transit Gateway overview
- Hybrid architecture design tips

---

## Optional Hands-On Tasks

- [ ] Create a custom VPC with 2 public and 2 private subnets
- [ ] Launch EC2 instances in both subnet types and test internet access
- [ ] Create and test a NAT Gateway
- [ ] Set up a VPC peering connection
- [ ] Use a VPC endpoint to connect to S3 privately
- [ ] Enable VPC Flow Logs and analyze traffic patterns
