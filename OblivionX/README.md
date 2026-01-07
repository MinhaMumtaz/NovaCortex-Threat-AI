

# 🛡️ OblivionX – Ubuntu Host Security Scanner  
**Automated Host Security Assessment and Reporting with Explainable AI**

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

## 📌 Project Overview
**OblivionX** is an advanced, automated security scanning and assessment framework for **Ubuntu hosts**, designed to perform:

- Comprehensive host configuration audits  
- File integrity verification  
- Policy-as-Code evaluation  
- OVAL compliance checks  
- AI-based risk assessment with explainability  

It consolidates multiple layers of host security validation into a **single, clean, human-readable report**, focusing on **actionable insights** by highlighting **only non-compliant configurations and policies**.  
OblivionX is **enterprise-ready** and ideal for audits, compliance reviews, and security assessments.

---

## 🎯 Purpose and Motivation
The primary motivation behind OblivionX is to provide:

- Automated security validation for Ubuntu hosts  
- Actionable and **explainable** insights for system administrators and security engineers  
- Clear differentiation between compliant and non-compliant configurations  
- A **policy-driven** approach for repeatable and testable security baselines  
- A showcase of **AI-driven security assessment** aligned with modern enterprise security frameworks  

Organizations like **Canonical** require repeatable, verifiable, and explainable security mechanisms.  
OblivionX demonstrates both **technical depth** and **strategic security thinking**.

---

## Core Features

### 1. Host Configuration Audit
- SSH root login status  
- Sudo user verification  
- Password policy evaluation (max days, retry limits)  
- Firewall status  
- Open ports enumeration  
- OS and OpenSSL versions  
- Pending package updates  

### 2. File Integrity Checks
- Critical system files  
  - `/etc/passwd`  
  - `/etc/shadow`  
  - `/etc/group`  
  - `/etc/gshadow`  
- Configuration files  
  - `/etc/ssh/sshd_config`  
  - `/etc/ufw/ufw.conf`  

### 3. Policy-as-Code Evaluation
- YAML-defined security baselines  
- Automated compliance checks  
- Non-compliant policies highlighted  

### 4. OVAL Compliance Checks
- Evaluates Ubuntu hosts against OVAL definitions  
- Highlights non-compliant rules in reports  

### 5. AI-Based Risk Assessment
- Computes host risk scores  
- Provides explainable reasoning for each risk factor  
- Helps prioritize mitigation  

### 6. Clean Reporting
- Human-readable final report  
- Displays **only non-compliant items**  
- Ready for audits, executive review, or security engineering teams  

---

## Methodologies and Technologies
- **Python 3.x** – Core programming language  
- **YAML** – Policy definitions as code (Policy-as-Code)  
- **JSON** – Structured input/output for AI and reporting  
- **Subprocess Automation** – Orchestrates scans, policy evaluation, AI analysis, and reporting  
- **Explainable AI (XAI)** – Risk scoring with transparent reasoning  
- **OVAL (Open Vulnerability and Assessment Language)** – Standardized compliance checks  
- **Hashing** – Integrity verification of critical system files  
- **Virtual Environment (venv)** – Isolated and reproducible Python environment  

---

## Project Architecture & Workflow


---

## Terminology

- **Policy-as-Code (PaC):** Security rules defined as YAML code for automated evaluation.
- **OVAL:** Open standard for vulnerability and compliance assessment.
- **Explainable AI:** AI that provides human-understandable reasoning behind risk predictions.
- **Non-Compliant:** Host setting, policy, or rule that violates the defined security baseline.
- **Critical System File Hash:** Cryptographic hash of system files to ensure integrity.

---

## AI Risk Assessment & Explainability

The AI model in **OblivionX**:

- Computes a **risk score (0–1.0)** for each host
- Categorizes risk into **Low**, **Medium**, or **High**
- Uses **explainable AI** to show exact settings contributing to risk
- Focuses on **non-compliant configurations** to prioritize mitigation

### 🔍 Example Features Analyzed

- Unsafe SSH configurations
- Weak or expired password policies
- Open high-risk ports
- Non-compliant OVAL rules

---

## Policy-as-Code Implementation

- Policies are defined in **YAML format** (`policies/ubuntu_baseline.yaml`).
- Each policy includes:
  - **id:** Unique identifier
  - **description:** Human-readable explanation
  - **check:** Host setting to evaluate
  - **expected** or **max:** Expected value or threshold
  - **severity:** High, Medium, or Low
- The evaluator compares scan results with policy expectations, flags **non-compliance**, and outputs a clean **JSON** structure for reporting.

---

## OVAL Compliance Validation

- Checks Ubuntu hosts against predefined **OVAL rules**
- Highlights **only non-compliant rules** for clarity
- Example rules include:
  - Firewall status
  - SSH key authentication
  - Kernel hardening (`sysctl net.ipv4.ip_forward`)
  - SELinux / AppArmor enforcement
  - Password policies

---

## File Integrity and Host Configuration Checks

- Critical system files are **hashed** and compared against known trusted values
- Detects **unauthorized modifications**
- Checks key host settings, including:
  - SSH login settings
  - Firewall and network configurations
  - Installed OpenSSL and OS versions
  - Pending package updates
  - Open ports

---

## Example Output

### Final Report (Generated by OblivionX)

[final_report.txt ↗](final_report.txt)


## Impact & Use Cases

- **Security Auditing:** Automated Ubuntu host security validation
- **Enterprise Deployment:** Repeatable, auditable, and policy-driven compliance reports
- **Canonical-Ready:** Clear, concise, and non-compliance-focused reporting for executives and security engineers
- **Educational & Portfolio Value:** Demonstrates expertise in Python, security scanning, AI-driven analysis, OVAL, and policy-as-code


---
