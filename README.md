# AURA: Real-Time Commodity Price Prediction Platform

**Aura** is a next-generation platform designed to bring transparency and predictive insights to the commodity market. By leveraging community-driven data and advanced machine learning, Aura empowers consumers and admins to track, verify, and forecast price trends for essential goods.

---

## 🚀 The Vision
In many regions, the prices of essential commodities (like petrol, diesel, or groceries) fluctuate based on local market dynamics that are often opaque to the average consumer. Aura bridges this gap by providing a real-time, verified directory of local prices, protected by AI-driven anomaly detection and enhanced by predictive forecasting.

---

## ✨ Key Features

### 1. Community-Driven Price Directory
Users can report prices they observe in their local markets. The directory provides a clean, searchable interface to view modal prices, price ranges, and specific market locations.

### 2. AI-Powered Data Integrity (Anomaly Detection)
To prevent spam or "fake" price reporting, Aura integrates a **Z-Score Anomaly Detection** system. Every submission is analyzed against historical data:
- **Automatic Flagging**: Submissions that deviate by more than 3 standard deviations from the mean are automatically flagged as "FLAGGED".
- **Spam Protection**: Only "APPROVED" entries are shown in the public directory, ensuring data reliability.

### 3. Predictive Insights (Forecasting)
Aura doesn't just show you where prices are—it tells you where they are going. Using **Meta's Prophet Model**, the platform generates 7-day forecasts:
- **Decision Support**: The system provides clear advice like "Buy Now" or "Wait to Buy" based on predicted trends.
- **Seasonality**: The model accounts for daily and weekly patterns to provide accurate time-series analysis.

### 4. Community Verification (Voting System)
Accuracy is further reinforced through a net-voting system. Community members can upvote or downvote price entries, allowing the most accurate data to rise to the top.

### 5. Robust Admin Dashboard
A dedicated admin suite for:
- **Data Governance**: Approving or deleting flagged entries.
- **Analytics**: Viewing system-wide trends and user activity.
- **User Management**: Secure sign-in/sign-up for administrators.

---

## 🛠️ Technical Stack

### **Frontend (Client)**
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite
- **Routing & State**: TanStack Router & TanStack Start
- **Styling**: Tailwind CSS with Framer Motion for interactive UI
- **Icons**: Lucide React

### **Backend (Server)**
- **Framework**: FastAPI (Python 3.11+)
- **Database**: PostgreSQL (Hosted on **Neon Serverless**)
- **ORM**: SQLAlchemy
- **Validation**: Pydantic v2

### **Machine Learning Engine**
- **Forecasting**: Facebook Prophet
- **Analytics**: Pandas & NumPy
- **Algorithm**: Z-Score for real-time outlier detection

---

## 📂 Project Structure

### **Server (Backend)**
```text
server/
├── app/
│   ├── api/            # FastAPI Route Definitions
│   ├── ml/             # ML Engine (Anomaly & Forecasting)
│   ├── crud.py         # Database Transaction Logic
│   ├── models.py       # SQLAlchemy Database Models
│   ├── schemas.py      # Pydantic Data Validation
│   └── main.py         # Application Entry Point
├── DOC/                # Technical Documentation
└── seed_db.py          # Data Seeding Scripts
```

### **Client (Frontend)**
```text
AURA(CLIENT)/
├── src/
│   ├── routes/         # TanStack File-based Routing
│   ├── components/     # Reusable UI Components
│   ├── lib/            # Auth and API Utilities
│   └── server.ts       # SSR Handler for TanStack Start
├── vite.config.ts      # Vite & Proxy Configuration
└── tailwind.config.ts  # Design System Tokens
```

---

## 🛠️ Getting Started

### 1. Prerequisites
- Python 3.11+
- Node.js 18+
- Neon PostgreSQL Database Account

### 2. Backend Setup
```bash
cd server
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
# Create a .env file with DATABASE_URL
uvicorn app.main:app --reload
```

### 3. Frontend Setup
```bash
cd AURA(CLIENT)
npm install
npm run dev
```

---

## 🗺️ Roadmap
- [ ] **JWT Authentication**: Moving from simple session cookies to secure JWT tokens.
- [ ] **Mobile App**: Expanding the React-based logic to a native mobile experience.
- [ ] **Advanced ML**: Implementing more complex seasonal models for specific agricultural products.
- [ ] **Map Integration**: Visualizing price data on an interactive map using Leaflet/Google Maps.

---
**Project Developed for University Excellence**
*Authored by Raktim & Team Aura*
