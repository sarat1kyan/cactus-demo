# 🌵 **CACTUS – Security Platform Designer Brief**

## 🚀 1. **Platform Overview**

**CACTUS** is an **enterprise security platform** that unifies:

✔️ Continuous Compliance
✔️ Automated Hardening
✔️ Forensic Analysis
✔️ Device Management
✔️ Network Visibility
✔️ Autonomous Remediation

**Primary Users**

| Role                      | Purpose                            |
| ------------------------- | ---------------------------------- |
| SOC Analysts (Tier 2–3)   | Incident triage & investigation    |
| IT Administrators         | Device control & enforcement       |
| DevSecOps / SRE           | Stability & configuration security |
| Forensic Analysts         | Evidence analysis & threat tracing |
| Enterprise Security Teams | Governance & compliance            |

---

### 🧠 **Platform Capabilities**

**One platform** – multiple integrated engines:

| Feature                 | Description                                           |
| ----------------------- | ----------------------------------------------------- |
| **Security Compliance** | Evaluates CIS / ISO / NIST or mixed custom frameworks |
| **Device Management**   | 50+ built-in commands & custom script execution       |
| **Forensic Analytics**  | Upload memory/pcap files + AI/MITRE-based analysis    |
| **Network Management**  | Live topology + device relationship control           |
| **Threat Management**   | VirusTotal integration + MITRE ATT&CK mapping         |
| **Log Management**      | Collects & analyzes all logs with AI-rule creation    |

---

## 💡 2. **Core Platform Values**

### 🔁 1. Continuous Compliance

* Real-time evaluation (not static audits)
* CIS/ISO/NIST/custom frameworks
* Compliance score recalculates continuously

### 🧩 2. Dynamic Compliance Builder

* **3-layer tree:** Framework → Section → Control
* Users can **mix frameworks** to build their own
* Saved version becomes **enforced baseline**

### 🛡️ 3. Automated Hardening

* Auto-applies secure baselines
* Fixes misconfigurations instantly
* Reduces human interaction

### ♻️ 4. Unified Security Operations

> All tools in **one single UI** – no fragmentation.

### 🔍 5. Built-in Forensics

* Upload memory dumps & PCAP
* Agents can collect data remotely
* MITRE ATT&CK threat mapping

### 🌐 6. Infrastructure Visibility

* Real-time network topology
* Device relationships & vulnerabilities
* Security graph & contextual awareness

### 🖥️ 7. Device Management

* Status, actions, rule updates
* Built-in actions (reboot, isolate, refresh)
* Execute custom scripts (CMD/Powershell)

### 🧠 8. Self-Healing System

* Repairs failed/insecure configs
* Restores MFA, closes ports, enforces baselines

### 🤖 9. Automated Remediation Playbooks

* Lightweight SOAR triggers
* Example: “If suspicious process → isolate + scan”

### 🧬 10. Security Knowledge Graph

> Connects **devices, vulnerabilities, users, logs, alerts, controls, topology & artifacts**.

---

## 🧱 3. **Feature Pillars (Designer-Friendly)**

| # | Pillar                     | Key Features                                 |
| - | -------------------------- | -------------------------------------------- |
| 1 | **Compliance & Hardening** | Real-time score, auto-fixes, dynamic builder |
| 2 | **Device & Agent Mgmt.**   | Health status, actions, agent view           |
| 3 | **Digital Forensics**      | Upload & analyze memory/pcap + MITRE mapping |
| 4 | **Network Topology**       | Live map, relationships, device status       |
| 5 | **Log Management**         | AI rule creation, anomaly detection          |
| 6 | **Autonomous Operations**  | Playbooks, auto-remediation, self-healing    |

---

## 📸 4. **MVP Screen List**

1. **Dashboard**
2. Digital Forensics
3. Compliance Overview
4. Dynamic Compliance Builder
5. Network Topology
6. Log Management
7. Agents
8. Device Management
9. Settings
10. **Shared Components**

* Modals
* Output Viewer
* Tables

---

## ⚙️ 5. **Functional Behavior**

