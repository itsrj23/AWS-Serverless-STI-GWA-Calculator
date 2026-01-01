# AWS Serverless GWA Calculator

## Overview

> *AWS Serverless GWA Calculator* is a cloud-native web application designed to compute a student’s **General Weighted Average (GWA)** based on the **STI Tertiary Student Handbook (Admit Year 2022–2023)**.  
>  
> This project showcases **Cloud and DevOps Engineering practices** using AWS serverless services, Infrastructure as Code, and CI/CD automation.

---

## Project Description

The application allows students to input their **subjects, number of units, and final grades**, then accurately computes their **GWA** following official academic rules.

It uses a **serverless architecture** where the frontend is hosted as a static website and the backend computation is handled by AWS Lambda through a REST API.

---

## GWA Computation Rules

- Only **numeric grades** are included
- Courses with **INC, DRP, or Failed (5.00)** are excluded
- **Non-credit courses** (e.g., NSTP) are excluded
- Computation strictly follows the **STI Tertiary Student Handbook**

---

### GWA Formula

\[
\text{GWA} = \frac{\sum (\text{Final Grade} \times \text{Units})}{\sum (\text{Total Units})}
\]

---


---

## Technology Stack

### Frontend Tools
- **HTML5** – page structure
- **Bootstrap 5** – responsive UI design
- **JavaScript (Vanilla JS)** – form handling and API calls
- **Amazon S3** – static website hosting
- **Amazon CloudFront** – CDN and HTTPS support

### Backend & Cloud Services
- **AWS Lambda** – serverless computation logic
- **Amazon API Gateway** – REST API exposure
- **AWS IAM** – access control and security

### DevOps & Automation
- **AWS SAM** – Infrastructure as Code
- **GitHub Actions** – CI/CD pipeline

---

## Features

- 📘 Handbook-compliant GWA computation
- 🌐 Web-based and mobile-responsive UI
- ⚡ Fully serverless and scalable
- 🔐 Secure and cost-efficient architecture
- 🚀 Automated deployment using CI/CD

---

## Sample Input

```json
{
  "courses": [
    { "name": "IT101", "units": 3, "grade": 1.75 },
    { "name": "IT102", "units": 3, "grade": 2.00 },
    { "name": "GE101", "units": 2, "grade": 1.50 }
  ]
}


## System Architecture

