

<!-- Tool Logos -->
<p align="left">
  <img src="https://upload.wikimedia.org/wikipedia/commons/5/58/XGBoost_logo.svg.svg" alt="Postgres" width="40" height="40"/>
  <img src="https://en.wikipedia.org/wiki/Python_%28programming_language%29#/media/File:Python-logo-notext.svg" alt="Such" width="40" height="40"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="MySQL" width="40" height="40"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="VS Code" width="40" height="40"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" alt="Docker" width="40" height="40"/>
  <img src="https://user-images.githubusercontent.com/38404461/65588818-7734b500-df88-11e9-907c-a0bc0c0fdfc1.png" alt="SHAP" width="60" height="60"/>
  <img src="https://media2.dev.to/dynamic/image/width=1000,height=420,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F7w8rh2oj5arc1epo2sls.png.png" alt="Such" width="40" height="40"/>
  <!-- Add more logos here if needed -->
</p>

📌 **Caption**  
**Figure 1: CortexAI Modular Detection Pipeline Architecture**

📌 **Pipeline Name**  
**CortexAI Modular Behavioral Intelligence Pipeline**

---

## **Module Overview**

CortexAI is built as a **modular, containerized research framework**. Each module can operate **standalone** for experimentation or **integrated** as part of the full behavioral intelligence pipeline.

| Module               | Overview                                                                 |
| -------------------- | ------------------------------------------------------------------------ |
| **Zeek Sensor**      | Captures live network traffic or processes raw PCAP files for analysis. |
| **Log-to-CSV Converter** | Converts raw Zeek logs into structured CSV files; supports controlled folder selection. |
| **Feature Engine**   | Extracts behavioral features from logs for generalized threat detection. |
| **Labeling Engine**  | Merges features, applies labels, and prepares balanced datasets.        |
| **Inference Engine** | Generates behavioral verdicts using trained ML models; supports research-focused evaluation. |

> ⚠️ Modules are **containerized** and can be executed independently for analysis or as part of the full pipeline.  

---

## **Reference Diagram**

📌 **Diagram Location:** `diagrams/`  

💡 **Figure Insight:**  
The architecture diagram visually presents the **data flow** from raw traffic ingestion → feature extraction → labeling → inference. Arrows indicate the **processing sequence**, while module independence emphasizes **research flexibility**.

---

## **Key Notes**

- Supports **standalone testing** and **integrated end-to-end evaluation**.  
- Focuses on **behavioral learning** rather than family-specific malware signatures.  
- Designed for **ethical, IP-safe research**—internal detection logic and thresholds are intentionally abstracted.  
- Enables **robust experimentation** with both known and unseen ransomware families, as well as benign traffic.

---

### 💡 Summary

The **CortexAI Modular Behavioral Intelligence Pipeline** provides a **flexible, modular framework** that balances **research transparency** with **IP protection**, supporting advanced behavioral threat analysis in both standalone and integrated modes.

