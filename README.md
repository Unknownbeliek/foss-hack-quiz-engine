# 🎬 [Project Name] / Offline Movie Quiz Engine

**The Offline-First, Zero-Latency Multiplayer Trivia Game.**

> *Built for FOSS Hack 2026*

## 🛑 The Problem
Standard quiz games (Kahoot, Jackbox, Skribbl) have a single point of failure: **The Internet.**
If the venue Wi-Fi is congested or the ISP goes down, the game is over. They also require 100% online connectivity for every player, leading to lag and disconnects in crowded spaces like college auditoriums.

## ⚡ The Solution
**[Project Name]** is a self-hosted game engine. The "Server" runs on **your** laptop, not in the cloud.
* **Internet Down?** No problem. Players join via your Local Hotspot (LAN).
* **Remote Friends?** No problem. They join via a secure Tunnel (WAN).
* **Latency?** Near Zero (2ms) for local players.

## 🚀 Key Features
* **Hybrid Network Core:** Supports LAN (Offline) and WAN (Online) players in the same game room.
* **"Forgiving" Input System:** Uses `Fuse.js` for fuzzy matching. (e.g., Typing "Interstelar" correctly guesses "Interstellar").
* **Danmaku Chat:** Live player comments float across the Host's big screen in real-time.
* **Privacy First:** No data harvesting. No tracking. 100% Open Source.
* **Dynamic Asset Loading:** Uses a hybrid "Cache-on-Demand" system to keep the install size small (20MB) while fetching high-res posters only when needed.

## 🛠️ Tech Stack
* **Backend:** Node.js + Express
* **Real-time:** Socket.io
* **Frontend:** React (Vite)
* **Search Engine:** Fuse.js (Client-side Fuzzy Search)
* **Data:** Local JSON (No external DB required for offline mode)

## 🔮 Roadmap (Hackathon Goals)
- [x] **Phase 1:** Core Offline Server Logic (Node.js/Socket.io)
- [ ] **Phase 2:** Fuzzy Search & Autocomplete UI
- [ ] **Phase 3:** The "Danmaku" Chat Overlay
- [ ] **Phase 4:** Hybrid Tunneling Integration

## 💿 Installation (Dev)
```bash
# Clone the repo
git clone [https://github.com/YOUR_USERNAME/offline-movie-quiz.git](https://github.com/YOUR_USERNAME/offline-movie-quiz.git)

# Install dependencies
npm install

# Start the Server
npm start
