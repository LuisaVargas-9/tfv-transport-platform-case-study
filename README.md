# 🚐 Transportation Management Platform — Technical Case Study

A production-oriented Full Stack platform built to digitize transportation records, operational traceability, vehicle workflows, and GPS-based trip tracking.

The system was developed collaboratively by a multidisciplinary team. I participated as **Full Stack Developer & Project Lead**, contributing directly to development while coordinating the work across frontend, backend, and infrastructure.

> This repository is a public technical case study. Production source code, operational data, credentials, client-specific information, and production UI captures remain private.

---

## 🚀 Project Overview

The platform replaces manual transportation records with a structured digital workflow used by operational and administrative roles.

A central workflow is the digital trip record: a driver registers the trip, identifies the **destination** and the **employee accompanying the trip**, records operational information, and the employee can provide a **signature** as part of the validation process. GPS points are also recorded during active trips to support route traceability.

The solution is maintained across three private codebases:

```text
Frontend                 Backend                  Infrastructure
Vue 3                    NestJS                   Terraform
Pinia                    TypeScript               Ansible
Vue Router               Prisma                   Docker Compose
Tailwind CSS             PostgreSQL               GitHub Actions
Axios                     Redis                    AWS
Socket.IO Client         WebSockets               GHCR
```

---

## 👩‍💻 My Role

**Full Stack Developer & Project Lead**

My work combined direct technical contribution with project coordination. Responsibilities included:

- Coordinating frontend, backend, infrastructure, and development tasks
- Following up on implementation progress and integration between application layers
- Supporting technical decisions and debugging
- Contributing to frontend functionality and backend integration
- Supporting operational workflows, GPS-related functionality, exports, and production improvements
- Participating in deployment-related work and cloud infrastructure coordination

The project was collaborative; the case study does not imply sole authorship of the platform.

---

## ✨ Core Capabilities

### Transportation Operations

- Digital trip registration and management
- Destination and employee association within trip records
- Employee signature collection as part of trip validation
- Trip history and operational traceability
- Driver-oriented workflows
- Role-based administrative workflows

### GPS Tracking

- GPS point recording during active trips
- Route reconstruction and map visualization
- Synchronization of GPS points during the trip lifecycle
- Handling of pending GPS points when a trip is finalized

### Reporting & Exports

- Filtered trip-history reporting
- PDF generation
- Excel exports
- Map-related reporting information
- Document preview and download workflows

### Evidence & Maintenance

- Evidence records with attached files
- Vehicle-related administrative workflows
- Daily and monthly maintenance records
- Maintenance checklist functionality

### Additional Operational Modules

- Service requests
- Quote requests
- Vehicle and driver administration
- Employee and destination management

---

## 🏗️ System Architecture

![Transportation Management Platform Architecture](./images/tfv-architecture.png)

*High-level architecture validated against the private application and infrastructure repositories. Client-specific values and production configuration are intentionally omitted.*

The application uses a Vue frontend and NestJS API. The backend persists relational data in PostgreSQL, uses Redis as an application service, stores files in Amazon S3, and exposes REST and WebSocket-based functionality.

---

## 🛠️ Technology Stack

### Frontend

![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Pinia](https://img.shields.io/badge/Pinia-State_Management-FFD859?style=flat-square)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?style=flat-square&logo=vite&logoColor=white)

Additional technologies: **Vue Router, Axios, Socket.IO Client, Chart.js, ExcelJS, jsPDF, PDF.js, XLSX**.

### Backend

![NestJS](https://img.shields.io/badge/NestJS-11-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-7-2D3748?style=flat-square&logo=prisma&logoColor=white)

Additional technologies: **JWT / Passport, Redis, WebSockets / Socket.IO, AWS S3 SDK, Swagger / OpenAPI, Class Validator, NestJS Throttler, Jest**.

### Cloud & DevOps

![AWS](https://img.shields.io/badge/AWS-EC2_·_RDS_·_S3-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-IaC-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-Provisioning-EE0000?style=flat-square&logo=ansible&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)

---

## ☁️ Infrastructure & Deployment

The AWS infrastructure is defined with **Terraform** and the EC2 server is provisioned with **Ansible**.

Terraform manages the main cloud resources used by the platform:

- VPC, subnets, Internet Gateway, and routing
- EC2 instances and Elastic IPs
- RDS PostgreSQL
- Amazon S3
- Security Groups
- IAM

The application services run with **Docker Compose on EC2**. The deployment includes frontend, backend, and Redis containers, while the backend connects to RDS PostgreSQL and Amazon S3.

```text
Code Change
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions
    │
    ▼
Build & Publish Docker Image
    │
    ▼
GitHub Container Registry (GHCR)
    │
    ▼
AWS EC2
    │
    ▼
Docker Compose
    ├── Vue Frontend
    ├── NestJS Backend
    └── Redis

Backend ─────► RDS PostgreSQL
Backend ─────► Amazon S3
```

### Environments

The infrastructure and deployment workflow support separate **production**, **development**, and **test** environments.

---

## 🧪 Testing & Quality

The NestJS backend includes Jest-based testing infrastructure with scripts for unit tests, watch mode, coverage, debugging, and end-to-end test configuration.

The project also involved iterative production-oriented improvements around authentication, GPS synchronization, reporting, exports, operational workflows, and deployment reliability.

---

## 🔐 Product Scope & Confidentiality

This case study intentionally documents the **engineering scope and architecture** without publishing sensitive production details.

The following remain private:

- Production source repositories
- Production UI screenshots and internal workflows
- Customer and organization information
- Employee and user data
- Signatures and validation records
- Vehicle identifiers and operational records
- Addresses and GPS route data
- Credentials and environment secrets
- Terraform state and production infrastructure values

The architecture diagram is therefore a high-level representation rather than a reproduction of production configuration.

---

## 📌 Repository Status

Maintained as part of my software development portfolio.

---

## 👩‍💻 Portfolio Owner

**Luisa Vargas**  
Full Stack Developer & Project Lead

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Luisa_Vargas-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/luisa-vargas-233494200/)
