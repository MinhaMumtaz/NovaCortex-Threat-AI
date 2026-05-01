# 🛡️ NovaCortex-Threat-AI  (Self-Created Virtualized R&D Lab)

**Author:** Minha Mumtaz  
**Domain:** Software Security • Cybersecurity • Threat Intelligence • Security Analytics • AI  
**Status:** Active Development  

---

## 📌 Overview

**NovaCortex-Threat-AI** is a modular, AI-driven cybersecurity research lab and umbrella initiative. It provides a platform for advanced research in threat intelligence and cyber forensics, following a **research-to-production mindset**. The initiative encompasses multiple sub-projects—some developed (e.g., CortexAI, CortexNexus, OblivionX, VaultX, VaultX-Kernel), some in progress, and others planned—aimed at advancing cybersecurity knowledge, developing innovative tools, and empowering cybersecurity professionals.

---

## 🎯 Problem Statement

Modern security teams face challenges including:

* Fragmented threat intelligence sources  
* Lack of structured IOC normalization  
* Limited explainability in AI-driven threat detection  
* Poor scalability of security tools
* Weak host scanning and compliance with security best practices


**NovaCortex-Threat-AI** addresses these gaps by offering an **end-to-end, automated, and explainable security analytics platform**.

---

## 🧠 Core Capabilities

* Automated threat intelligence feed ingestion  
* IOC normalization and structured storage  
* Ransomware behavioral pattern analysis using AI  
* Explainable ML decisions (e.g., SHAP-based insights)  
* Dockerized, modular security pipelines  
* Automated Host Scan: Detects SSH settings, firewall status, open ports, password policies, critical package updates, and file integrity.
* Policy-as-Code Validation: YAML-driven rules allow easy modification, testing, and expansion.
* AES-256-GCM encryption and decryption
* Strong password-based key derivation (Argon2 for VaultX, PBKDF2-HMAC-SHA256 for VaultX-Kernel)
* OVAL Compliance Checks 
* Research-ready and production-aware architecture

---

## 🧩 Active Sub-Projects

| Project       | Description                                                                 |
| ------------- | --------------------------------------------------------------------------- |
| **CortexAI**  | AI-powered behavioral intelligence framework for cyber threat analysis      |
| **CortexNexus** | Dockerized orchestration pipeline for automated IOC feed management        |
| **OblivionX** | Automated Ubuntu Host Security Scanner with AI-driven Risk Assessment and Policy-as-Code Compliance        |
| **VaultX** | High-level, Python-based, GUI-driven encryption system       |
| **VaultX-Kernel** | Low-level, C-based system cryptography with OpenSSL EVP APIs       |

Each project can be used **independently** or as part of the unified NovaCortex platform.

---

## 🛠️ Tech Stack

* **Languages:** Python, C/C++, Go, Rust, SQL, PHP, JSON  
* **Security:** Threat Intelligence Feeds, IOC Analysis, OVAL Compliance Checks  
* **AI/ML:** Machine Learning, Behavioral Analysis, XAI, Risk Scoring, Feature Attribution  
* **Databases:** SQL-based Structured Storage  
* **DevOps:** Docker, Docker Compose  
* **Data Handling:** Feature Engineering, Normalization Pipelines, Risk Aggregation, Compliance Evaluation, YAML Policy Parsing
* **Virtualization:** VMware, Python Virtual Environment (venv)
* **Operating System:** Ubuntu (VMware Virtual Machine), Windows, Kali Linux
* **High-Level Encryption:** Cryptography library (AES-GCM), argon2 (PBKDF2 alternative)
* **Low-Level Encryption:** C, OpenSSL (EVP AES-256-GCM, PBKDF2-HMAC-SHA256), POSIX libraries (time.h, stdlib.h)



---

## 🔮 Future Enhancements

* Real-time streaming ingestion  
* Graph-based threat correlation  
* MITRE ATT&CK mapping  
* API-based integration with SIEM/SOAR platforms  
* Cloud-native deployment support
* Policy Optimization - Use AI to recommend ideal baseline policies tailored to environment and threat models
* Evaluate side-channel attack resistance in low-level kernel implementation


---

## < Note >
Advanced systems projects **(NovaSentry-X and NovaCortex-Sentinel)** are currently in private development for security research purposes. Documentation and logic walkthroughs are available upon request for technical interviews.
