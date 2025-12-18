# **CortexAI**  
**_An AI-Powered Behavioral Intelligence Framework for Cyber Threat Analysis_**  

---

## 1️⃣ **Project Overview**  

CortexAI is a **modular, AI-driven behavioral intelligence framework** for advanced network traffic analysis.  
Unlike traditional signature-based systems, CortexAI learns **generalized behavioral patterns** to distinguish malicious activity from benign traffic — enabling detection **beyond known malware families**.  

**Key Highlights:**  
✨ Modular system design  
✨ Behavioral generalization  
✨ Model explainability  
✨ Ethical handling of sensitive detection logic  

---

## 2️⃣ **Problem Statement**  

Modern cyber threats evolve **rapidly**, making signature-based detection **ineffective**.  
Most ML models overfit to **family-specific patterns**, limiting their ability to detect **unknown or zero-day threats**.  

CortexAI solves this by:  
✅ Learning **behavioral characteristics** of network traffic, not signatures  
✅ Providing a **modular research pipeline** for controlled experimentation  
✅ Maintaining **ethical abstraction** of sensitive detection logic  

---

## 3️⃣ **Dataset Creation & Behavioral Learning**  

CortexAI is trained on a **self-created, balanced dataset** with multiple ransomware families and benign traffic.  

**Objective:** Behavioral learning — not family identification.  

📄 Detailed documentation: `DATASET_CREATION.md`  

**Covers:**  
- Raw PCAP sourcing from **University of Navarra Ransomware Repository**  
- Log conversion, feature engineering, preprocessing  
- Labeling logic & dataset balancing  
- Ethical considerations for **generalization & misuse prevention**  

**Why It Matters:**  
🌟 Detects **previously unseen ransomware families**  
🌟 Discriminates **malicious vs benign traffic** across diverse sources  

**Future Work:**  
- Expand traffic scenarios  
- Refine behavioral feature representations  
- Improve **generalization across evolving threats**  

> *Dataset visuals emphasize behavioral diversity — research-driven, not inflated.*  

---

## 4️⃣ **Modular Pipeline Overview**  

CortexAI features **containerized modules**, each a standalone research tool:  

| Module               | Purpose                                                   |
| -------------------- | --------------------------------------------------------- |
| Zeek Sensor          | Captures live traffic or processes PCAP files             |
| Log-to-CSV Converter | Converts raw logs with controlled manual folder selection |
| Feature Engine       | Performs feature extraction on categorized logs           |
| Labeling Engine      | Handles feature merging and labeling operations           |
| Inference Engine     | Applies trained models to generate behavioral verdicts    |

> ⚠️ Internal detection logic, feature thresholds, and model internals are **abstracted for security & IP protection**  

---

## 5️⃣ **Architecture & Activity Diagrams**  

**Diagrams included:**  
- **Architecture Diagram** — All Dockerized modules, traffic ingestion → inference  
- **Activity Diagram** — Execution flow, manual analyst decisions, research control points  
- **Dataset Pipeline Flowchart** — PCAP → CSV → Feature Engineering → Labeling  

📁 Available in: `diagrams/`  

---

## 6️⃣ **System Testing & Generalization Results**  

**Evaluation:** Known & **unseen ransomware families**, plus benign traffic  

**Key Results:**  

**Unseen Ransomware Families**  
✅ 90%-100% detection accuracy  
✅ No prior family labels  
✅ True behavioral generalization  

**Benign Traffic**  
✅ 100% on live host traffic  
✅ 90–95% on Stratosphere Labs normal traffic  

**Impact:**  
🌟 Confirms learning of **generalized malicious behavior**  
🌟 Demonstrates robustness beyond training data  
🌟 Validates research-oriented design & analytical rigor  

---

## 7️⃣ **Security & IP Notice**  

To protect research integrity:  
- **Not disclosed:** Behavioral detection rules, feature weights, model internals  
- Focus: Architecture, workflow, abstracted dataset methodology, evaluation results  
- Detailed internals available **under NDA** for academic/professional review  

---

## 8️⃣ **Future Work & Research Potential**  

- Expand datasets across **diverse network environments**  
- Introduce **explainability metrics**  
- Integrate inference with **real-time monitoring** (research mode)  
- Publish **anonymized analytical findings** for research  

---

### ✅ **Final Verdict**  

This README demonstrates:  
🌟 Deep analytical thinking  
🌟 Differentiation from “model-only” projects  
🌟 IP protection  
🌟 Recruiter- & researcher-friendly clarity  

**Ready to upload and showcase your expertise!**

