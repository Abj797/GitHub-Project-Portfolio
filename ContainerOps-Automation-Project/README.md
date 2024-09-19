# ContainerOps-Automation-Project

## Project Overview
Implemented a streamlined DevOps lifecycle, automating deployment, scaling, and operations of containerized applications. Utilized Git workflow for version control, triggered CodeBuild for continuous integration, and
deployed Dockerized code to Kubernetes cluster in production. Automated infrastructure setup using Terraform and configuration management tools.

## Key Features
Automated Deployment: Continuous deployment of Dockerized applications to a Kubernetes cluster.
Scalable Infrastructure: Kubernetes is used to handle horizontal scaling, ensuring high availability and efficient resource usage.
Infrastructure as Code (IaC): Automated setup of infrastructure using Terraform.
Configuration Management: Ansible automates the configuration of EC2 instances.
CI/CD Pipeline: GitHub integration triggers CodeBuild for continuous integration, followed by deployment using Jenkins pipelines.

## Tools & Technologies
Amazon EC2: Cloud infrastructure to host application components.

Git & GitHub: Version control and code repository.

Docker: Containerization for applications.

Terraform: Infrastructure as code for automated provisioning.

Jenkins: Automation server for managing CI/CD pipelines.

Kubernetes: Orchestrates containerized applications and ensures scalability.

Ansible: Configuration management for provisioning and software installation.

## Architecture Diagram

![Capstone Project-2](https://github.com/user-attachments/assets/d7914a89-79f2-493e-9a85-3fdb8bd38da3)

![Capstone Project-2 new](https://github.com/user-attachments/assets/64157eec-0a44-4448-9c6c-d1ed1b9f0fbd)

![image](https://github.com/user-attachments/assets/99d207e9-2bb9-4fe0-a1f1-a76381e36b04)

![image](https://github.com/user-attachments/assets/a1462025-4bcf-4edf-a99b-28d2114bbdb9)

![image](https://github.com/user-attachments/assets/aeecf8f9-2c51-404f-b361-39cf4678ea5f)

![image](https://github.com/user-attachments/assets/d624676a-0d54-4aec-ab9b-e3d1cc6eee2d)

![image](https://github.com/user-attachments/assets/695928c6-9ea5-4660-91c2-bb813be99352)

![image](https://github.com/user-attachments/assets/6d9e9da9-cea2-4517-bf9c-03871278639d)

## Workflow
Version Control: Code is managed in a GitHub repository.

Continuous Integration (CI): When a new commit is pushed to the main branch, it triggers a build in AWS CodeBuild.

Infrastructure Automation: Terraform automates the creation of EC2 instances and other infrastructure components.

Configuration Management: Ansible configures the instances, installing necessary software and setting up the environment.

Containerization: The application is Dockerized, and the Docker images are pushed to a container registry.

Continuous Deployment (CD): Jenkins orchestrates the deployment process, using Kubernetes to manage containerized application deployments.

Production Environment: The Dockerized app is deployed in a Kubernetes cluster, ensuring scalability and fault tolerance.

## Installation
AWS Console: Sign up AWS Console with the necessary credentials.

Terraform: Install Terraform.

Docker: Install Docker.

Kubernetes: Ensure you have a running Kubernetes cluster.

Jenkins: Set up Jenkins with Docker and Kubernetes plugins installed.

## Steps
#### 1) Clone the repository:
git clone https://github.com/your-username/ContainerOps-Automation.git
cd ContainerOps-Automation

#### 2) Provision Infrastructure with Terraform:
terraform init
terraform apply

#### 3) Set Up Configuration with Ansible:
ansible-playbook -i inventory setup.yml

#### 4) Build and Push Docker Image:
docker build -t your-dockerhub-username/app:latest .
docker push your-dockerhub-username/app:latest

#### 5) Deploy Application on Kubernetes:
kubectl apply -f k8s/deployment.yml
kubectl apply -f k8s/service.yml

#### 6) Monitor Jenkins Pipeline:
The Jenkins pipeline is triggered by new commits to the GitHub repo, ensuring automated deployment.
