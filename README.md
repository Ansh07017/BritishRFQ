# 🏛️ British Auction RFQ System

<p align="center">
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" width="100%">
</p>

<p align="center">
  <h1 align="center">BRITISH AUCTION RFQ SYSTEM</h1>
  <p align="center">
    <i>Elite Logistics Procurement & Real-Time Reverse Auction Engine</i>
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi" alt="FastAPI">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <br>
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/Build-Passing-brightgreen.svg?style=flat-square" alt="Build Status">
</p>

---

## 📖 Overview

The **British Auction RFQ System** is an enterprise-grade logistics procurement platform designed for high-stakes freight bidding. It implements a **Reverse British Auction** model where suppliers compete in real-time to offer the lowest price for shipping contracts.

The system is engineered with strict temporal constraints, including **Dynamic Time Extensions** (to prevent last-second "sniping") and **Forced-Close Windows** to ensure operational deadlines are met.

---

## ✨ Core Features

*   **👑 Role-Based Access Control (RBAC):** Distinct workflows for **Buyers** (Auctioneers) and **Suppliers** (Bidders).
*   **⏱️ Real-Time Auction Logic:** Descending price competition with live WebSocket updates for rankings and activity logs.
*   **🛡️ Anti-Sniping Engine:** Automatic auction extensions when bids are placed within the final minutes of a window.
*   **📦 Dynamic JSONB Quoting:** Flexible cost breakdown structures (Freight, Origin, Destination charges) stored as structured JSON.
*   **📊 Live Supplier Rankings:** Instant "L1, L2, L3" ranking visibility for both buyers and suppliers.
*   **📜 Audit-Ready Activity Logs:** Comprehensive event tracking for every bid, extension, and status change.

---

## 🛠️ Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Backend** | FastAPI (Python 3.10+), SQLAlchemy, Pydantic |
| **Frontend** | React 18, Vite, Tailwind CSS, Framer Motion |
| **Database** | PostgreSQL with JSONB support |
| **Real-time** | WebSockets for live bid broadcasting |
| **Icons** | Lucide React |

---

## 🏗️ System Architecture

The system follows a modern asynchronous architecture:

1.  **Async API Layer:** FastAPI handles high-concurrency bid submissions with minimal latency.
2.  **Database Strategy:** PostgreSQL handles relational data, while `JSONB` columns store flexible cost breakdowns, allowing for varied quoting structures without schema migrations.
3.  **Concurrency Control:** Row-level locking and atomic updates ensure bid integrity during rapid-fire competition.
4.  **Background Schedulers:** A dedicated worker process monitors auction expiry, triggering closures and status transitions precisely.

---

## 🎥 Video Presentation

Check out the full video presentation of the **British Auction RFQ System** on Loom:

<p align="center">
  <a href="https://www.loom.com/share/your_loom_video_id">
    <img src="https://cdn.loom.com/sessions/thumbnails/your_loom_video_id-with-play.gif" alt="British Auction RFQ System Presentation" width="600">
  </a>
</p>

---

## 🚀 Quickstart & Local Setup

### 1. Prerequisites
*   Python 3.10+
*   Node.js 18+
*   PostgreSQL Instance

### 2. Repository Setup
```bash
# Clone the repository
git clone https://github.com/your-org/british-rfq-system.git
cd british-rfq-system

# Set up Python Virtual Environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install Backend Dependencies
pip install -r requirements.txt

# Install Frontend Dependencies
npm install
```

### 3. Environment Configuration
Create a `.env` file in the root directory:
```env
DATABASE_URL=postgresql://user:password@localhost:5432/rfq_db
SECRET_KEY=your_royal_secret_key
VITE_API_URL=http://localhost:8000
```

### 4. Launching the System
```bash
# Start the Backend Server (FastAPI)
uvicorn main:app --reload --port 8000

# Start the Frontend Development Server (Vite)
npm run dev
```

---

## 🖼️ UI Previews

### Dashboard View
![Dashboard View](https://via.placeholder.com/800x450.png?text=British+RFQ+Dashboard+Preview)

### Auction Details & Real-Time Bidding
![Auction Details](https://via.placeholder.com/800x450.png?text=Real-Time+Auction+Interface)

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

<p align="center">
  <img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/aqua.png" width="100%">
</p>
