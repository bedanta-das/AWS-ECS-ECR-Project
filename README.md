# 🚀 AWS ECS + ECR Project (Node.js Application Deployment)

📌 Project Overview
This project demonstrates end-to-end deployment of a Node.js application using AWS container services with a project-based DevOps approach.
* You will learn how to:
* Build a Docker image from a Node.js app
* Push the Docker image to Amazon ECR (Elastic Container Registry)
* Deploy and run the container on Amazon ECS using AWS Fargate (Serverless)
* View application logs in Amazon CloudWatch
* Secure access using IAM roles and policies
This project is designed for Cloud Engineers, DevOps Engineers, and AWS beginners who want real-world hands-on experience.

## 🏗️ Architecture Diagram (Conceptual)

            GitHub 
               |
               |
               V
         EC2 (Docker Build)
                |
                |
                V
         ECR (Docker Image Registry)
               |
               |
               V
      ECS (Fargate - Serverless Containers)
               |
               |
               V
      CloudWatch (Logs & Monitoring)

## 🧩 AWS Services Used
      Services	                                 Purpose
      GitHub	                                   Source code repository
      EC2	                                        Build Docker image & push to ECR
      Docker	                                  Containerize Node.js application
      ECR	                                        Store Docker images
      ECS (Fargate)	                               Run containers without managing servers
      IAM	                                        Secure access & permissions
      CloudWatch	                               Logs & monitoring

## 📂 Application Details

* Application Type: Node.js (Todo App)
* Port: 3000
* Container Runtime: Docker
* Deployment Type: Serverless (AWS Fargate)

## ⚙️ Prerequisites

* AWS Account
* Basic understanding of:
  * Linux
  * Docker
  * AWS IAM
* AWS CLI installed
* Docker installed
* Git installed

🛠️ Step-by-Step Implementation
1️⃣ Clone the GitHub Repository

            git clone https://github.com/bedanta-das/AWS-ECS-ECR-Project.git
            
2️⃣ Launch EC2 Instance (Build Server)
* AMI: Ubuntu
* Instance Type: t2.micro (Free Tier)
* Purpose: Build Docker image and push to ECR

Install required tools:
  
            sudo apt update
            sudo apt install docker.io unzip -y

Add user to Docker group:

            sudo usermod -aG docker $USER
            reboot

3️⃣ Install AWS CLI

            curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
            sudo apt install unzip
            unzip awscliv2.zip
            sudo ./aws/install
            aws --version

Configure AWS credentials:

aws configure
