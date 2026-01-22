# Portfolio Website Hosted on AWS EC2 with ALB and Auto Scaling

## Description
This project demonstrates deploying a personal portfolio website on AWS using EC2 instances along with an Application Load Balancer and Auto Scaling Group to achieve high availability, scalability, and fault tolerance.

---

## Technologies Used
- HTML, CSS, JavaScript
- AWS EC2
- Application Load Balancer (ALB)
- EC2 Auto Scaling
- Amazon Linux
- Apache Web Server
- SSH
- VPC and Security Groups

---

## Architecture Overview
- Multiple EC2 instances host the same portfolio application
- Application Load Balancer distributes incoming HTTP traffic
- Auto Scaling Group automatically scales EC2 instances based on CPU utilization
- High availability achieved using multiple Availability Zones

---

## EC2 Configuration Steps
1. Created an EC2 Launch Template using Amazon Linux and t2.micro instance type
2. Configured Security Groups to allow SSH (22) and HTTP (80)
3. Installed Apache web server on EC2 instances
4. Deployed portfolio files to `/var/www/html`
5. Verified application access using instance public IP

---

## Application Load Balancer Setup
1. Created an internet-facing Application Load Balancer
2. Configured HTTP listener on port 80
3. Created a target group
4. Registered EC2 instances with the target group
5. Verified traffic routing using the ALB DNS name

---

## Auto Scaling Configuration
1. Created an Auto Scaling Group using the launch template
2. Attached the Auto Scaling Group to the Application Load Balancer
3. Set minimum, desired, and maximum instance capacity
4. Configured scaling policy based on CPU utilization
5. Verified automatic scale-out and scale-in behavior

---

## Outcome
- Portfolio website is highly available and fault tolerant
- Traffic is evenly distributed across EC2 instances
- Instances automatically scale based on traffic load
- Application is accessible via the Application Load Balancer DNS URL

---

## Key Learnings
- Launching and configuring EC2 instances
- Implementing load balancing using ALB
- Automatic scaling with Auto Scaling Groups
- Designing scalable and highly available AWS architectures

---

## Access
The application is accessible using the Application Load Balancer DNS endpoint.

