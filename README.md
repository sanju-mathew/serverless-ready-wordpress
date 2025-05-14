# 🚀 Serverless-Ready WordPress on AWS via CloudFormation

This project demonstrates a modern, scalable, and resilient deployment of WordPress on AWS using Infrastructure-as-Code (IaC) with AWS CloudFormation. Transitioning from traditional monolithic setups, this approach leverages AWS services to ensure high availability, scalability, and maintainability.

---

## 🧱 Architecture Overview

The deployment encompasses the following AWS components:

- **Virtual Private Cloud (VPC):** Provides isolated networking.
- **Elastic Compute Cloud (EC2):** Hosts WordPress within an Auto Scaling Group.
- **Application Load Balancer (ALB):** Distributes incoming traffic efficiently.
- **Amazon RDS (MySQL):** Manages the WordPress database.
- **Amazon Elastic File System (EFS):** Offers persistent storage for WordPress files.

*Note: While termed "serverless-ready," this architecture utilizes managed services to minimize server management overhead.*

---

## ⚙️ CloudFormation Template Highlights

The CloudFormation template is written in YAML for clarity and ease of maintenance. Key parameters include:

- **KeyName:** Specifies the SSH key pair for EC2 instance access.
- **DBUsername & DBPassword:** Sets credentials for the RDS instance.
- **InstanceType:** Defines the EC2 instance type (e.g., `t2.micro`).
- **LatestAmiId:** Dynamically fetches the latest Amazon Linux 2 AMI ID using AWS Systems Manager Parameter Store.

---
Read the full guide on my website: [Serverless-Ready WordPress on AWS via CloudFormation](https://homelab.sanjuprojects.uk/serverless%E2%80%91ready-wordpress-on-aws-via-cloudformation/)
---
## 🛠 Deployment Instructions

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/serverless-wordpress-aws.git
   cd serverless-wordpress-aws
