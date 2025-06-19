## 🛡️ The CIA Triad: Foundation of Information Security


**+ CVSS Scoring & Real-World Exploits**

> *"Confidentiality, Integrity, and Availability aren't just principles — they're the pillars every secure system stands on."*

---

## 📖 Introduction

In the complex world of cybersecurity, the **CIA Triad** — **Confidentiality, Integrity, and Availability** — remains a timeless and foundational model. This triad defines the core objectives of security efforts and offers a lens through which threats can be assessed.

In this guide, we’ll explore:

* 🔐 Advanced interpretations of each CIA pillar
* 💣 Real-world vulnerabilities (CVEs) that impact CIA
* 🧮 How CVSS (Common Vulnerability Scoring System) quantifies risk

---

## 🔐 The CIA Triad — Beyond the Basics

### 1. 🕵️ Confidentiality

> “Only the right people access the right information.”

**Breach Risk:** When sensitive data is disclosed to unauthorized entities.

**🔒 Key Safeguards:**

* **Encryption** (AES, TLS, RSA) — Data at rest and in transit
* **Access Control** (RBAC, ABAC, MFA)
* **Data Masking & Tokenization**
* **Network Segmentation**

**💥 Real-World Exploit:**

> 🔓 *Misconfigured AWS S3 bucket leaking customer financial data.*

---

### 2. 📊 Integrity

> “Trust that the data hasn’t been tampered with.”

**Breach Risk:** Altered records, corrupted files, or unauthorized modifications.

**🔐 Key Safeguards:**

* **Hashing** (SHA-256, SHA-3)
* **Digital Signatures**
* **Secure Audit Logs**
* **Input Validation & Injection Protection**

**💥 Real-World Exploit:**

> 🧾 *Tampered invoices in a payment system via SQL injection.*

---

### 3. 🟢 Availability

> “The system is up when you need it.”

**Breach Risk:** System downtime, denial-of-service, or resource exhaustion.

**🛡️ Key Safeguards:**

* DDoS Protection (Cloudflare, AWS Shield)
* Load Balancing and Failover Clusters
* Regular Backups & Disaster Recovery Plans
* Real-Time Monitoring & Alerts

**💥 Real-World Exploit:**

> 🌐 *Ransomware shuts down hospital systems during an emergency.*

---

## 🧮 CVSS — Quantifying the Risk

The **Common Vulnerability Scoring System (CVSS)** provides an open framework for rating the **severity of software vulnerabilities**.

### 🧩 CVSS Breakdown:

| Category          | Description                                                |
| ----------------- | ---------------------------------------------------------- |
| **Base Score**    | Intrinsic qualities: attack vector, complexity, privileges |
| **Temporal**      | Exploit maturity, fix availability                         |
| **Environmental** | Contextual importance in the target’s environment          |

📊 **Score Range**:

* 0.0–3.9: Low
* 4.0–6.9: Medium
* 7.0–8.9: High
* 9.0–10.0: Critical

➡️ [Try the CVSS v3.1 Calculator](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator)

---

## ⚠️ Real-World CVEs Mapped to CIA Impact

### 1. **CVE-2021-44228 – Log4Shell**

Remote Code Execution in Apache Log4j via JNDI

| CIA Impact      | ✓ Affects All                      |
| --------------- | ---------------------------------- |
| Confidentiality | Full internal data exposure        |
| Integrity       | Remote modification of config/code |
| Availability    | System crash, ransomware potential |

📈 **CVSS:** 10.0 (Critical)
📌 One of the most widespread exploits of the decade.

---

### 2. **CVE-2017-0144 – EternalBlue**

SMBv1 flaw exploited by WannaCry ransomware.

| CIA Impact      | ✓ Affects All       |
| --------------- | ------------------- |
| Confidentiality | Data theft          |
| Integrity       | Data encryption     |
| Availability    | Full system lockout |

📈 **CVSS:** 9.8 (Critical)
📌 Disrupted healthcare, finance, and logistics globally.

---

### 3. **CVE-2021-41773 – Apache Path Traversal**

Path traversal → file leak & possible RCE.

| CIA Impact                            |
| ------------------------------------- |
| Confidentiality – config file leakage |
| Integrity – web shell upload          |
| Availability – crash/hijack service   |

📈 **CVSS:** 9.8 (Critical)
📌 Caused by a misconfigured web server in production.

---

### 4. **CVE-2022-0847 – Dirty Pipe**

Linux kernel privilege escalation.

| CIA Impact                            |
| ------------------------------------- |
| Confidentiality – read root files     |
| Integrity – overwrite protected files |
| Availability – possible kernel panic  |

📈 **CVSS:** 7.8 (High)
📌 Exploited in many Linux containers and local privilege attacks.

---

## 🔎 CIA Impact Matrix (Attack Mapping)

| Attack Type        | Confidentiality | Integrity | Availability |
| ------------------ | --------------- | --------- | ------------ |
| **SQL Injection**  | ✅               | ✅         | ❌            |
| **DDoS Attack**    | ❌               | ❌         | ✅            |
| **Ransomware**     | ✅               | ✅         | ✅            |
| **Insider Threat** | ✅               | ✅         | ✅            |

---

## 🧠 Final Thoughts

The **CIA Triad is more than a model — it's your cybersecurity compass**. Use it to:

✅ Evaluate the **blast radius** of each vulnerability
✅ Design layered defenses
✅ Communicate risk clearly to stakeholders

---
