# CACTUS Architecture

## High-Level Architecture

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

## Component Details

### Frontend (Next.js)

- **Framework**: Next.js 14 with React 18
- **Styling**: TailwindCSS with NVIDIA-style theme
- **State Management**: Zustand
- **Data Fetching**: React Query
- **Real-time**: WebSocket connections
- **Visualization**: Recharts, Three.js, Cytoscape

### Backend (FastAPI)

- **Framework**: FastAPI with Python 3.9+
- **Database**: PostgreSQL 14+ with SQLAlchemy async
- **Cache**: Redis
- **Authentication**: JWT with bcrypt
- **API Gateway**: Rate limiting, CORS, security headers
- **WebSocket**: Real-time event streaming

### AI Engine

- **Anomaly Detection**: Isolation Forest + Autoencoder
- **Threat Classification**: XGBoost
- **MITRE Mapping**: BERT-based technique mapping
- **Threat Scoring**: Neural network

### Agents

- **Windows**: Python + PowerShell hybrid
- **Linux**: Python + systemd service
- **macOS**: Python + launchd service

## Data Flow

### Threat Detection Pipeline

```
Agent → Telemetry → API Gateway → AI Engine → Threat Scoring → Database → WebSocket → Frontend
```

### Firewall Analysis Pipeline

```
Config Upload → Parser → Normalizer → Analyzer → Compliance Checker → Remediation Generator → Report
```

## Security Architecture

- **Authentication**: JWT tokens with refresh mechanism
- **Authorization**: Role-based access control (RBAC)
- **Encryption**: TLS/SSL for all communications
- **Audit Logging**: All actions logged
- **Input Validation**: Pydantic models
- **Rate Limiting**: Redis-based rate limiting
- **Security Headers**: Comprehensive security headers

## Scalability

- **Horizontal Scaling**: Stateless backend, multiple instances
- **Database**: Connection pooling, read replicas
- **Cache**: Redis for session and rate limiting
- **Load Balancing**: NGINX or cloud load balancer

## Monitoring

- **Metrics**: Prometheus endpoint
- **Health Checks**: `/health` endpoint
- **Logging**: Structured logging with levels
- **Tracing**: Distributed tracing support

