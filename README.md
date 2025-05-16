# Serverless LMS

A scalable, modern **Learning Management System (LMS)** built using the **MERN stack** with a **serverless and microservices architecture**.

This project is designed for high availability, flexibility, and easy deployment using AWS-managed services such as **Lambda**, **API Gateway**, **ECS**, and **DocumentDB**.

---

## 📁 Project Structure

| Directory     | Description |
|---------------|-------------|
| `Ansible/`    | Contains Ansible playbooks for provisioning EC2 instances and performing post-deployment configuration tasks. |
| `Backend/`    | Microservices built using Node.js, deployed via AWS Lambda behind API Gateway. Handles all core logic like user management, course handling, etc. |
| `Docs/`       | Documentation files, architecture diagrams, and design decisions. Useful for onboarding and reference. |
| `Frontend/`   | React-based web application deployed on Amazon ECS behind an Application Load Balancer (ALB). Serves the UI for students, instructors, and admins. |
| `Pipeline/`   | CI/CD pipeline configurations using Jenkins. Contains scripts and Jenkinsfiles to automate build, test, and deployment processes. |
| `Shared/`     | Shared utilities, libraries, and configurations used across backend microservices and frontend components. |
| `Terraform/`  | Terraform code to provision and manage AWS infrastructure (Lambda, API Gateway, ECS, DocumentDB, IAM roles, etc.). |
| `README.md`   | You're here! The entry point and guide to understanding this repository. |

---

## 🚀 Tech Stack

- **Frontend:** React, ECS, ALB
- **Backend:** Node.js (Express), AWS Lambda, API Gateway
- **Database:** Amazon DocumentDB (MongoDB-compatible)
- **Infrastructure as Code:** Terraform
- **Provisioning & Configuration:** Ansible
- **CI/CD:** Jenkins running on EC2
- **Architecture:** Microservices + Serverless

---

## 📦 Deployment Overview

1. **Infrastructure Setup:** Use Terraform modules under `Terraform/` to provision cloud resources.
2. **Configuration:** Run Ansible playbooks from `Ansible/` to configure EC2 instances (e.g., Jenkins server).
3. **Build & Deploy:** Use Jenkins jobs defined in the `Pipeline/` directory to automate deployment of the frontend, backend, and infrastructure.
4. **Access the LMS UI:** The frontend hosted on ECS will be publicly accessible via the Application Load Balancer.

---

## 📚 Documentation

Refer to the `Docs/` directory for:

- Detailed architecture diagrams
- Sequence flows
- Environment setup guides
- Developer onboarding instructions

---

## 🤝 Contributing

We welcome contributions! Please review the guidelines in `Docs/CONTRIBUTING.md` (if available) and open an issue or pull request.

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE).

---

## 🧑‍💻 Maintainer

**Nabeel Hassan**  
DevOps | Cloud Architect | Trainer  
[LinkedIn](https://www.linkedin.com/in/thenabeelhassan/) | [YouTube - DevOps Medium](https://www.youtube.com/@DevOpsMedium) | [GitHub](https://github.com/thenabeelhassan)

---

> **DevOps Made Simple** – One LMS at a time.
