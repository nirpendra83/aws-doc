+++
title = "AWS EC2 (Elastic Compute Cloud)"
weight = 3
+++



## Objective
- **Understand the purpose and features of AWS EC2.**
- Learn how to launch, configure, and manage EC2 instances.
- Explore different EC2 instance types and their use cases.
- Understand Elastic IPs and Security Groups for networking and security.
- Learn how to implement Auto Scaling to manage instance availability and cost.
- Discover other important EC2 features like EBS, Placement Groups, Spot Instances, and more.

---

## 2.1 Introduction to EC2

Amazon Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers by allowing you to launch and manage virtual servers called instances. EC2 provides secure, scalable computing capacity and supports various operating systems.

**Key Features:**
- Scalable compute capacity
- Multiple instance types optimized for different workloads
- Flexible cloud hosting services
- Pay-as-you-go pricing model
- Integration with other AWS services

---

## 2.2 Launching EC2 Instances

Launching an EC2 instance involves the following steps:

1. **Sign in to the AWS Management Console**  
2. Navigate to the EC2 Dashboard  
3. Click **Launch Instance**

### AMI (Amazon Machine Image)
- A preconfigured template that contains the operating system, application server, and applications.
- Provides the information required to launch an instance.
- You can choose from public AMIs, AWS Marketplace AMIs, or create your own custom AMIs.

### Instance Type
- Defines the hardware configuration of the instance (CPU, memory, storage, networking).
- Choose based on your workload requirements.

### Placement
- Select the **Availability Zone** to specify where your instance will physically run within a region.
- You can also choose **Placement Groups** for optimized network performance or to meet regulatory requirements.

### SSH Key Pair
- Key pairs are used for secure login to your instances.
- When launching an instance, you specify an SSH key pair; the private key is used to securely connect to the instance.
- AWS does not store your private key — you must keep it safe.

### Proximity (Placement Groups)
- Placement Groups control how instances are placed on underlying hardware.
- Types of placement groups:
  - **Cluster:** Packs instances close together for low-latency network performance.
  - **Spread:** Distributes instances across distinct hardware to reduce correlated failures.
  - **Partition:** Divides instances into logical partitions to isolate failure domains.

### Debugging Options
- Enable **detailed monitoring** for performance metrics.
- Use **System Logs** and **Instance Console Output** for troubleshooting boot or OS issues.
- Use **CloudWatch Logs** and **CloudTrail** to track and audit instance activity.
- Configure **IAM Roles** to securely access AWS services from the instance.

### Additional Steps:
4. Configure Instance Details — network settings, IAM role, shutdown behavior  
5. Add Storage — attach EBS volumes  
6. Add Tags — optional metadata for organizing resources  
7. Configure Security Group — firewall settings controlling inbound/outbound traffic  
8. Review and Launch — confirm settings and launch instance  
9. Connect to your instance using SSH (Linux) or RDP (Windows)  

---

## 2.3 EC2 Instance Types

EC2 provides a variety of instance types tailored to different use cases. Instances are grouped into families based on their capabilities:

- **General Purpose:** Balanced CPU, memory, and networking (e.g., t3, m5)  
- **Compute Optimized:** High CPU for compute-intensive applications (e.g., c5, c6g)  
- **Memory Optimized:** High memory for in-memory databases (e.g., r5, x1)  
- **Storage Optimized:** High disk throughput and IOPS (e.g., i3, d2)  
- **GPU Instances:** For machine learning and graphics applications (e.g., p3, g4)  

Choosing the right instance depends on your workload requirements and budget.

---

## 2.4 Elastic IP and Security Groups

### Elastic IP

An Elastic IP address is a static, public IPv4 address designed for dynamic cloud computing. It allows you to mask instance failures by quickly remapping the address to another instance.

- It is associated with your AWS account, not a specific instance.  
- Useful for applications requiring a fixed IP address.  
- You can associate or disassociate Elastic IPs as needed.  

### Security Groups

Security Groups act as virtual firewalls that control inbound and outbound traffic for your instances.

- You define rules to allow specific IP addresses or ranges on certain ports.  
- By default, inbound traffic is blocked and outbound traffic is allowed.  
- Security groups are stateful — if inbound traffic is allowed, the response outbound traffic is automatically allowed.  
- You can assign multiple security groups to an instance.  

---

## 2.5 EC2 Auto Scaling

EC2 Auto Scaling helps maintain application availability by automatically adjusting the number of instances.

- **Auto Scaling Groups:** Define a collection of EC2 instances treated as a logical group for scaling and management.  
- **Scaling Policies:** Automatically increase or decrease instance count based on metrics like CPU utilization.  
- Ensures that you have the right number of instances to handle load.  
- Helps reduce costs by scaling down when demand is low.  
- Supports health checks to replace unhealthy instances automatically.  

---

## Other Important AWS EC2 Features