| Behavior               | Notes                               |
| ---------------------- | ----------------------------------- |
| Async actions          | Always show state                   |
| Status flow            | queued → running → success → failed |
| High-frequency updates | Backend stream/log updates          |
| Multi-step uploads     | Forensics & logs                    |
| Dynamic visuals        | Topology, compliance score          |
| Real-time feedback     | Needed for all operations           |

---

## 🧭 6. **Key User Journeys**

### 🧑‍💻 **1. Login & Dashboard**

* Login (MFA protected) → Dashboard
* Dashboard shows:
  ✔ Compliance score (live)
  ✔ Agent health
  ✔ Active alerts
  ✔ Forensic activity
  ✔ Network snapshot
  ✔ AI recommendations

> 🟡 **Example:** Compliance dropped from **94% → 81%**

---

### 📉 **2. Detecting the Problem – Compliance View**

Shows:

* Active frameworks (ISO / NIST / CIS)
* Failed controls
* Button: **See Affected Devices**

---

### 🛠 **3. Dynamic Compliance Builder**

User builds their own compliance baseline:

```
ISO 27001 → +3 new controls  
CIS Windows → -1 outdated control  
```

System re-evaluates compliance automatically.

---

### 💻 **4. Agents – Health Check**

| Total Agents | Online | Unhealthy |
| ------------ | ------ | --------- |
| 142          | 142    | 3         |

User clicks unhealthy → sees:

* High CPU
* Missing log forwarding
  Action taken: **Refresh Config + Update Ruleset** → becomes healthy.

---

### 📊 **5. Full Compliance Scan**

System shows:

* 142 queued
* 42 scanning
* Live results
* Compliance: **81% → 86%**

---

### 🔧 **6. Auto-Hardening**

User picks:
✔ Enforce TLS
✔ Fix password policy
✔ Close RDP ports

> **Modes**: Immediate | Batch rollout | Rollback possible

---

### 📜 **7. Log Management**

* Search for RDP logs
* Detect suspicious attempts
* User creates AI rule:

  ```
  Alert if RDP logins > 3 per minute
  ```

---

### 🌐 **8. Network Topology**

* Shows 6 exposed devices
* After hardening → ports visually close
* Suspicious lateral movement disappears

---

### 🧪 **9. Threat Management**

* CACTUS checks VirusTotal
* MITRE match: **T1110 (Brute Force)**
* User triggers forensic collection

---

### 🧠 **10. Digital Forensics**

Memory dump auto-analyzed:
✔ Processes
✔ Registry keys
✔ Network connections
✔ Malware signatures
MITRE reports credential access attempt.

---

### 🧹 **11. Device Cleanup**

Action: **Apply Cleanup Script**
→ Kill processes → Reset password → Reboot → Done.

---

### 🤖 **12. Playbook Creation**

```
IF RDP threat → isolate device + collect logs + capture memory
```

---

### 🟢 **13. Final System State**

| Item       | Status      |
| ---------- | ----------- |
| Compliance | **97%**     |
| Alerts     | 0           |
| Agents     | All Healthy |
| Forensics  | Complete    |

---

### 📤 **14. Export / Reporting**

User exports:

* Compliance Report
* Forensic Investigation
* Logs & Health Summary
* Hardening Execution Data

**→ Ready for manager / auditor.**

---

## 🔌 7. **API Groups**

```
- Dashboard
- Alerts
- Forensics
- Compliance
- Agents
- Topology
- FIM / DLP
- Login
```

---

## 🧷 8. **Non-Functional Requirements**

✔ High-density UI
✔ Works under heavy load
✔ Real-time feedback
✔ Fast triage
✔ Clear section separation

---

## 🔭 9. **Future Modules**

| Feature                   | Status |
| ------------------------- | ------ |
| File Integrity Monitoring | Coming |
| Data Loss Prevention      | Coming |
| Agent UI                  | Coming |

---

## 🧠 Final Designer Notes

**CACTUS is not a monitoring tool — it is a decision-making engine.**
It must feel:
✔ Fast ⚡
✔ Reliable 🛡
✔ Professional 🧠
✔ AI-assisted 🤖
✔ Enterprise-grade 🏢

---
