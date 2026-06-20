Architecture Diagram
![image alt](https://github.com/teajo99/finance-web-app-aws/blob/a89e59182b4c1852bfe42e8008463783868adac4/Finance%20web%20app/Architecture%20diagram.png)

AWS-based finance web application architecture designed for scalability and high availability. User traffic is distributed through an Application Load Balancer to an Auto Scaling Group of EC2 instances deployed across multiple Availability Zones within a VPC. The EC2 instances host a simple finance web application initialized using a user data script. CloudWatch monitors CPU utilization and triggers scaling policies to automatically adjust capacity between one and three instances based on demand, demonstrating elastic infrastructure and fault-tolerant design principles.

# Finance Web App Simulation on AWS

## Overview
This project simulates the deployment of a **finance web application** on AWS, focusing on scalability, high availability, and infrastructure automation. The environment is designed to replicate a trading platform that can handle fluctuations in user traffic, highlighting expertise in AWS core services including **VPC, EC2, and Auto Scaling**.

---

## Architecture
- **Virtual Private Cloud (VPC)** with 2 public subnets across 2 Availability Zones  
  - Ensures network isolation and redundancy.  
- **EC2 Instances** running a minimal web application  
  - Configured via a **User Data script** to serve a simple page: "Finance Web App is Up and Running!"  
- **Auto Scaling Group (ASG)**  
  - Configured to maintain **1–3 instances** based on **CPU utilization (target: 50%)**  
  - Simulates automatic response to traffic spikes to ensure continuous availability  

---

## Features
- **High Availability:** Distribution across multiple AZs to maintain uptime.  
- **Scalability:** Auto Scaling demonstrates automatic adjustment of compute resources under simulated load.  
- **Infrastructure Automation:** EC2 instances configured automatically using a bash User Data script.  
- **Traffic Simulation:** Apache Benchmark (`ab`) used to generate load and verify scaling behavior.  

---

## Repository Contents
- `user-data.sh` → EC2 instance initialization script  
- `load-test.sh` → Bash script to simulate traffic for ASG validation  
- `screenshots/` → Visual documentation of instance status, ASG configuration, and simulated traffic results  
- `diagrams/` →  Network diagrams illustrating VPC and subnet layout  

---

## Skills and Knowledge Demonstrated
- Designing **VPC architecture with multiple subnets and AZs** for redundancy  
- Configuring **EC2 instances** with automated initialization scripts  
- Implementing **Auto Scaling Groups** and CPU-based scaling policies  
- Simulating traffic to validate **scalability and performance**  
- Understanding AWS concepts of **high availability, fault tolerance, and resource optimization**  

---

## How to Explore
1. Review `user-data.sh` to see automated EC2 setup.  
2. Examine Auto Scaling configuration in screenshots to understand instance scaling logic.  
3. Observe load test results in `screenshots/` to see how scaling responds under simulated traffic.  

---

This simulation provides a clear example of **designing and configuring scalable cloud infrastructure** using AWS, demonstrating knowledge applicable to real-world finance applications.
