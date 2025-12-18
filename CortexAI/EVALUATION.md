## 🔴 Confusion Matrix Evaluation — Unseen Ransomware Families

To evaluate classification performance, confusion matrix heatmaps were generated
for **three ransomware families not included during training**.

These visualizations illustrate the system’s ability to correctly identify
malicious behavior while minimizing false negatives.

<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/cerber_heatmap.png" alt="Cerber" width="450" height="450"/>

##### Figure 5: Confusion Matrix — Cerber (Unseen Ransomware Family) 

---
<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/Stop_heatmap.png" alt="Stop" width="450" height="450"/>

##### Figure 6: Confusion Matrix — STOP (Unseen Ransomware Family)

---
<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/phobos_heatmap.png" alt="Phobos" width="450" height="450"/>

##### Figure 7: Confusion Matrix — Phobos (Unseen Ransomware Family)


**Interpretation**

- High true-positive rates across all unseen families
- No reliance on family-specific signatures
- Confirms behavior-driven classification

---
## 🟢 Benign Traffic Evaluation — False Positive Analysis

CortexAI was evaluated against **benign network traffic**
to assess false positive behavior and robustness.

Benign samples were sourced from:

- Stratosphere Labs normal traffic datasets (two samples)
- Additional real-world benign traffic capture

<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/stratosphere%20lab%20sample-1.png" alt="stratosphere lab sample-2" width="450" height="450"/>

##### Figure 8: Confusion Matrix — Benign Traffic (Stratosphere Lab - Sample#1)

---
<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/stratosphere%20lab%20sample-2.png" alt="stratosphere lab sample-1" width="450" height="450"/>

##### Figure 9: Confusion Matrix — Benign Traffic (Stratosphere Lab - Sample#2)

---
<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/Benign-2.png" alt="Benign-2" width="450" height="450"/>

##### Figure 10: Confusion Matrix — Benign Traffic (UNSW-NB15 - PCAP files)


**Interpretation**

- Low false-positive rates across benign datasets
- Misclassifications occur primarily during bursty legitimate activity
- Confirms controlled sensitivity of behavioral detection

---
## 🧠 Behavioral Generalization — Detection Rate on Unseen Families

To assess behavioral generalization, CortexAI was evaluated on
**seven ransomware families not present in training data**.

The chart below shows the **detection rate (%)** for each unseen family,
based purely on behavioral characteristics.

<img src="https://github.com/MinhaMumtaz/NovaCortex-Threat-AI/blob/main/CortexAI/diagrams/Behavioral%20generalization%20on%20unseen%20families.png" alt="behavioral generalization" width="800" height="800"/>

###### Figure 11: Behavioral Detection Rate Across Unseen Ransomware Families

**Interpretation**

- High detection rates across all unseen families
- Performance consistency confirms family-agnostic learning
- Validates CortexAI’s ability to generalize beyond known threats

## ✅ Evaluation Summary

The evaluation results demonstrate that CortexAI:

- Detects ransomware based on **behavior**, not signatures
- Generalizes effectively to **previously unseen families**
- Maintains low false-positive rates on benign traffic
- Produces consistent, interpretable outcomes

These results confirm CortexAI as a **research-grade behavioral detection framework**
suitable for advanced cyber threat analysis.

