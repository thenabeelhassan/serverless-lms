# Serverless LMS – Architecture Documentation

This document outlines the architecture and deployment strategy for the Serverless LMS built on AWS.

---

## 🧭 High-Level Overview

The system is broken down into three core layers:

1. **Frontend (Presentation Layer)**
2. **Backend (Business Logic Layer)**
3. **Database (Data Layer)**

---

## 🔧 Architecture Components

### 1. Frontend (ECS + ALB)

- React-based SPA hosted on Amazon ECS (Fargate)
- Deployed behind an Application Load Balancer (ALB)
- Static assets served via NGINX container or React build

### 2. Backend (Lambda + API Gateway)

- Modular microservices architecture
- REST APIs created using Node.js
- Deployed as AWS Lambda functions behind API Gateway
- Each service handles a bounded context (e.g., Courses, Users, Enrollments)

### 3. Database (Amazon DocumentDB)

- MongoDB-compatible document store
- Hosted in a private subnet inside a VPC
- Accessed securely via Lambda using VPC peering and IAM roles

---

## 📊 Diagram (Text Representation)


ALB - Public

↓

React Frontend - ECS

↓

API Gateway - Private

↓

AWS Lambda Functions

↓

Amazon DocumentDB - Private Subnet


---

## 🔐 Security

- IAM roles for Lambda access to DocumentDB
- API Gateway authorization (e.g., JWT)
- HTTPS enabled via ALB
- VPC subnets used to isolate backend and database layers

---

## 📦 CI/CD Workflow

- Terraform for infrastructure provisioning
- GitHub Actions for frontend build & deploy
- Backend Lambda deployments using zipped artifacts
- Shared config and environment files managed centrally

---

## 🛠️ Future Enhancements

- Add support for Cognito-based user authentication
- Implement GraphQL gateway
- Use Step Functions for orchestrating workflows (e.g., grading)

---

_Last updated: May 2025_
