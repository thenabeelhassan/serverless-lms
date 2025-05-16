# CI/CD Pipeline

This directory contains Jenkins pipeline configurations for automating the build and deployment processes.

## Structure

- `Jenkinsfile.frontend` – CI/CD for the frontend React app
- `Jenkinsfile.backend` – CI/CD for backend services
- `scripts/` – Bash scripts used by Jenkins pipelines

## Jenkins Setup

- Jenkins runs on a dedicated EC2 instance
- Uses credentials for AWS and Docker/ECR
- Pipelines include stages for checkout, build, test, push, and deploy

## Sample Workflow

1. Code push triggers Jenkins job
2. Docker image is built and pushed to ECR
3. Terraform is executed (for infra) or Serverless Framework (for Lambda)