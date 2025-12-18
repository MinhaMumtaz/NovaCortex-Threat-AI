# ⚡ CortexNexus

---

## 📌 Overview

Cortex Nexus is an **automated, Dockerized threat intelligence automation tool** and a key sub-project of **Nova Cortex Threat AI**.  

It automates the **collection, normalization, and structured storage of threat intelligence feeds** from multiple sources with a single click. This enables security teams and AI analytics pipelines to receive **ready-to-use IOC data efficiently and securely**.

---

## 🎯 Purpose

Cortex Nexus addresses core challenges in threat intelligence automation by:

- Aggregating threat feeds from multiple sources (OTX, Abuse.ch, CEH, PhishTank, FISH, TANK, etc.)
- Automating feed collection, normalization, and structured storage
- Reducing manual intervention while maintaining a **modular design** suitable for research or production
- Seamlessly integrating into the **Nova Cortex Threat AI** ecosystem

---

## 🧩 Modules & Responsibilities

| Module | Purpose |
|--------|---------|
| **FeedHub** | Entry point for multiple threat intelligence feeds; fetches raw data from various sources |
| **AutoCollector** | Collects feeds from FeedHub and stores them locally as raw data |
| **AutoNormalizer** | Reads raw feeds and normalizes/formats them into structured data |
| **AutoFeed Orchestrator** | Main automation hub/scheduler; orchestrates all modules hourly |
| **IntelVault** | Takes normalized feeds, structures them further, and stores them in a database with categorized IOC tables |

> **Note:** Only the **AutoFeed Orchestrator** will be showcased publicly to demonstrate workflow and automation logic. Other modules remain internal to protect intellectual property.

---

## 🧠 Key Capabilities

- Automated feed ingestion from multiple threat intelligence platforms  
- One-click automation through **AutoFeed Orchestrator**  
- Data normalization & structured storage in SQL database  
- Modular architecture enabling independent module operation  
- Dockerized deployment for containerized automation pipelines  

---

## 🛠️ Tech Stack

- **Languages:** Python  
- **DevOps / Containerization:** Docker, Docker Compose  
- **Database:** SQL-based structured storage  
- **Automation & Scheduling:** Python scheduler  
- **Data Handling:** Feature engineering, feed normalization  

---

## 📸 Visual Proof (Screenshots)

- Running Docker containers (`docker ps` screenshot)  
- Database schema (tables and structure)  
- Sample IOC entries (dummy/sanitized data)  

> Screenshots are placed in the `screenshots/` folder.

---

## 🔮 Future Enhancements

- Real-time streaming ingestion from all feeds  
- API-based integration with SIEM / SOAR platforms  
- Enhanced error handling, logging, and monitoring dashboards  
- Integration with Nova Cortex Threat AI analytics modules  

---

## 👩‍💻 Author

**Minha Mumtaz**  
Early-Career Cybersecurity & Threat Intelligence Specialist  
Focused on **AI-driven, automated security systems**  

- GitHub: [profile link]  
- LinkedIn: [to be added]  
- Portfolio Website: [coming soon]  

---

## 📜 Copyright & Usage

© 2025 Minha Mumtaz. All rights reserved.  

> This sub-project is published strictly for **portfolio and evaluation purposes**.  
> No part of this project may be used, copied, modified, or redistributed for commercial or non-commercial purposes without explicit written permission.

