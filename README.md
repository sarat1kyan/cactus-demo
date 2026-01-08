<div align="center">

# 🌵 CACTUS - Enterprise Security Platform / Hardened by Design


### *AI-Powered Threat Detection • Digital Forensics • Compliance • Network Intelligence*


**Enterprise-Grade Security Automation | AI/ML Detection | Forensics | Compliance | Real-Time Network Intelligence**

[![License](https://img.shields.io/badge/License-Private-red.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-success.svg)](https://github.com)
[![Security](https://img.shields.io/badge/Security-Hardened-critical.svg)](SECURITY.md)
[![Compliance](https://img.shields.io/badge/Compliance-NIST%20%7C%20CIS%20%7C%20ISO-orange.svg)](DEPLOYMENT.md)

**⚡ Your Cybersecurity Command Center – From Threat Intel to Remediation.**

</div>

---

## 🧠 **Core Capabilities**

| Category                      | Key Features                                                           |
| ----------------------------- | ---------------------------------------------------------------------- |
| 🤖 **AI/ML Threat Detection** | Isolation Forest • Autoencoder • XGBoost • BERT (MITRE ATT&CK Mapping) |
| 🔍 **Digital Forensics**      | Volatility3 • YARA • PCAP Analysis • File & Memory Forensics           |
| 📜 **Compliance Engine**      | NIST • CIS • ISO 27001 • STIG • Continuous Monitoring                  |
| 🛡️ **Self-Healing Defense**  | File Integrity Monitoring • Process Protection • Auto-Remediation      |
| 🌐 **Network Intelligence**   | Topology Mapping • Node Discovery • Flow Monitoring • Graph Engine     |
| 🔥 **Firewall Governance**    | Cisco • Palo Alto • Fortinet • Rule Audits & Risk Scoring              |
| 🧬 **Agent Management**       | Linux • Windows • macOS • Remote Commands • Telemetry • Heartbeat      |
| 🎨 **Premium Dashboard**      | NVIDIA-style UI • Live WebSockets • Dark Mode • Real-Time Insights     |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────┐
│                Management Console (UI)                  │
└───────────────────────────┬─────────────────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌───────▼───────┐  ┌────────▼─────────┐
│  FastAPI Core  │  │  API Gateway  │  │  WebSocket API   │
│   (REST API)   │  │  (Rate Limit) │  │  (Real-time)     │
└───────┬────────┘  └───────┬───────┘  └────────┬─────────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌───────▼───────┐  ┌────────▼─────────┐
│  AI Engine     │  │  Forensics    │  │  Defense System  │
│  (ML Models)   │  │  Engine       │  │  (Self-Healing)  │
└───────┬────────┘  └───────┬───────┘  └────────┬─────────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
                            │
┌─────────────────────────────┐
│       AI Model Router       │  ← Takes input + routes to correct model
└───────────────────────────┬─┘
                            │
      ┌─────────────────────┼───────────────────────────┐
      │                     │                           │
┌─────▼──────┐          ┌───▼────────┐          ┌───────▼───────┐
│ Anomaly    │          │ Classifier │          │ NLP / ATT&CK  │
│ Detection  │          │ (XGBoost)  │          │ Mapping (BERT)│
│ (IF / AE)  │          └────────────┘          └───────────────┘
└────────────┘                  │                      │
       │                        └────────────┬─────────┘
       │                                     │
┌──────▼─────────────────────────────────────▼────────┐
│              Threat Scoring Engine (NN)             │
└───────────────────────────┼─────────────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌───────▼───────┐  ┌────────▼─────────┐
│  PostgreSQL    │  │  Redis        │  │  File Storage    │
│  (Database)    │  │  (Cache)      │  │  (Artifacts)     │
└────────────────┘  └───────────────┘  └──────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌───────▼───────┐  ┌────────▼────────┐
│  Endpoint      │  │  Network      │  │  Compliance     │
│  Agents        │  │  Topology     │  │  Engine         │
└────────────────┘  └───────────────┘  └─────────────────┘
```
See [ARCHITECTURE.md](ARCHITECTURE.md) for detailed diagrams and component descriptions.
---
</div>

---

## 🎯 Overview

**CACTUS** is a production-ready, enterprise-grade security platform that unifies security automation, AI/ML-powered threat detection, digital forensics, compliance management, network intelligence, firewall governance, data loss prevention (DLP), and file integrity monitoring (FIM) into a single, cohesive system.

CACTUS provides comprehensive security visibility, automated threat response, continuous compliance monitoring, and advanced analytics through a modern, intuitive dashboard interface.

### Core Capabilities

- 🤖 **AI/ML Threat Detection** - Isolation Forest, Autoencoder, XGBoost, BERT-based MITRE ATT&CK mapping
- 🔍 **Digital Forensics** - Volatility3 integration, YARA scanning, PCAP analysis, file analysis
- ✅ **Compliance Engine** - NIST 800-53, CIS Benchmarks, ISO 27001, STIG continuous monitoring
- 🛡️ **Self-Healing Defense** - File integrity monitoring, process protection, automated remediation
- 🌐 **Network Intelligence** - Real-time topology mapping, node discovery, flow monitoring
- 🔥 **Firewall Governance** - Multi-vendor rule analysis
- 🔒 **Data Loss Prevention (DLP)** - Real-time data protection, policy enforcement, incident management
- 📁 **File Integrity Monitoring (FIM)** - Real-time file change detection, baseline management
- 📡 **Agent Management** - Cross-platform agents (Windows, Linux, macOS)
- 🎨 **Premium Dashboard** - Modern UI with real-time WebSocket updates
- 🔐 **Advanced Authentication** - JWT with 2FA (TOTP), role-based access control

---

## 💻 Technical Requirements

### Minimum System Requirements

**For Testing:**
- **CPU**: 2 cores (4 recommended)
- **RAM**: 8 GB (16 GB recommended)
- **Storage**: 50 GB free space (SSD recommended)
- **Network**: 100 Mbps connection
- **OS**: Linux (Debian 12+, RHEL 8+), Windows 10/11, macOS 11+

**For Production (Small Deployment - < 100 agents):**
- **CPU**: 4 cores (8 recommended)
- **RAM**: 16 GB (32 GB recommended)
- **Storage**: 200 GB free space (SSD required)
- **Network**: 1 Gbps connection
- **OS**: Linux (Debian 12+, RHEL 8+)

**For Production (Medium Deployment - 100-500 agents):**
- **CPU**: 8 cores (16 recommended)
- **RAM**: 32 GB (64 GB recommended)
- **Storage**: 500 GB free space (NVMe SSD recommended)
- **Network**: 10 Gbps connection
- **OS**: Linux (Debian 12+, RHEL 8+)

**For Production (Large Deployment - 500+ agents):**
- **CPU**: 16+ cores
- **RAM**: 64 GB+ (128 GB recommended)
- **Storage**: 1 TB+ free space (NVMe SSD required)
- **Network**: 10 Gbps+ connection
- **OS**: Linux (Debian 12+, RHEL 8+)

### Software Requirements

- **Python**: 3.11 or higher (3.13+ recommended)
- **Node.js**: 18.x or higher (20.x LTS recommended)
- **PostgreSQL**: 14.x or higher (15.x recommended)
- **Redis**: 7.x or higher
- **Docker**: 20.10+ (for containerized deployment)
- **Docker Compose**: 2.0+ (for containerized deployment)

### Database Requirements

- **PostgreSQL**: 
  - Minimum: 2 GB RAM, 20 GB storage
  - Recommended: 4 GB+ RAM, 100 GB+ storage
  - Connection pool: 10-50 connections (configurable)
  
- **Redis**:
  - Minimum: 512 MB RAM
  - Recommended: 2 GB+ RAM
  - Persistence: AOF + RDB recommended for production

### Network Requirements

- **Ports Required**:
  - `3000`: Frontend (HTTP/HTTPS)
  - `8000`: Backend API (HTTP/HTTPS)
  - `5432`: PostgreSQL (internal, restrict access)
  - `6379`: Redis (internal, restrict access)
  - `9090`: Prometheus metrics (optional, internal)

- **Bandwidth**:
  - Agent telemetry: ~1-5 KB per agent per minute
  - WebSocket updates: ~10-50 KB per connected client
  - File uploads (forensics, firewall configs): Variable

### Resource Usage Estimates

**Per Agent (Average):**
- Network: 1-5 KB/min
- Database: ~100-500 rows/day
- Storage: ~1-10 MB/month (logs, events)

**Backend Service:**
- Base memory: ~500 MB
- Per concurrent request: ~10-50 MB
- ML model loading: +200-500 MB per model

**Frontend Service:**
- Base memory: ~200-300 MB
- Per connected user: ~10-20 MB

---


## 🎨 Features

### AI/ML Threat Detection
- **Anomaly Detection**: Isolation Forest + Autoencoder for behavioral anomaly detection
- **Threat Classification**: XGBoost-based multi-class threat classification
- **MITRE ATT&CK Mapping**: BERT-powered technique mapping and attribution
- **Threat Scoring**: Neural network-based threat scoring (0-1 scale)
- **Model Router**: Intelligent routing to appropriate ML models

### Digital Forensics
- **Memory Analysis**: Volatility3 integration for memory forensics
- **YARA Scanning**: Custom YARA rule scanning for malware detection
- **Network Analysis**: PCAP file analysis and network traffic inspection
- **File Analysis**: Static analysis of PE, ELF, and Mach-O binaries
- **Incident Timeline**: Automated timeline reconstruction

### Compliance Engine
- **Continuous Monitoring**: Real-time compliance checking
- **NIST 800-53**: Information security controls
- **CIS Benchmarks**: Security configuration guidelines
- **ISO 27001**: Information security management
- **STIG Compliance**: Security Technical Implementation Guides
- **Multi-OS Support**: Windows, Linux, macOS compliance checks

### Data Loss Prevention (DLP)
- **Real-time Monitoring**: File, network, clipboard, email, USB monitoring
- **Policy Management**: Flexible policy creation and enforcement
- **Data Type Detection**: PII, PHI, PCI, credentials, financial data, IP, confidential
- **Action Enforcement**: Block, alert, log, quarantine, encrypt
- **Incident Management**: Comprehensive incident tracking and investigation
- **Scanning**: Scheduled and on-demand sensitive data scans

### File Integrity Monitoring (FIM)
- **Real-time Monitoring**: File system change detection
- **Baseline Management**: Automated baseline creation and comparison
- **Event Types**: Created, modified, deleted, renamed, permissions, ownership, attributes
- **Hash Verification**: SHA256 file hash computation and verification
- **Policy-based**: Configurable monitoring policies per path
- **Alerting**: Configurable severity levels and alerting

### Firewall Governance
- **Multi-vendor Support**: Cisco ASA/Firepower, Palo Alto, Fortinet
- **Rule Analysis**: Any-any detection, shadowed rules, duplicates, overlapping, risk scoring
- **Compliance Checking**: NIST, CIS, ISO 27001, PCI-DSS compliance
- **Remediation**: Automated lockdown plan generation
- **API Integration**: Direct integration with firewall management APIs

### Network Intelligence
- **Topology Mapping**: Real-time network topology visualization
- **Node Discovery**: Automatic device and service discovery
- **Flow Monitoring**: Network flow analysis and visualization
- **Graph Generation**: Interactive network graph with Cytoscape

### Agent Management
- **Cross-platform**: Windows, Linux, macOS agents
- **Remote Execution**: Secure remote command execution
- **Telemetry Collection**: System metrics, processes, network connections
- **Heartbeat Monitoring**: Real-time agent health monitoring
- **Service Integration**: systemd (Linux), Windows Service, launchd (macOS)

### Self-Healing Defense
- **Automated Remediation**: Automated response to detected threats
- **Process Protection**: Process monitoring and protection
- **File Integrity**: Real-time file integrity monitoring
- **Incident Response**: Automated containment and remediation

---

## 🔧 Configuration

Environment variables are managed through `.env` files. Key configuration areas:

- **Database**: `POSTGRES_HOST`, `POSTGRES_PORT`, `POSTGRES_DB`, `POSTGRES_USER`, `POSTGRES_PASSWORD`
- **Redis**: `REDIS_HOST`, `REDIS_PORT`
- **Security**: `SECRET_KEY`, `JWT_ALGORITHM`, `ACCESS_TOKEN_EXPIRE_MINUTES`
- **API**: `CORS_ORIGINS`, `TRUSTED_HOSTS`, `DEBUG`
- **Firewall APIs**: Vendor-specific API keys and endpoints
- **ML Models**: `ML_MODELS_PATH`

Integration with Vault is available.

---

## 📊 Monitoring

- **Prometheus Metrics**: `http://localhost:8000/metrics`
- **Health Check**: `http://localhost:8000/health`
- **API Documentation**: `http://localhost:8000/docs`
- **WebSocket**: `ws://localhost:8000/ws`

---

## 🔐 Security

CACTUS implements comprehensive security measures:

- **Authentication**: JWT tokens with refresh mechanism
- **2FA**: TOTP-based two-factor authentication
- **Authorization**: Role-based access control (root "In case of force majeure", Admin, Analyst, Viewer)
- **Encryption**: TLS/SSL for all communications
- **Audit Logging**: Comprehensive audit trail
- **Input Validation**: Pydantic models for all inputs
- **Rate Limiting**: Redis-based rate limiting
- **Security Headers**: Comprehensive security headers

See [SECURITY.md](SECURITY.md) for detailed security guidelines.

---

## 📈 Performance

### Benchmarks (Typical Deployment)

- **API Response Time**: < 100ms (p95)
- **Threat Detection**: < 500ms per event
- **Compliance Scan**: 1-5 seconds per host
- **Forensics Analysis**: 10-60 seconds per file
- **Concurrent Users**: 100+ supported
- **Agents Supported**: 1000+ per instance

### Scalability

- **Horizontal Scaling**: Stateless backend, multiple instances
- **Database**: Connection pooling, read replicas
- **Cache**: Redis for session and rate limiting
- **Load Balancing**: NGINX or cloud load balancer

---

## 🗺️ Roadmap

- [ ] Kubernetes operator for automated deployment
- [ ] Additional ML model types
- [ ] Enhanced compliance frameworks
- [ ] Mobile app for iOS/Android
- [ ] SIEM integration
- [ ] Threat intelligence feeds
- [ ] Advanced reporting and analytics

---
