# Automated CI/CD Pipeline with Jenkins on AWS

## 📖 Description
This project implements a complete CI/CD (Continuous Integration/Continuous Deployment) pipeline using Jenkins on AWS. The pipeline is automatically triggered by a Git push, building a Docker application, and pushing the image to Docker Hub. Infrastructure is managed as code using Terraform.

## 📋 Prerequisites
Before you begin, ensure you have the following:
- An [AWS account](https://aws.amazon.com/) with appropriate permissions.
- A [Docker Hub](https://hub.docker.com/) account.
- The following tools installed on your local machine:
  - [Terraform](https://www.terraform.io/downloads.html) (`v1.5.0+`)
  - [AWS CLI](https://aws.amazon.com/cli/) (configured with your credentials)
  - Git

## 🏗️ Architecture
![CI/CD Architecture Diagram](images/architecture-diagram.png) <!-- You can create a simple diagram and add it to an 'images' folder -->

The workflow is as follows:
1. A developer pushes code to the main GitHub branch.
2. GitHub sends a webhook notification to the Jenkins server.
3. Jenkins pulls the latest code, including the `Jenkinsfile`.
4. Jenkins executes the pipeline stages defined in the `Jenkinsfile`.
5. The pipeline builds a new Docker image and pushes it to Docker Hub.

## ⚙️ Setup & Installation

### 1. Terraform Infrastructure Provisioning
This repository uses Terraform to provision the Jenkins server on AWS.

**Initialize Terraform:**
```bash
terraform init
