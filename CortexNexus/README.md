# ⚡ CortexNexus

---

## 📌 Overview

Cortex Nexus is an **automated, Dockerized threat intelligence automation tool** and a key sub-project of **Nova Cortex Threat AI**.  

It automates the **collection, normalization, and structured storage of threat intelligence feeds** from multiple sources with a single click. This enables security teams and AI analytics pipelines to receive **ready-to-use IOC data efficiently and securely**.

---

## 🎯 Purpose

Cortex Nexus addresses core challenges in threat intelligence automation by:

- Aggregating threat feeds from multiple sources (OTX, Abuse.ch [MalwareBazaar, FeodoTracker, SSL Blacklist, URLhaus, ThreatFox, YaraIFY], PhishTank)
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

- Running Docker containers (screenshot)  
- Database schema (tables and structure)  
- Sample IOC entries (dummy/sanitized data)  

---

## 🔮 Future Enhancements

- Real-time streaming ingestion from all feeds  
- API-based integration with SIEM / SOAR platforms  
- Enhanced error handling, logging, and monitoring dashboards  
- Integration with Nova Cortex Threat AI analytics modules  

---
