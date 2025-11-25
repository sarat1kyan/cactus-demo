<div align="center">

# 🛡️ CACTUS
## Elite Forensics & Security Intelligence Platform

**Production-Ready Security Automation Platform for Continuous Threat Detection, Compliance, and Forensics**

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)](https://fastapi.tiangolo.com/)
[![License](https://img.shields.io/badge/License-Private-red.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-success.svg)](https://github.com)
[![Security](https://img.shields.io/badge/Security-Hardened-critical.svg)](SECURITY.md)
[![Compliance](https://img.shields.io/badge/Compliance-NIST%20%7C%20CIS%20%7C%20ISO-orange.svg)](DEPLOYMENT.md)

[Features](#-features) • [Quick Start](#-quick-start) • [Installation](#-installation) • [Documentation](#-documentation) • [Architecture](#-architecture)

</div>

---

## 🌟 What is CACTUS?

**CACTUS** (formerly CACTUS) is an **enterprise-grade security automation and forensics platform** that transforms your security operations from reactive to **proactively continuous**. 

Unlike traditional security tools that operate in silos, CACTUS unifies **threat detection**, **compliance monitoring**, **digital forensics**, and **infrastructure hardening** into a single, intelligent platform.

### 🎯 Core Value Proposition

| **Traditional Security** | **CACTUS Solution** |
|-------------------------|---------------------|
| ❌ Static compliance checks | ✅ Continuous real-time compliance engine |
| ❌ Manual, inconsistent hardening | ✅ Automated, policy-driven hardening |
| ❌ Fragmented security tools | ✅ Unified console for all security operations |
| ❌ Separate forensics tools | ✅ Built-in memory & PCAP analysis pipeline |
| ❌ Limited infrastructure visibility | ✅ Real-time network topology & agent intelligence |
| ❌ Reactive threat response | ✅ Proactive AI-powered threat detection |

> **Result:** Transform your infrastructure from *reactive* to **continuously secured, hardened, and auditable**.

---

## ✨ Features

### 🔐 Security & Authentication
- ✅ **Production-Ready Authentication** - Bcrypt password hashing, JWT tokens, role-based access control
- ✅ **Security Hardening** - Rate limiting, CORS protection, security headers, input validation
- ✅ **Audit Logging** - Comprehensive security event logging and request tracking
- ✅ **Secret Management** - Environment-based configuration with validation

### 🤖 AI-Powered Threat Detection
- ✅ **Machine Learning Engine** - Isolation Forest anomaly detection, behavior classification
- ✅ **MITRE ATT&CK Mapping** - Automatic technique identification and mapping
- ✅ **Threat Scoring** - Neural network-based threat risk assessment
- ✅ **Real-time Analysis** - Continuous behavioral pattern analysis

### 🔍 Digital Forensics
- ✅ **Memory Analysis** - Volatility3 integration for memory dump analysis
- ✅ **Network Forensics** - PCAP file analysis and network traffic investigation
- ✅ **File Analysis** - YARA rules, PE file analysis, malware detection
- ✅ **IOC Management** - Indicator of Compromise tracking and correlation

### 📊 Compliance & Hardening
- ✅ **Multi-Framework Support** - NIST, CIS Controls, STIG, ISO 27001
- ✅ **Continuous Compliance** - Real-time compliance checking and reporting
- ✅ **Automated Hardening** - Policy-driven system hardening
- ✅ **Compliance Scoring** - Quantitative compliance metrics

### 🌐 Network Intelligence
- ✅ **Topology Mapping** - Real-time network graph visualization
- ✅ **Node Discovery** - Automatic endpoint and device detection
- ✅ **Connection Tracking** - Network flow analysis and monitoring
- ✅ **Health Monitoring** - Node status and performance tracking

### 🤖 Agent Management
- ✅ **Cross-Platform Agents** - Windows, Linux, macOS support
- ✅ **Remote Command Execution** - Secure agent command interface
- ✅ **Telemetry Collection** - System metrics and event collection
- ✅ **Heartbeat Monitoring** - Agent health and connectivity tracking

### 🛡️ Defense System
- ✅ **Self-Healing Capabilities** - Automated threat response and system restoration
- ✅ **Process Protection** - Critical process monitoring and protection
- ✅ **File System Monitoring** - Real-time file integrity monitoring
- ✅ **Network Protection** - Connection blocking and rate limiting

### 📈 Monitoring & Analytics
- ✅ **Real-Time Dashboard** - Live system health and threat statistics
- ✅ **Alert Management** - Security alert triage and investigation
- ✅ **Threat Timeline** - Chronological threat event visualization
- ✅ **Prometheus Metrics** - Comprehensive metrics for monitoring

---

## 🚀 Quick Start

### Prerequisites
- **Python 3.9+**
- **PostgreSQL 13+** (or Docker)
- **Redis 6+** (optional, for caching)

### Installation

#### 🐧 Linux / macOS
```bash
# Clone the repository
git clone https://github.com/your-org/CACTUS.git
cd CACTUS

# Run installation script
chmod +x install.sh
./install.sh
```

#### 🪟 Windows
```powershell
# Clone the repository
git clone https://github.com/your-org/CACTUS.git
cd CACTUS

# Run installation script
.\install.ps1
```

#### 🐳 Docker (Recommended)
```bash
# Copy environment file
cp env.example .env
# Edit .env with your settings

# Start all services
docker compose up -d

# Initialize database
docker compose exec CACTUS alembic upgrade head

# Create admin user
docker compose exec CACTUS python scripts/create_admin_user.py
```

### First Run

1. **Activate virtual environment:**
   ```bash
   # Linux/macOS
   source venv/bin/activate
   
   # Windows
   .\venv\Scripts\Activate.ps1
   ```

2. **Start the application:**
   ```bash
   python -m CACTUS.main
   ```

3. **Access the platform:**
   - Web Interface: http://localhost:8000
   - API Documentation: http://localhost:8000/api/docs
   - Health Check: http://localhost:8000/health

4. **Login:**
   - Default credentials (change immediately!):
     - Username: `admin`
     - Password: `admin` (or the password you set during installation)

---

## 📖 Documentation

| Document | Description |
|----------|-------------|
| [📘 Installation Guide](INSTALLATION.md) | Detailed installation instructions for all platforms |
| [🚀 Deployment Guide](DEPLOYMENT.md) | Production deployment, scaling, and maintenance |
| [✅ Production Checklist](PRODUCTION_CHECKLIST.md) | Pre-deployment security and configuration checklist |
| [📊 Improvements Summary](IMPROVEMENTS_SUMMARY.md) | Complete list of production-ready improvements |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                    Management Console (UI)                      │
│              http://localhost:8000                              │
└───────────────────────────┬─────────────────────────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌──────▼───────┐  ┌───────▼──────────┐
│  FastAPI Core  │  │  API Gateway  │  │  WebSocket API   │
│   (REST API)   │  │  (Rate Limit) │  │  (Real-time)     │
└───────┬────────┘  └──────┬────────┘  └───────┬──────────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌──────▼───────┐  ┌───────▼──────────┐
│  AI Engine     │  │  Forensics    │  │  Defense System  │
│  (ML Models)   │  │  Engine       │  │  (Self-Healing)  │
└───────┬────────┘  └──────┬────────┘  └───────┬──────────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌──────▼───────┐  ┌───────▼──────────┐
│  PostgreSQL    │  │  Redis        │  │  File Storage    │
│  (Database)    │  │  (Cache)       │  │  (Artifacts)     │
└────────────────┘  └───────────────┘  └──────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
┌───────▼────────┐  ┌──────▼───────┐  ┌───────▼──────────┐
│  Endpoint      │  │  Network      │  │  Compliance     │
│  Agents        │  │  Topology     │  │  Engine         │
└────────────────┘  └───────────────┘  └──────────────────┘
```

### Technology Stack

- **Backend Framework:** FastAPI 0.104+
- **Database:** PostgreSQL 13+ with asyncpg
- **Cache:** Redis 6+
- **AI/ML:** TensorFlow, PyTorch, scikit-learn
- **Forensics:** Volatility3, YARA, Scapy
- **Monitoring:** Prometheus, Grafana
- **Containerization:** Docker, Docker Compose

---

## 🔒 Security Features

### Production-Ready Security

✅ **Authentication & Authorization**
- Bcrypt password hashing with salt
- JWT token-based authentication
- Role-based access control (Admin, Analyst, Viewer)
- Secure session management

✅ **API Security**
- Rate limiting (configurable per endpoint)
- CORS protection with whitelist
- Trusted host validation
- Input validation and sanitization
- SQL injection prevention (SQLAlchemy ORM)

✅ **Security Headers**
- Content Security Policy (CSP)
- X-Frame-Options
- X-Content-Type-Options
- Strict-Transport-Security
- X-XSS-Protection

✅ **Audit & Logging**
- Security event logging
- Request/response logging
- Failed login attempt tracking
- Audit trail for all security events

---

## 🎯 Use Cases

### 🏢 Enterprise Security Teams
- **Continuous Compliance Monitoring** - Real-time NIST/CIS/ISO compliance checking
- **Threat Detection & Response** - AI-powered threat identification and automated response
- **Security Auditing** - Comprehensive audit logs and compliance reporting

### 🔍 SOC Analysts
- **Incident Investigation** - Integrated forensics tools for rapid analysis
- **Alert Triage** - Centralized alert management and prioritization
- **Threat Hunting** - Proactive threat detection with MITRE ATT&CK mapping

### 🛠️ System Administrators
- **Infrastructure Hardening** - Automated security configuration enforcement
- **Network Visibility** - Real-time topology mapping and health monitoring
- **Endpoint Management** - Remote agent control and monitoring

### 🔬 Forensic Analysts
- **Memory Analysis** - Volatility3 integration for memory dump investigation
- **Network Forensics** - PCAP analysis and traffic reconstruction
- **Malware Analysis** - YARA rules and behavioral analysis

---

## 📡 API Endpoints

### Authentication
- `POST /api/auth/login` - User authentication
- `GET /api/auth/me` - Get current user info
- `POST /api/auth/logout` - User logout

### Dashboard
- `GET /api/dashboard/overview` - System overview and statistics
- `GET /api/dashboard/alerts` - Recent security alerts
- `GET /api/dashboard/metrics` - System metrics

### Threats
- `GET /api/threats/detected` - List detected threats
- `POST /api/threats/scan` - Scan file or URL
- `GET /api/threats/{id}` - Get threat details

### Forensics
- `POST /api/forensics/analyze` - Upload and analyze forensic artifact
- `GET /api/forensics/{id}` - Get analysis results
- `GET /api/forensics` - List all analyses

### Compliance
- `GET /api/compliance/status` - Current compliance status
- `GET /api/compliance/checks` - List compliance checks
- `POST /api/compliance/run` - Run compliance check

### Network
- `GET /api/network/topology` - Network topology graph
- `GET /api/network/nodes` - List network nodes
- `GET /api/network/connections` - Network connections

### Agents
- `GET /api/agents` - List registered agents
- `POST /api/agents/{id}/command` - Execute command on agent
- `GET /api/agents/{id}/status` - Get agent status

**Full API Documentation:** http://localhost:8000/api/docs

---

## 🧪 Development

### Setup Development Environment

```bash
# Clone repository
git clone https://github.com/your-org/CACTUS.git
cd CACTUS

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: .\venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt

# Install development dependencies
pip install pytest pytest-asyncio black flake8 mypy

# Setup pre-commit hooks
pre-commit install
```

### Running Tests

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=CACTUS --cov-report=html

# Run specific test file
pytest tests/test_auth.py
```

### Code Quality

```bash
# Format code
black CACTUS/

# Lint code
flake8 CACTUS/

# Type checking
mypy CACTUS/
```

---

## 🚢 Deployment

### Production Deployment Options

1. **Docker Compose** (Recommended for small to medium deployments)
   ```bash
   docker compose up -d
   ```

2. **Kubernetes** (For large-scale deployments)
   - See [DEPLOYMENT.md](DEPLOYMENT.md) for Kubernetes manifests

3. **Manual Installation** (For custom configurations)
   - Follow [INSTALLATION.md](INSTALLATION.md) guide

### Health Checks

- **Liveness:** `GET /health/live`
- **Readiness:** `GET /health/ready`
- **Basic Health:** `GET /health`

### Monitoring

- **Prometheus Metrics:** `GET /metrics`
- **Grafana Dashboards:** Pre-configured dashboards available
- **Log Aggregation:** Structured JSON logging

---

## 📊 Production-Ready Features

### ✅ What Makes CACTUS Production-Ready?

- **🔐 Enterprise Security** - Production-grade authentication, authorization, and encryption
- **📈 Scalability** - Async architecture, connection pooling, horizontal scaling support
- **🛡️ Reliability** - Comprehensive error handling, graceful shutdown, health checks
- **📝 Observability** - Structured logging, metrics, distributed tracing support
- **🔧 Maintainability** - Database migrations, configuration management, documentation
- **⚡ Performance** - Optimized queries, caching, async operations
- **🧪 Testability** - Test suite, CI/CD ready, code quality tools

See [IMPROVEMENTS_SUMMARY.md](IMPROVEMENTS_SUMMARY.md) for complete details.

---

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 style guide
- Write tests for new features
- Update documentation
- Ensure all tests pass
- Run code quality checks

---

## 📋 Roadmap

### ✅ Completed (v1.0)
- [x] Production-ready authentication and authorization
- [x] Database models and migrations
- [x] Security hardening and rate limiting
- [x] AI-powered threat detection
- [x] Forensics engine integration
- [x] Compliance engine
- [x] Network topology mapping
- [x] Agent management system
- [x] Installation scripts
- [x] Comprehensive documentation

### 🚧 In Progress (v1.1)
- [ ] Enhanced UI/UX
- [ ] Mobile SOC companion app
- [ ] Advanced policy builder
- [ ] Cloud multi-tenancy

### 🔮 Planned (v2.0)
- [ ] Machine learning model training pipeline
- [ ] Advanced threat intelligence integration
- [ ] Compliance reporting API
- [ ] SIEM integration
- [ ] SOAR capabilities

---

## 📄 License

**Private** – All rights reserved.

This software is proprietary and confidential. Unauthorized copying, distribution, or use is strictly prohibited.

---

## 🙏 Acknowledgments

- **FastAPI** - Modern, fast web framework
- **Volatility3** - Memory forensics framework
- **MITRE ATT&CK** - Threat intelligence framework
- **PostgreSQL** - Robust database system
- **All Contributors** - Thank you for your support!

---

## 📞 Support

- **Documentation:** [INSTALLATION.md](INSTALLATION.md) | [DEPLOYMENT.md](DEPLOYMENT.md)
- **Issues:** [GitHub Issues](https://github.com/your-org/CACTUS/issues)
- **Security:** security@CACTUS.local

---

<div align="center">

**Built with ❤️ for Security Professionals**

[⭐ Star us on GitHub](https://github.com/your-org/CACTUS) • [📖 Documentation](INSTALLATION.md) • [🚀 Get Started](#-quick-start)

---

**CACTUS** - *Secure. Investigate. Comply. Continuously.*

</div>
