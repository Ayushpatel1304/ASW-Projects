# Day 2 — EC2 Web Server with Auto Scaling

This project demonstrates how to provision, configure, and scale a web server on AWS using Amazon EC2, Auto Scaling Groups (ASG), and an Elastic Load Balancer (ELB). It walks through the full lifecycle of deploying a web application — from a single manually configured server to a resilient, self-healing, and automatically scalable architecture.

Project Overview
The primary objective is to gain hands-on experience with:

* Server provisioning using Amazon EC2.

* Web server configuration (Apache/Nginx) on Amazon Linux 2.

* Creating custom Amazon Machine Images (AMIs) for repeatable deployments.

* Implementing Auto Scaling to dynamically adjust capacity.

* Load balancing incoming traffic across multiple instances.

By the end of this project, the infrastructure will:

* serve a simple sample application (HTML page or basic app).

* Automatically launch new instances when demand increases.

* Distribute traffic evenly across healthy instances using an ELB.

* Replace failed or unhealthy instances without manual intervention.

Implementation Steps
* 1.Launch EC2 Instance
Deployed an Amazon Linux 2 instance and connected via SSH.

* 2.Install Web Server
Installed and configured Apache HTTP Server (or Nginx) to serve a sample app.

* 3.Create Custom AMI
Captured the instance configuration into a reusable AMI for launching identical servers.

* 4.Set Up Auto Scaling Group (ASG)
Configured scaling policies, health checks, and minimum/maximum instance counts.

* 5.Configure Elastic Load Balancer
Integrated an Application Load Balancer to distribute requests across the ASG.

* 6.Load Testing
Used ApacheBench (ab) or Locust to simulate traffic spikes and observe scaling in action.

Learning Outcomes
Understanding EC2 instance lifecycle and AMI creation.

Automating server scaling to match workload demand.

Implementing high availability and fault tolerance using AWS native tools.

Load testing and monitoring scaling behavior.

Architecture
The final architecture consists of:

Elastic Load Balancer (ALB) in front.

Auto Scaling Group spanning multiple Availability Zones.

Instances launched from the custom AMI running the pre-configured web server.

This setup ensures scalability, resilience, and reduced operational overhead, forming a solid foundation for more complex cloud-native deployments.
