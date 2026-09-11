# HelpDesk-AWS

## AWS Cloud-Based Help Desk Application

HelpDesk-AWS is a cloud-based Help Desk application built with **Python Flask** and deployed on **Amazon Web Services (AWS)**.

The project demonstrates practical cloud engineering concepts including EC2 deployment, Amazon RDS MySQL, Application Load Balancing, Auto Scaling, VPC networking, Linux administration, and Git/GitHub.

## Architecture

```text
                    Internet
                       |
                       v
              Application Load
                 Balancer
                       |
              +--------+--------+
              |                 |
              v                 v
           EC2 #1            EC2 #2
         Flask :5000        Flask :5000
              |                 |
              +--------+--------+
                       |
                       v
                  Amazon RDS
                   MySQL DB
```

## Technologies

**Technologies:**
AWS • Linux • Python • Flask • MySQL • Amazon RDS • Amazon EC2 • Application Load Balancer • Auto Scaling • VPC • Git • GitHub

## AWS Services

* **Amazon EC2** – Hosts the Flask application.
* **Amazon RDS MySQL** – Stores help desk tickets.
* **Application Load Balancer** – Distributes traffic between EC2 instances.
* **Auto Scaling Group** – Manages multiple application instances.
* **Amazon VPC** – Provides the cloud networking environment.
* **Security Groups** – Controls inbound and outbound traffic.

## Application Features

* Create help desk tickets
* Store tickets in MySQL
* View submitted tickets
* Ticket status tracking
* Application health endpoint
* Load-balanced application access

## Database

The application uses an Amazon RDS MySQL database with a `tickets` table containing:

```text
id
name
email
subject
description
status
created_at
```

## Deployment

The application was deployed to Amazon EC2 using Amazon Linux and Python Flask.

The Application Load Balancer forwards traffic to EC2 instances running the application on:

```text
HTTP : 5000
```

Health checks use:

```text
/health
```

The Auto Scaling Group maintains two application instances across:

```text
ap-south-1a
ap-south-1b
```

## Key Learning Outcomes

This project provided hands-on experience with:

* AWS EC2 deployment
* Amazon RDS and MySQL
* VPC and subnet configuration
* Security Groups
* Application Load Balancer
* Target Groups and health checks
* Auto Scaling Groups
* Linux server administration
* Python Flask deployment
* Git and GitHub

## AWS Region

```text
ap-south-1 (Mumbai)
```

## Project Type

**Cloud Engineer / AWS Portfolio Project**
