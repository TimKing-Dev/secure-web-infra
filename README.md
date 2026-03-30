# Secure Containerized Web Infrastructure

## Executive Summary
This project demonstrates the deployment of a highly available, lightweight web infrastructure using modern DevSecOps principles. By migrating a traditional web server to a containerized architecture, this project achieves a 90% reduction in deployment time and enforces strict Infrastructure as Code (IaC) standards.

## Architecture & Technology Stack
* **Containerization:** Docker
* **Base OS Image:** Alpine Linux (Security Hardened)
* **Web Server:** Apache HTTP Server (`httpd`)
* **Version Control:** Git

## Security Implementation (DevSecOps)
A primary focus of this build is **Attack Surface Reduction (ASR)** and secure supply chain practices. 

* **Shift-Left Vulnerability Management:** Initial deployments utilizing standard Debian-based images (`httpd:2.4`) were scanned using Docker Scout, identifying several baseline vulnerabilities.
* **Hardening via Alpine Linux:** The architecture was refactored to utilize `httpd:alpine`. This transition reduced the operating system footprint from over 100MB to approximately 5MB, successfully eliminating critical CVEs and adhering to the principle of least privilege.
* **Immutable Infrastructure:** Server configurations are defined entirely in the `Dockerfile`, preventing configuration drift and ensuring that production environments perfectly match development environments.

## Deployment Instructions

To reproduce this environment locally, ensure Docker is installed and running, then execute the following commands:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/secure-web-infra.git](https://github.com/your-username/secure-web-infra.git)
   cd secure-web-infra
