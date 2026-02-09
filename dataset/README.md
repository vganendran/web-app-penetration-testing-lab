# Web Application Penetration Testing Project

## Overview
This project demonstrates an ethical penetration testing assessment conducted on a simulated web application environment. The objective of the assessment was to identify common web application security vulnerabilities, evaluate associated risks, and provide remediation recommendations aligned with industry best practices.

All testing and analysis were performed in a controlled lab environment using intentionally vulnerable applications and simulated datasets for educational purposes only.

---

## Project Objectives
- Identify common web application vulnerabilities
- Map findings to OWASP Top 10 categories
- Analyze security risks based on impact and likelihood
- Provide clear and actionable remediation guidance
- Demonstrate structured penetration testing documentation

---

## Target Environment
- **Application Type:** Web-based E-commerce Application
- **Simulated Platform:** OWASP Juice Shop
- **Hosting:** Local lab environment (Docker-based)
- **Data:** Fictional and simulated datasets

---

## Methodology
The assessment follows a structured penetration testing approach aligned with:
- OWASP Testing Guide
- OWASP Top 10 (2021)
- Penetration Testing Execution Standard (PTES)

Testing phases include reconnaissance, threat modeling, vulnerability identification, validation, risk assessment, and reporting.

---

## Key Findings
| Vulnerability | OWASP Category | Risk Level |
|--------------|---------------|------------|
| SQL Injection | A03: Injection | High |
| Cross-Site Scripting (XSS) | A03: Injection | Medium |

Detailed findings are documented in the `/findings` directory.

---

## Dataset Source and Usage
The dataset used in this project is **simulated security data** designed to reflect realistic web application behavior. Data sources include:
- Simulated HTTP request logs
- Authentication attempt records
- Application configuration information
- User role definitions

The dataset does **not** contain real user data or production logs and is used solely for security analysis and documentation purposes.

---

## Repository Structure

