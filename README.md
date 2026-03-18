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
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
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
| **Backend** | Node.js, Express, TypeScript |
| **Frontend** | React 19, Vite, Tailwind CSS 4, Framer Motion |
| **Database** | PostgreSQL with JSONB support |
| **Real-time** | WebSockets (ws) for live bid broadcasting |
| **Icons** | Lucide React |

---

## 🏗️ System Architecture

The system follows a modern asynchronous architecture:

1.  **Node.js API Layer:** Express handles high-concurrency bid submissions with minimal latency, written in Type-Safe TypeScript.
2.  **Database Strategy:** PostgreSQL handles relational data, while `JSONB` columns store flexible cost breakdowns, allowing for varied quoting structures without schema migrations.
3.  **Concurrency Control:** Row-level locking and atomic updates ensure bid integrity during rapid-fire competition.
4.  **Real-time Updates:** WebSocket integration provides instant feedback on bid rankings and auction status.

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
*   Node.js 20+
*   PostgreSQL Instance

### 2. Repository Setup
```bash
# Clone the repository
git clone https://github.com/your-org/british-rfq-system.git
# Install Dependencies
npm install
```

### 3. Environment Configuration
Create a `.env` file in the root directory:
```env
DATABASE_URL=postgresql://user:password@localhost:5432/rfq_db
JWT_SECRET=your_royal_secret_key
```

### 4. Launching the System
```bash
# Start the Development Server (Express + Vite)
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
