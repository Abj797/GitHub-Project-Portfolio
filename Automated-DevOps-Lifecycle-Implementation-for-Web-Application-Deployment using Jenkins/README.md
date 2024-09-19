# Project Title

Automated-DevOps-Lifecycle-Implementation-for-Web-Application-Deployment using jenkins
  
## Project Overview

This project demonstrates the full implementation of the DevOps Lifecycle for Abode Software, a product-based company. The company’s web application, available on GitHub, is containerized, tested, and deployed using a continuous integration/continuous delivery (CI/CD) pipeline. The project leverages Jenkins, AWS CodeBuild, Docker, and Ansible to achieve fast and efficient deployment while ensuring code quality.

## Key Features

#### 1) Configuration Management:

Using Ansible, software such as Docker, Git, and Jenkins are installed and configured on servers automatically, ensuring a consistent environment setup across machines.

#### 2) Git Workflow:

A branch-based development workflow is implemented. Changes to the develop branch trigger tests, while commits to the master branch trigger both tests and deployment to production.
CI/CD Pipeline:

#### 3) AWS CodeBuild automatically triggers builds based on branch commits:
Develop branch: Tests are run, but no deployment.
Master branch: Tests are run, and on success, the code is automatically pushed to production.
Containerization:

#### 4) The application is packaged as a Docker container using a pre-built image: hshar/webapp.
The code resides in /var/www/html, and the Dockerfile ensures that the application is ready to be deployed in a portable and scalable containerized environment.
Jenkins Jobs:

#### 5) A Jenkins Freestyle Project is created to handle the build, test, and production deployment steps.
Job 1: Build: Builds the Docker image.
Job 2: Test: Runs tests inside the Docker container.
Job 3: Prod: Deploys the built Docker image to production when a commit is made to the master branch.

## Architectural Overview

#### The architecture for this DevOps lifecycle is as follows:

##### 1) Configuration Management: Ansible playbooks configure software dependencies across the infrastructure.
##### 2) GitHub Integration: Commits to the GitHub repository trigger the CI/CD pipeline.
##### 3) Docker: The code is containerized, allowing for easy portability and scalability.
##### 4) Jenkins: Manages the build, test, and deployment jobs, ensuring the automation of the DevOps pipeline.
##### 5) AWS CodeBuild: Automates the build and test phases, ensuring continuous integration across environments.

## Technologies Used

#### 1) Jenkins: For orchestrating the CI/CD pipeline.

#### 2) Ansible: For configuration management.

#### 3) Docker: For containerizing the application.

#### 4) AWS CodeBuild: To automate builds and tests.

#### 5) Git: For version control and branching strategy.

## Installation and Usage

#### 1) Clone the repository:

git clone https://github.com/hshar/website.git
cd website

#### 2) Build the Docker container:

docker build -t hshar/webapp .

#### 3) Run the application inside a Docker container:

docker run -p 8080:80 hshar/webapp

#### 4) To set up Jenkins Jobs:

Create three jobs in Jenkins (Build, Test, and Prod) as described in the project details.

## Screenshots 

![image](https://github.com/user-attachments/assets/363cca13-6c76-4d6f-b789-9f744b0d8bbf)

![image](https://github.com/user-attachments/assets/8248103f-c334-40e5-8436-13b3757242f2)

![image](https://github.com/user-attachments/assets/9d98800a-c567-4eac-b5b4-aed345634da1)

![image](https://github.com/user-attachments/assets/b669ce55-3a0e-4c4c-bb69-a78ebd58dfae)

![image](https://github.com/user-attachments/assets/1c67c833-8cbf-467c-a746-ee171211b888)

## Conclusion 
This project provides a complete DevOps lifecycle for a web application, from configuration management to continuous integration and delivery. The use of automated freestyle jobs ensures efficient code testing, containerization, and deployment, making this setup scalable and reliable for a production environment.
