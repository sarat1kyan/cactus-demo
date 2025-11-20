# CACTUS — Security Automation & Forensics Platform  
![Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-private-red)
![Built_with](https://img.shields.io/badge/built%20with-Python-blue)
![Security](https://img.shields.io/badge/focus-security-critical)
![Compliance](https://img.shields.io/badge/compliance-ISO%20%7C%20NIST%20%7C%20CIS-orange)

---

## 🚀 What is CACTUS?

**CACTUS** is an advanced **security automation and compliance platform** designed to **harden, monitor, and investigate** infrastructure in real time.  
It ensures **24/7 compliance**, detects misconfigurations, identifies threats, performs deep forensics, and generates a real-time **infrastructure topology map** — all from a **single console**.

---

## 🔍 Primary Users

| Role | Usage |
|------|------|
| SOC Analysts | Incident response & alert investigation |
| Sysadmins | Hardening & configuration enforcement |
| DevOps / SRE | Infrastructure insights & performance checks |
| Forensic Analysts | Memory / PCAP analysis inside the same tool |
| Enterprise Security Teams | Compliance & risk management |

---

## 💡 Core Vision & Value Proposition

CACTUS exists because **traditional security tools are reactive** — **CACTUS is proactive and continuous.**

| Problem Today | How CACTUS Solves It |
|----------------|-----------------------------|
| Compliance is static. Environments change constantly. | Continuous compliance engine with real-time checks |
| Hardening is manual and inconsistent. | Automated, policy-driven hardening |
| Security tools are fragmented. | Unified compliance, threats & forensics in one console |
| Forensics requires separate tools. | Built-in memory & PCAP forensic analysis pipeline |
| Low infrastructure visibility. | Real-time network topology & agent intelligence |

> **Result:** CACTUS transforms infrastructure from *reactive* to **continuously secured, hardened, and auditable**.

---

## 🧠 Architecture Overview

```
                 ┌────────────────────────────┐
                 │  Management Console (UI)   │
                 └───────────────┬────────────┘
                                 │
      ┌──────────────────────────┼──────────────────────────────┐
      │                          │                              │
┌──────────────┐        ┌───────────────────┐        ┌─────────────────┐
│ Backend Core │◄──────►│ Agents (Endpoints)│◄──────►│ Forensics Engine │
└──────────────┘        └───────────────────┘        └─────────────────┘
       │                          │
       │                          ▼
       │                  Network Topology Service
       │                          │
       ▼                          ▼
 Alerting Engine        Compliance / Hardening Engine
```

---

## 🧪 Features — MVP Scope

| Feature | Description |
|--------|-------------|
| Dashboard | Live stats, alerts, system health |
| Threat Management | File & URL scanner, threat table |
| Forensics | Memory/PCAP upload & investigation |
| Compliance Engine | ISO/NIST/CIS checks & summaries |
| Network Topology | Real-time graph, node health |
| Agents | Commands, sysinfo, terminal output |
| Settings | Security JSON view & config |

---

## 🧭 Roadmap

| Stage | Deliverable |
|------|--------------|
| MVP | Management Console (current focus) |
| Stage 2 | Agent UI |
| Stage 3 | AI anomaly detection & policy builder |
| Stage 4 | Mobile SOC companion app |
| Future | Cloud multi-tenancy & compliance reporting API |

---

## 🎨 UX & Design Guidelines

| Aspect | Expectation |
|--------|-------------|
| Style | Professional enterprise UI — not Hollywood hacker |
| Theme | Dark preferred, but accessible & clean |
| Accessibility | WCAG AA minimum |
| Typography | UI font + monospaced for terminal |
| Responsiveness | Desktop-first, tablet-friendly |

---

## 🧪 Example User Flows

### 🔎 Investigate an Alert  
1. Dashboard → alert → forensic analysis → results & incident options.

### 🚨 Run File Scan  
1. Threats → upload file → progress → results → quarantine or allowlist.

### 🖥 Agent Command Flow  
1. Agents → sysinfo/processes/ping → result in terminal modal.

---

## 📡 API Endpoints (For Design Reference)

| Endpoint | Purpose |
|----------|---------|
| `/api/dashboard/overview` | Dashboard statistics |
| `/api/dashboard/alerts` | Alerts list |
| `/api/threats/detected` | Threats overview |
| `/api/agents` | Registered endpoints |
| `/api/network/topology` | Infrastructure graph |
| `/api/settings/security` | Compliance/security JSON |
| `/api/auth/login` | Authentication |

---

## 🧾 Summary

**CACTUS = One platform for everything enterprise security teams actually do**  
✔ Hardening  
✔ Compliance  
✔ Forensics  
✔ Threat detection  
✔ Topology intelligence  
✔ Agent-level control  

> **Not reactive. Not static. Not fragmented.**  
> **Secure + Investigate + Comply — Continuously.**

---

### 🔗 Project Status
> MVP Management Console currently in progress. All UI requirements available in `demo.html`  
> Next phase → Agent UI + extended policy builder.

---

## 📄 License
Private – All rights reserved.

---

**Let’s build the future of security.**
