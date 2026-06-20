# 🌌 AURA — AUTOMATED REAL-TIME ANALYSIS 

<div align="center">

### **MACHINE LEARNING BASED GROCERY PRICE PREDICTION AND FORECASTING SYSTEM**

*Bringing transparency, trust, and predictive insights to real-world commodity markets. Update check*

<br/>

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-green?style=for-the-badge&logo=fastapi)
![React](https://img.shields.io/badge/React-18-blue?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-Frontend-3178C6?style=for-the-badge&logo=typescript)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon_DB-336791?style=for-the-badge&logo=postgresql)
![Prophet](https://img.shields.io/badge/ML-Facebook_Prophet-purple?style=for-the-badge)

</div>

---

# OVERVIEW

**Aura** is a purely Machine Learning based platform designed to provide **real-time commodity future price predictions** through community-driven reporting, anomaly detection, and machine learning forecasting.

The platform enables users to:
- Discover verified local commodity prices
- Detect suspicious or manipulated price entries
- Analyze market trends
- Predict future price movements using AI

Aura transforms scattered market information into a **transparent, intelligent, and reliable ecosystem** for both consumers and administrators.

---

#  VISION

In many regions, commodity prices fluctuate rapidly due to local market dynamics that are often hidden from consumers.

Aura aims to solve this by creating:

✅ A trusted community-driven price network  
✅ AI-verified pricing integrity  
✅ Predictive forecasting for smarter decisions  
✅ A scalable real-time market intelligence system  

---

# CORE FEATURES

---

## 1. Community-Driven Price Directory

Users can submit and browse commodity prices from local markets in real time.

### Features
- Searchable market directory
- Price ranges & modal prices
- Location-specific entries
- Clean and responsive UI
- Community-generated market intelligence

---

## 2. Machine Learning based Anomaly Detection

Aura integrates a **Z-Score Statistical Detection Engine** to identify suspicious price submissions automatically.

### How It Works

Every submitted price is analyzed against historical market data.

If a value deviates significantly from the statistical norm:

\[
Z = \frac{(X - \mu)}{\sigma}
\]

The entry is automatically flagged.

### Detection Logic
- **Approved** → Normal submissions
- **Flagged** → Suspicious outliers
- **Spam Prevention** → Fake entries blocked from public visibility

### Benefits
- Prevents manipulation
- Maintains data integrity
- Improves trustworthiness of market information

---

## 3. Predictive Forecasting Engine

Aura leverages **Meta's Prophet Model** for intelligent time-series forecasting.

### Forecasting Capabilities
- 7-Day commodity price predictions
- Seasonal trend analysis
- Daily & weekly market pattern recognition
- Predictive buying recommendations

### Example Insights
| Market Trend | Recommendation |
|---|---|
| Prices expected to rise | **Buy Now** |
| Prices expected to fall | **Wait to Buy** |

### ML Stack
- Prophet
- Pandas
- NumPy
- Time-Series Analysis

---

## 4. Community Verification System

Aura includes a voting-based trust mechanism.

### Voting Features
- Upvote accurate entries
- Ignore suspicious reports
- Surface trustworthy data
- Community-driven verification layer

This creates a decentralized validation ecosystem.

---

## 5. Admin Governance Dashboard

A complete administrative suite for platform governance.

### Admin Capabilities
- Review flagged entries
- Approve/Delete submissions
- Monitor analytics
- Observe system-wide trends

---

# System Architecture

```text
 ┌────────────────────┐
 │     React Client    │
 │  (TanStack Start)   │
 └─────────┬──────────┘
           │ REST API
           ▼
 ┌────────────────────┐
 │      FastAPI        │
 │   Backend Server    │
 └─────────┬──────────┘
           │
   ┌───────┴────────┐
   ▼                ▼
┌───────────┐   ┌────────────┐
│ PostgreSQL │   │ ML Engine │
│ Neon DB    │   │ Prophet AI│
└───────────┘   └────────────┘
```

---

# Tech Stack

# 🎨 Frontend

| Technology | Purpose |
|---|---|
| React 18 | Frontend Framework |
| TypeScript | Type Safety |
| Vite | Build Tool |
| TanStack Router | Routing |
| TanStack Start | SSR Framework |
| Tailwind CSS | Styling |
| Framer Motion | UI Animations |
| Lucide React | Icons |

---

# ⚙️ Backend

| Technology | Purpose |
|---|---|
| FastAPI | API Framework |
| Python 3.11+ | Runtime |
| SQLAlchemy | ORM |
| Pydantic v2 | Validation |
| PostgreSQL | Database |
| Neon Serverless | Cloud Database Hosting |

---

# 🤖 Machine Learning

| Tool | Purpose |
|---|---|
| Prophet | Forecasting |
| Pandas | Data Analysis |
| NumPy | Numerical Computing |
| Z-Score Algorithm | Anomaly Detection |

---

# 📂 Project Structure

# 🖥️ Backend Structure

```text
server/
│
├── app/
│   ├── api/                # FastAPI Route Definitions
│   ├── ml/                 # Machine Learning Engine
│   ├── crud.py             # Database Operations
│   ├── models.py           # SQLAlchemy Models
│   ├── schemas.py          # Pydantic Validation Schemas
│   └── main.py             # FastAPI Entry Point
│
├── DOC/                    # Technical Documentation
│
└── seed_db.py              # Database Seeding Script
```

---

# 🌐 Frontend Structure

```text
AURA(CLIENT)/
│
├── src/
│   ├── routes/             # File-Based Routing
│   ├── components/         # Reusable Components
│   ├── lib/                # Utilities & API Layer
│   └── server.ts           # SSR Handler
│
├── vite.config.ts
└── tailwind.config.ts
```

---

# ⚡ Getting Started

# 1️⃣ Prerequisites

Ensure the following are installed:

- Python 3.11+
- Node.js 18+
- PostgreSQL / Neon Database
- Git

---

# 2️⃣ Backend Setup

```bash
# Navigate to backend
cd server

# Create virtual environment
python -m venv .venv

# Activate environment

# Windows
.venv\Scripts\activate

# Linux / Mac
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create environment file
touch .env

# Add DATABASE_URL inside .env

# Start server
uvicorn app.main:app --reload
```

---

# 3️⃣ Frontend Setup

```bash
# Navigate to frontend
cd AURA(CLIENT)

# Install dependencies
npm install

# Start development server
npm run dev
```

---

# 🔐 Environment Variables

Create a `.env` file inside the backend directory.

```env
DATABASE_URL=your_neon_postgresql_url
```

---

# 📊 Machine Learning Workflow

```text
User Submission
       │
       ▼
Data Validation
       │
       ▼
Z-Score Analysis
       │
 ┌─────┴─────┐
 │           │
 ▼           ▼
APPROVED   FLAGGED
 │
 ▼
Stored in PostgreSQL
 │
 ▼
Forecasting Engine
 │
 ▼
Prediction Results
```

---

# 🧪 API Philosophy

Aura follows:
- RESTful API Design
- Clean Separation of Concerns
- Scalable Service Architecture
- Typed Validation using Pydantic
- Async-first Backend Design

---

# 📌 Future Roadmap

- [ ] JWT Authentication
- [ ] Native Mobile Application
- [ ] Real-Time WebSocket Updates
- [ ] Advanced Seasonal Forecast Models
- [ ] Interactive Market Maps
- [ ] Regional Trend Heatmaps
- [ ] AI-Based Demand Prediction
- [ ] Multi-Language Support

---

# 🤝 Contributing

Contributions are welcome.

### Development Workflow
```bash
# Fork Repository
# Create Feature Branch
git checkout -b feature/amazing-feature

# Commit Changes
git commit -m "Add amazing feature"

# Push Changes
git push origin feature/amazing-feature
```

---

# 📄 License

This project is developed for educational and research purposes.

---

# 👨‍💻 Author

### Roktim Taye
### LinkedIn 
```text
https://www.linkedin.com/in/roktim-taye-86957437a/
```

**Developed for University Excellence**

---

# 🔗 Repository Links

## Frontend Repository
```text
https://github.com/RoktimTaye/AURA-CLIENT
```

## Backend Repository
```text
https://github.com/YOUR_BACKEND_REPO
```

---

# ⭐ Final Note

Aura is more than a price directory.

It is a scalable Machine Learning based ecosystem designed to:
- Improve market transparency
- Empower consumers
- Prevent misinformation
- Predict future commodity trends intelligently

---

<div align="center">

## AURA

### *"Predicting Markets. Empowering Communities."*

</div>
