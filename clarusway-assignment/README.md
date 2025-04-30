# Week 9 Assignment – Clarusway Infrastructure Bootcamp

## Overview
This project demonstrates how to deploy a highly available web application using:
- **Amazon S3** for static assets
- **Auto Scaling Group (ASG)** with EC2 instances running **NGINX**
- **Application Load Balancer (ALB)** for traffic distribution

## Deployed By:  
**Amjad Albeladi**

---

## Part 1: S3 Static Website

- Bucket Name: `amjad-clarusway-assets`
- Region: `eu-north-1`
- Static Website URL:  
  http://amjad-clarusway-assets.s3-website.eu-north-1.amazonaws.com/

### Screenshots:
- `s3-website.png`
- `s3-curl-test.png`

---

## Part 2: Auto Scaling Group (ASG)

- Launch Template with User Data to install NGINX and fetch index.html from S3
- IAM Role: `EC2S3AccessRole` (S3 read permissions)
- ASG configuration:
  - Min: 1
  - Desired: 2
  - Max: 3

### Screenshots:
- `ec2-running-instances.png`
- `asg-configuration.png`

---

## Part 3: Application Load Balancer (ALB)

- Internet-facing ALB
- Port 80 listener
- Health check on `/`

### ALB DNS Name:
http://clarusway-alb-1910199538.eu-north-1.elb.amazonaws.com/

### Screenshots:
- `alb-browser.png`
- `alb-curl-test.png`

---

## Cleanup
All AWS resources (S3, EC2, ASG, ALB) have been deleted.

