+++
title = "Part 01: Introduction to AWS Cloud"
weight = 1
+++

##  Introduction to AWS Cloud

## Objectives

By the end of this page, you will be able to:

- [Understand what AWS Cloud is and its evolution](#01-what-is-aws-cloud)
- [Describe AWS’s global infrastructure including Regions and Availability Zones](#03-aws-global-infrastructure)
- [Identify core AWS services and their benefits](#04-core-aws-services)
- [Recognize common use cases for AWS Cloud](#06-use-cases-for-aws-cloud)
- [Differentiate AWS from other cloud providers](#07-how-aws-differs-from-other-cloud-providers)
- [Get started with AWS and understand basic terminology](#08-getting-started-with-aws)
- [Learn about AWS account structure, support plans, and foundational concepts](#aws-account-and-infrastructure-overview)
- [Understand the AWS Well-Architected Framework and its five pillars](#aws-well-architected-framework)
- [Perform basic AWS tasks including managing EC2 instances and configuring security](#assignments)

---

## 0.1 What is AWS Cloud? <a id="01-what-is-aws-cloud"></a>

- AWS Cloud is a comprehensive and widely adopted cloud platform offered by Amazon, providing on-demand computing resources and services such as storage, databases, analytics, and networking over the internet.

## 0.2 History and Evolution of AWS

- AWS was launched in 2006 as one of the first cloud service providers. It has rapidly evolved from simple infrastructure services to a vast ecosystem of scalable, secure, and flexible cloud solutions used globally.

## 0.3 AWS Global Infrastructure <a id="03-aws-global-infrastructure"></a>

- AWS's global infrastructure consists of data centers grouped into **Regions** and **Availability Zones (AZs)**, strategically located worldwide to provide high availability, fault tolerance, and low latency.

## 0.4 Core AWS Services <a id="04-core-aws-services"></a>

- Core AWS services include:
  - **EC2** (Elastic Compute Cloud) for virtual servers
  - **S3** (Simple Storage Service) for scalable storage
  - **RDS** (Relational Database Service) for managed databases
  - **Lambda** for serverless computing
  - And many more...

## 0.5 Benefits of AWS Cloud

- AWS offers benefits such as:
  - Cost efficiency through pay-as-you-go pricing
  - Scalability to handle varying workloads
  - Robust security features
  - Global presence for high availability and performance

## 0.6 Use Cases for AWS Cloud <a id="06-use-cases-for-aws-cloud"></a>

- AWS supports use cases like:
  - Hosting websites and applications
  - Big data analytics
  - Disaster recovery
  - IoT applications
  - Machine learning workloads

## 0.7 How AWS Differs from Other Cloud Providers <a id="07-how-aws-differs-from-other-cloud-providers"></a>

- AWS stands out due to:
  - Early market entry and maturity
  - Extensive service portfolio
  - Global reach with many regions and AZs
  - Strong security and compliance
  - Large ecosystem of partners and customers

## 0.8 Getting Started with AWS <a id="08-getting-started-with-aws"></a>

- To get started:
  - Create an AWS account
  - Explore the AWS Management Console
  - Use the **AWS Free Tier** to experiment
  - Follow AWS documentation and tutorials

## 0.9 Common AWS Terminology

- **Region:** Geographical area with multiple data centers  
- **Availability Zone (AZ):** Isolated data center within a region  
- **Instance:** Virtual server running on EC2  
- **Bucket:** Storage container in S3  
- **IAM:** Identity and Access Management for permissions  

---

## AWS Account and Infrastructure Overview <a id="aws-account-and-infrastructure-overview"></a>

Learn about the basic building blocks of the AWS ecosystem.

### AWS Account

- Your **AWS Account** is your unique identity in AWS, managing your resources, billing, and permissions.
- Supports multiple users through **IAM**.
- Can be grouped into **Organizations** to manage multiple accounts.

### AWS Regions

- Geographically isolated locations designed for fault tolerance and low latency.
- Examples: `us-east-1` (N. Virginia), `eu-west-1` (Ireland), `ap-south-1` (Mumbai).

### Availability Zones (AZs)

- Physically separate data centers within a region.
- Connected with low-latency links for high availability.
- Distribute resources across AZs to increase fault tolerance.

### Edge Locations

- Part of AWS's Content Delivery Network (CDN).
- Cache and deliver content globally via **Amazon CloudFront**.
- Reduce latency and improve user experience.

### AWS Support Plans

| Plan       | Description                                   |
|------------|-----------------------------------------------|
| Basic      | Free, includes customer service and documentation |
| Developer  | Business hours email support                   |
| Business   | 24/7 phone, chat, and email support            |
| Enterprise | Dedicated Technical Account Manager and Concierge |

---


# Assignments <a id="assignments"></a>
1. [ ] **Create your AWS Account**
2. [ ] **Explore the AWS Management Console**
3. [ ] **Launch and manage EC2 instances:**
    - [ ] Create, start, and stop instances
    - [ ] Connect via SSH using key pairs
    - [ ] Modify or replace SSH keys if needed
    - [ ] Check the ec2 instance terminate protection and stop Protection.
    - [ ] Add a role to instance
    - [ ] Change the Instance Type
    - [ ] Add a new Disk
    - [ ] Create an AMI
4. [ ] **Learn about default users in various AWS AMIs**
5. [ ] **Use AWS CloudShell for command-line access without setup**
6. [ ] **Install AWS CLI and configure credentials:**
    - [ ] Test AWS CLI commands for various services
7. [ ] **Practice configuring Security Groups by opening and blocking ports to control traffic**

---

