 **Behavioral Dataset Construction Workflow**

---

## **1️⃣ Data Sources**

CortexAI’s behavioral dataset is sourced from multiple, diverse traffic streams to ensure **robust generalization**:

| Source | Description |
| ------ | ----------- |
| **Zeek Logs** | Captures live network traffic from hosts or simulated environments. |
| **CTU Normal Traffic (Stratosphere Lab)** | Benign network traffic datasets for comparison and validation. |
| **University of Navarra Ransomware Repository** | PCAP files of multiple ransomware families for behavioral analysis. |
| **CIC-IDS-2017(PCAPs)** | PCAP files of benign and malicios traffic for behavioral analysis. |
| **Other Public Sources** | Supplementary traffic sources as needed for diversity and coverage. |

> ⚠️ All sources are preprocessed and anonymized to maintain **ethical research standards**.
---

## **2️⃣ Dataset Distribution**

![Dataset Distribution Pie Chart](cortexai_dataset_distribution.png)

**Figure 2: Dataset Distribution – Benign vs. Ransomware Behavioral Samples**

> 💡 This pie chart illustrates the proportion of **benign and malicious traffic samples** in the CortexAI dataset, emphasizing balanced representation for **behavioral learning**.

---
---

## **3️⃣ Feature Categories**

To capture **comprehensive network behavior**, features are extracted across multiple categories:

| Category | Description |
| -------- | ----------- |
| **Connection Features** | Network flow metrics such as packet counts, byte totals, and connection duration. |
| **DNS Features** | Query frequency, domain entropy, response anomalies. |
| **DHCP Features** | IP lease patterns, request timings, and allocation behavior. |
| **SMB Features** | File sharing activity, request patterns, and session metadata. |
| **Temporal Features** | Timing patterns, session intervals, and burst analysis. |

> 💡 Features are selected for **behavioral significance**, not family-specific signatures.

---

## **4️⃣ Top Features – CortexAI Dataset (Ransomware Detection)**

| Feature | Description |
| ------- | ----------- |
| `conn_conn_count` | Number of connections; high activity may indicate ransomware propagation. |
| `conn_unique_dest_ips` | Diversity of destination IPs; abnormal patterns highlight suspicious communication. |
| `conn_total_orig_bytes` | Total bytes sent; excessive outgoing traffic often signals exfiltration. |
| `conn_total_resp_bytes` | Total bytes received; helps detect anomalous response sizes. |
| `conn_avg_duration` | Average connection duration; very short or very long durations can indicate attacks. |
| `conn_port_entropy` | Variation of destination ports; unusual port usage can be malicious. |
| `dns_dns_query_count` | Number of DNS queries; abnormal spikes suggest command-and-control activity. |
| `dns_unique_domains` | Count of unique queried domains; ransomware often contacts multiple domains. |
| `files_file_transfer_count` | Number of files transferred; ransomware modifies/copies files. |
| `files_file_entropy` | Entropy of transferred files; high randomness may indicate encryption. |
| `pe_unsigned_ratio` | Ratio of unsigned PE files; unsigned executables are suspicious. |
| `pe_no_aslr_ratio` | Proportion of binaries without ASLR; lack of memory protection is a red flag. |
| `ssl_ssl_established_ratio` | Ratio of successful SSL connections; malware may attempt stealthy encrypted communication. |
| `ntlm_ntlm_failure_ratio` | Failed authentication attempts; unusual failures may reveal lateral movement. |
| `conn_zscore_conn_count_vs_baseline` | Deviation from normal traffic patterns; highlights anomalies. |

✔ These features were carefully selected to **maximize behavioral discrimination** between malicious and benign traffic.

---

## **5️⃣ Labeling Strategy**

- Labels are applied **per traffic type**: `benign` or `malicious`.  
- For ransomware, the **family label** is recorded separately for analytical purposes.  
- Labeling follows **standardized, reproducible logic** to support research transparency.

---

## **6️⃣ Dataset Merging Logic**

- Individual log CSVs from different sources are **merged into unified datasets** per module.  
- Steps include:  
  1. Column alignment and normalization  
  2. Feature consistency checks  
  3. Deduplication and balancing  
- Ensures that **combined datasets maintain behavioral diversity** without bias.

---

## **7️⃣ Train / Test / Unseen Family Separation**

- **Training Set** – Balanced selection of ransomware families and benign traffic.  
- **Testing Set** – Separate portion of known families for model evaluation.  
- **Unseen Family Set** – Fully excluded ransomware families reserved for **behavioral generalization testing**.  

> This separation ensures that **model evaluation reflects true behavioral learning** rather than memorization.

---

## **8️⃣ Analytical Process (High-Level)**

Instead of raw logs or code, the dataset was constructed strategically:

1. Categorized network logs by protocol and type  
2. Engineered features relevant to **behavioral patterns**  
3. Standardized labels for **training and evaluation**  
4. Maintained separation between **training and unseen families** to validate generalization  

> 💡 This ensures the dataset is **research-ready, reproducible, and focused on behavioral learning**.

---

### 💡 Summary

The **CortexAI Behavioral Dataset** enables:  

- Detection of **unseen ransomware families** through generalized behavior  
- Robust discrimination between **malicious and benign traffic**  
- Transparent, reproducible, and **ethically sourced data**  

> All preprocessing, feature selection, and merging steps are **fully documented** for review and analytical rigor.
