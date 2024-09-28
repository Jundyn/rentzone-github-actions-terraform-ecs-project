# Deploying Dynamic Web Apps on AWS using CI/CD Pipelins - GitHub Actions

## Project Overview

This project outlines the deployment of a dynamic web application on AWS using CI/CD pipelines and GitHub Actions. It leverages various AWS services and tools to create a scalable, efficient infrastructure that supports automated deployment and continuous integration.

## Technologies and Tools Used

To set up and test the project, the following tools and services are essential:

- **Docker**: For building the container image.
- **Git**: To track changes in the source code and files.
- **GitHub**: For managing the Dockerfile and application code in repositories.
- **GitHub Actions**: For continuous integration and deployment.
- **AWS CLI**: To interact with AWS services from the command line.
- **Flyway**: For migrating SQL data into the RDS database.
- **VS Code**: As the code editor for writing and editing scripts.
- **Amazon ECR**: To store the Docker image.
- **Amazon ECS**: For containerizing the web application in the AWS cloud.
- **3-Tier VPC**: With public and private subnets across two availability zones.
- **Internet Gateway**: To enable communication between VPC resources and the internet.
- **NAT Gateways**: To allow resources in private subnets to access the internet.
- **Amazon MySQL RDS**: For the relational database.
- **ECS Fargate**: To run the containerized application.
- **Application Load Balancer**: For distributing web traffic to ECS Fargate tasks.
- **Auto Scaling Group**: To dynamically create new ECS tasks based on demand.
- **Route 53**: For domain name registration and DNS management.
- **AWS S3**: To store files containing environment variables for the container.
- **IAM Roles**: To grant permissions for ECS task execution.
- **Bastion Host**: For setting up an SSH tunnel to access private resources.
- **Security Groups**: To control inbound and outbound traffic to resources.
- **AWS Certificate Manager**: For encrypting data in transit.

## Project Structure

The repository contains the following key components:

- **Reference Diagram**: Visual representation of the architecture and resource setup.
- **Scripts**: Terraform scripts for provisioning AWS resources.
- **Dockerfile**: Instructions for building the Docker image of the web application.
- **GitHub Actions Workflows**: CI/CD configurations for automated deployments.

## Getting Started

### Prerequisites

Make sure to have the following tools installed on your local machine:

1. **Docker**
2. **Git**
3. **AWS CLI**
4. **Flyway**
5. **VS Code**

### Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
   ```

2. **Build the Docker Image**:
   ```bash
   docker build -t your-image-name .
   ```

3. **Push the Image to Amazon ECR**:
   Log in to your Amazon ECR repository and push the Docker image.

4. **Deploy with Terraform**:
   Initialize Terraform and apply the configuration:
   ```bash
   terraform init
   terraform apply
   ```

5. **Migrate Database with Flyway**:
   Use Flyway to execute the SQL migrations to the Amazon RDS database.

6. **Set Up CI/CD with GitHub Actions**:
   Ensure your GitHub Actions workflows are correctly configured to trigger on commits.

## Accessing the Application

After deployment, access your web application via the domain set up in Route 53. Make sure DNS settings are correctly configured.

![Rentzone web page](https://github.com/user-attachments/assets/dce9c212-8b95-4f11-9f71-54cac08c852d)


## Acknowledgments

Thanks to the AWS documentation and community resources for their invaluable support throughout the project.

---

Feel free to customize any section as needed!
