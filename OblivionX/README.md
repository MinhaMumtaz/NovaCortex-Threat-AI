# OblivionX – Ubuntu Host Security Scanner  
### Automated Host Security Assessment and Reporting with Explainable AI

---

## 📑 Table of Contents

1. [Project Overview](#project-overview)  
2. [Purpose and Motivation](#purpose-and-motivation)  
3. [Core Features](#core-features)  
4. [Methodologies and Technologies](#methodologies-and-technologies)  
5. [Project Architecture & Workflow](#project-architecture--workflow)  
6. [Terminology](#terminology)  
7. [AI Risk Assessment & Explainability](#ai-risk-assessment--explainability)  
8. [Policy-as-Code Implementation](#policy-as-code-implementation)  
9. [OVAL Compliance Validation](#oval-compliance-validation)  
10. [File Integrity and Host Configuration Checks](#file-integrity-and-host-configuration-checks)  
11. [How to Use OblivionX](#how-to-use-oblivionx)  
12. [Installation & Setup](#installation--setup)  
13. [Example Output](#example-output)  
14. [Impact & Use Cases](#impact--use-cases)  
15. [Contributing](#contributing)  
16. [License](#license)

---

## 🔍 Project Overview

**OblivionX** is an advanced, automated security scanning and assessment framework for **Ubuntu hosts**, designed to perform:

- Comprehensive host configuration audits  
- File integrity verification  
- Policy-as-Code evaluation  
- OVAL compliance checks  
- AI-based risk assessment with explainability  

It consolidates multiple layers of host security validation into a **single, clean, human-readable report**, focusing strictly on **non-compliant configurations** to ensure actionable insights.

This makes OblivionX **enterprise-ready**, audit-friendly, and ideal for compliance-driven environments.

---

## 🎯 Purpose and Motivation

The primary motivation behind OblivionX is to provide:

- Automated security validation for Ubuntu systems  
- Explainable, actionable insights for security engineers and sysadmins  
- Clear distinction between **compliant** and **non-compliant** configurations  
- A policy-driven, testable, and repeatable security baseline  
- A practical demonstration of AI-driven security assessment  

Organizations like **Canonical** value repeatability, transparency, and standards-based security. OblivionX reflects **engineering maturity**, **security reasoning**, and **design clarity**.

---

## ⭐ Core Features

### 1️⃣ Host Configuration Audit
- SSH root login status  
- Sudo user verification  
- Password policy evaluation (max days, retry limits)  
- Firewall status  
- Open ports enumeration  
- OS and OpenSSL version detection  
- Pending package updates  

### 2️⃣ File Integrity Checks
- Critical system files:
  - `/etc/passwd`
  - `/etc/shadow`
  - `/etc/group`
  - `/etc/gshadow`
- Configuration files:
  - `/etc/ssh/sshd_config`
  - `/etc/ufw/ufw.conf`

### 3️⃣ Policy-as-Code Evaluation
- YAML-defined security baselines  
- Automated compliance validation  
- Structured non-compliance reporting  

### 4️⃣ OVAL Compliance Checks
- Evaluates Ubuntu hosts against OVAL definitions  
- Highlights only non-compliant rules  

### 5️⃣ AI-Based Risk Assessment
- Computes host risk scores  
- Provides explainable reasoning for risk factors  
- Enables prioritized mitigation  

### 6️⃣ Clean Reporting
- Human-readable final report  
- Focused on non-compliance  
- Audit- and executive-ready  

---

## 🧠 Methodologies and Technologies

- **Python 3.x** – Core implementation  
- **YAML** – Policy-as-Code definitions  
- **JSON** – Structured outputs for reporting and AI  
- **Subprocess Automation** – Orchestrates scans and evaluations  
- **Explainable AI (XAI)** – Risk scoring with transparency  
- **OVAL (Open Vulnerability and Assessment Language)** – Standardized compliance checks  
- **Cryptographic Hashing** – File integrity verification  
- **Virtual Environments (venv)** – Reproducible execution  

---

## 🏗️ Project Architecture & Workflow

```text
host_scan.py
      ↓
policy_evaluator.py
      ↓
ai_runner.py
      ↓
report_generator.py

