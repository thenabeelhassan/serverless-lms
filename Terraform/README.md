# Terraform

This directory contains Terraform code to provision the entire LMS infrastructure in AWS.

## Key Resources

- ECS Cluster, ALB, Task Definitions
- Lambda Functions and API Gateway
- DocumentDB for MongoDB-compatible storage
- VPC, Subnets, Routing, IAM Roles

## Structure

- `main.tf` – Root module
- `modules/` – Custom reusable modules (e.g., ECS, Lambda)
- `environments/` – Dev/stage/prod specific configs
- `variables.tf`, `outputs.tf`, `backend.tf` – Supporting files

## Commands

```bash
terraform init
terraform plan
terraform apply
```