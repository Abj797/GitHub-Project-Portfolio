# Project Title

### AWS High Availability PHP Website with Auto Scaling and RDS

# Project Summary
This project showcases the deployment of a high-availability, scalable PHP-based website on Amazon Web Services (AWS), utilizing key AWS services like EC2, RDS, and Auto Scaling. The website is designed to handle dynamic traffic, ensuring optimal performance and uptime. Auto Scaling automatically adjusts the number of EC2 instances based on traffic demand, while Amazon RDS provides a scalable, secure, and fully managed MySQL database solution.



## Features:

#### 1. Auto Scaling:
Automatically scales the EC2 instances based on traffic load to ensure high availability and cost optimization.
Load Balancer: Distributes traffic across EC2 instances for optimal performance.
#### 2. Amazon RDS (MySQL): 
A managed database service that ensures high availability, automated backups, and scalability.
#### 3. VPC & Security Groups: 
Implements private and secure networking configurations to ensure communication between EC2 and RDS instances
## Tech Stack
#### Amazon Web Services (AWS):

      1) EC2 (Elastic Compute Cloud)

      2) RDS (Relational Database Service)

      3) Elastic Load Balancer

      4) Auto Scaling

#### PHP: Backend server technology

#### MySQL: Database engine hosted on Amazon RDS

#### Apache: Web server for hosting the PHP website
## Prerequisites

### Before you begin, make sure you have:

#### 1. AWS Account

#### 2. Key pair for EC2 SSH access

#### 3. MySQL client for database setup
## Setup Instructions

### Step 1: Clone the Repository

a) git clone https://github.com/yourusername/aws-auto-scaling-php-website.git

b) cd aws-auto-scaling-php-website

c) Install Apache Webserver: sudo apt install apache2 -y
 
d) cd var/www/html then delete the index.html file and 
   Copy the  index.php to var/www/html location

### Step 2: Create the Database

a) Launch an EC2 instance where application is being hosted

b) Create RDS instance and select database as Mysql using intel123 as username and set password for higher availability choose minimum 2 subnets and max Availability zones

c) Install mysql client to access database and log in to RDS using command below

sudo mysql -h <RDS Endpoint> - username - password

d) Run the command ‘sudo apt nano’ and enter your database details like your RDS Endpoint, Username, database name and password.
 
### Step 3: Connfigure Auto-Scaling Group and Loadbalancer (Loadbalancer is optional)

a) Create ‘AMI’ for the instance. 

b) Create ‘Launch template’ which is needed for auto scaling group

c) Create Auto-Scaling Group using launch template and set desired capacity and min and max capacity of instances as per requirement

## Screenshots

![AWS Project 1 step 8](https://github.com/user-attachments/assets/220b80de-5229-4f33-a477-e4f744472c2e)

![AWS Project 1 step 10](https://github.com/user-attachments/assets/b439aacd-c485-4f67-9435-a306fbb40790)

![AWS Project 1 step 11](https://github.com/user-attachments/assets/51dabbe1-2f5f-4526-963b-1813c8b4b6a4)