- **Elastic Block Store (EBS)**  
  Persistent block storage volumes that you can attach to your EC2 instances for data storage. Supports snapshots and resizing.

- **Elastic Load Balancing (ELB)**  
  Automatically distributes incoming traffic across multiple EC2 instances to improve fault tolerance and scalability.

- **Instance Store (Ephemeral Storage)**  
  Temporary block-level storage physically attached to the host computer, ideal for temporary data.

- **Instance Metadata and User Data**  
  Provides instance-specific information and allows bootstrapping via user data scripts (cloud-init).

- **Elastic IP Addresses**  
  Static public IPs that you can associate with your instances to maintain fixed IP addresses.

- **Security Groups**  
  Virtual firewalls controlling inbound and outbound traffic at the instance level.

- **Network Interfaces (ENIs)**  
  Attach multiple network interfaces to your instance for advanced networking configurations.

- **Placement Groups**  
  Placement strategies to optimize latency, throughput, or fault tolerance (cluster, spread, partition).

- **Auto Scaling**  
  Automatically adjust the number of instances based on demand.

- **Dedicated Hosts and Instances**  
  Physical servers dedicated to your use for compliance and licensing purposes.

- **Spot Instances**  
  Use spare AWS compute capacity at discounted prices, ideal for fault-tolerant and flexible applications.

- **Hibernation**  
  Pause and resume instances with their RAM contents saved, enabling faster start times.

- **Instance Types and Families**  
  Variety of instance types optimized for compute, memory, storage, or GPU workloads.

- **Amazon Machine Images (AMIs)**  
  Custom or pre-built OS and software configurations used to launch instances quickly.

- **Enhanced Networking**  
  Higher bandwidth, lower latency, and lower jitter network interfaces for EC2 instances.

- **Tagging**  
  Organize and manage instances and related resources using metadata tags.

# Assignments <a id="assignments"></a>
- [ ] Create an AWS account and access the EC2 dashboard.
- [ ] Launch a Linux EC2 instance using the free-tier eligible AMI.
- [ ] Launch a Windows EC2 instance.
- [ ] Generate and download an SSH key pair.
- [ ] Connect to a Linux instance using SSH.
- [ ] Connect to a Windows instance using RDP.
- [ ] Stop and start an EC2 instance.
- [ ] Reboot an EC2 instance.
- [ ] Terminate an EC2 instance.
- [ ] Create a custom AMI from an existing instance.
- [ ] Launch an EC2 instance using a custom AMI.
- [ ] Attach an Elastic IP to an EC2 instance.
- [ ] Detach an Elastic IP and associate it with another instance.
- [ ] Create and attach an EBS volume to an EC2 instance.
- [ ] Detach and delete an EBS volume.
- [ ] Resize an EBS volume attached to an instance.
- [ ] Take a snapshot of an EBS volume.
- [ ] Restore an EBS volume from a snapshot.
- [ ] Create and manage Security Groups.
- [ ] Add inbound rules to Security Groups to allow SSH, HTTP, and HTTPS.
- [ ] Remove rules from Security Groups.
- [ ] Assign multiple Security Groups to an EC2 instance.
- [ ] Use EC2 user data to automate instance setup with shell scripts.
- [ ] Enable detailed monitoring on an EC2 instance.
- [ ] View CloudWatch metrics for CPU utilization and network traffic.
- [ ] Set up CloudWatch alarms for high CPU usage.
- [ ] Create an IAM role and attach it to an EC2 instance.
- [ ] Use IAM roles to grant EC2 instances permissions to access S3 buckets.
- [ ] Enable and view instance console output and logs.
- [ ] Use EC2 instance metadata to query instance-specific information.
- [ ] Use AWS Systems Manager Session Manager to connect to an EC2 instance without SSH.
- [ ] Create a placement group and launch instances inside it.
- [ ] Launch instances in different Availability Zones for high availability.
- [ ] Set up an Auto Scaling Group with EC2 instances.
- [ ] Create scaling policies for Auto Scaling Groups based on CPU load.
- [ ] Create a launch template for EC2 instances.
- [ ] Update and version a launch template.
- [ ] Use EC2 Spot Instances to reduce costs.
- [ ] Create an Elastic Load Balancer and register EC2 instances.
- [ ] Enable termination protection for an EC2 instance.
- [ ] Modify instance types by stopping and changing instance size.
- [ ] Enable EBS encryption for an existing volume.
- [ ] Use tags to organize EC2 instances.
- [ ] Implement security best practices for EC2 (restrict SSH access, use key pairs).
- [ ] Enable EC2 instance hibernation and test it.
- [ ] Use Amazon EC2 Auto Recovery to automatically recover instances.
- [ ] Enable Enhanced Networking for high-performance network.
- [ ] Create a launch configuration and use it with Auto Scaling.
- [ ] Monitor EC2 instance billing and optimize costs.
- [ ] Backup EC2 instances and data regularly.
