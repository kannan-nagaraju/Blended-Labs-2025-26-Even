# Lab 6 – Scale and Load Balance Your Architecture
```
Author :KANNAN N
Reg no : 212223230097
Date : 18-05-2026
```
## Title

Scale and Load Balance Your Architecture
---


---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)


1.Launched a new EC2 instance named Web Server in the N. Virginia region using Amazon Linux 2023 AMI and t2.micro instance type.

2.Enabled termination protection and stop protection, configured a security group, and added a user data script to install and start an Apache web server.

3.Monitored the instance using status checks, CloudWatch metrics, and system logs to ensure it was running properly.

4.Modified the security group to allow HTTP (port 80) traffic and accessed the web server using the public IP address.

5.Resized the instance to t2.small, increased the EBS volume size, explored EC2 service quotas, tested stop protection, and finally stopped the instance.


## Output Screenshots 
<img width="1920" height="1022" alt="1" src="https://github.com/user-attachments/assets/a2948c68-c5ff-45ca-8635-17855910f160" />
<img width="1920" height="1024" alt="2" src="https://github.com/user-attachments/assets/b80c1f50-da59-43eb-9b1d-4b0557acca39" />
<img width="1920" height="1024" alt="3" src="https://github.com/user-attachments/assets/0ebd9fe5-a020-4b8a-82bd-149ef4cbfc80" />
<img width="1920" height="1024" alt="4" src="https://github.com/user-attachments/assets/3304498d-f211-4123-9f2c-ec5f11661dac" />


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
