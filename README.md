# Terraform Docker Infrastructure

A simple Infrastructure as Code (IaC) project that uses Terraform to provision and manage a Docker container running Nginx.

## Project Overview

This project demonstrates how Terraform can be used to automate Docker infrastructure instead of creating containers manually with Docker commands.

Terraform provisions:

- Nginx Docker image
- Nginx Docker container
- Port mapping from host `8080` to container `80`

## Architecture

```text
Terraform
    |
    v
Docker Provider
    |
    +------> Nginx Docker Image
    |
    v
Nginx Container
    |
    v
localhost:8080
```

## Technologies Used

- Terraform
- Docker
- Nginx
- Git
- GitHub
- Infrastructure as Code (IaC)

## Project Structure

```text
terraform-docker-infrastructure/
│
├── main.tf
├── .gitignore
├── .terraform.lock.hcl
└── README.md
```

## Terraform Configuration

The `main.tf` file defines the Docker provider, Nginx image, and Docker container.

The container exposes:

```text
localhost:8080 → container:80
```

## Prerequisites

Make sure the following are installed:

- Docker Desktop
- Terraform
- Git

Verify Terraform:

```bash
terraform version
```

Verify Docker:

```bash
docker --version
```

## How to Deploy

### 1. Initialize Terraform

```bash
terraform init
```

### 2. Review the Infrastructure Plan

```bash
terraform plan
```

### 3. Create the Docker Infrastructure

```bash
terraform apply
```

Type:

```text
yes
```

when prompted.

### 4. Verify the Container

```bash
docker ps
```

The container should appear as:

```text
terraform-nginx
```

### 5. Access the Application

Open the following URL in a browser:

```text
http://localhost:8080
```

The Nginx welcome page should be displayed.

## Useful Terraform Commands

```bash
terraform init
terraform plan
terraform apply
terraform show
terraform destroy
```

To remove the infrastructure:

```bash
terraform destroy
```

Type `yes` when prompted.

## What I Learned

Through this project, I practiced:

- Infrastructure as Code using Terraform
- Terraform provider configuration
- Docker resource provisioning
- Declarative infrastructure management
- Terraform plan and apply workflow
- Managing infrastructure through Git and GitHub
- Basic DevOps automation practices

## Resume Project Description

**Terraform Docker Infrastructure Automation**

- Provisioned and managed Docker infrastructure using Terraform and Infrastructure as Code (IaC).
- Automated Nginx container deployment with Terraform Docker provider and configured port mapping.
- Used Git and GitHub for version control and documented infrastructure deployment and management workflows.