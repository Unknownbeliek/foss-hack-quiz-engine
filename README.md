# 🎬 CineGnosis

**The Offline-First, Zero-Latency Multiplayer Movie Trivia Game.**

> *Built for FOSS Hack 2026*

## 🛑 The Problem
Popular multiplayer quiz games (like Kahoot, Jackbox, or Skribbl) have a single point of failure: **The Internet.**
In high-density venues like college auditoriums, hackathons, or basements with poor reception, these cloud-dependent apps frequently lag, disconnect, or crash. They also require 100% online connectivity for every player, ruining the social experience.

## ⚡ The Solution
**CineGnosis** is a self-hosted game engine that runs entirely on the host's machine. It decouples gameplay from ISP stability.
* **Internet Down?** No problem. Players join via your Local Hotspot (LAN).
* **Remote Friends?** No problem. They join via a secure Tunnel (WAN).
* **Latency?** Near Zero (2ms) for local players.

## 🚀 Key Innovations
* **Hybrid Network Core:** Uniquely allows players to join via Local LAN (Offline) and Secure Tunnel (Online) simultaneously in the same game lobby.
* **"Forgiving" Input System:** Uses `Fuse.js` for client-side fuzzy matching. It auto-corrects typos (e.g., "Interstelar" → "Interstellar"), making the game accessible and fast-paced.
* **Danmaku Social Layer:** Features a live chat overlay where player comments float across the host's main screen in real-time (like Niconico/Twitch).
* **Smart Asset Caching:** The engine works 100% offline with generic assets but uses a "Cache-on-Demand" strategy to fetch high-res posters only when connectivity permits.

## 🛠️ Tech Stack
* **Backend:** Node.js + Express
* **Real-time:** Socket.io (WebSocket)
* **Frontend:** React (Vite)
* **Search Engine:** Fuse.js (Client-side Fuzzy Search)
* **Data:** Local JSON / NoSQL (No external DB required)

## 🔮 Roadmap (Hackathon Goals)
- [x] **Phase 1:** Core Offline Server Logic (Node.js/Socket.io)
- [ ] **Phase 2:** Fuzzy Search & Autocomplete UI
- [ ] **Phase 3:** The "Danmaku" Chat Overlay
- [ ] **Phase 4:** Hybrid Tunneling Integration

## 💿 Installation (Dev)
## 📂 Project Structure
This project follows a monorepo-style structure to keep Backend and Frontend separated but synchronized.

```text
/cinegnosis
  ├── server/         # Node.js + Socket.io (Game State & Room Logic)
  ├── client/         # React + Vite (UI, Animation, Chat Overlay)
  ├── data/           # movies.json (The pre-seeded offline database)
  └── docs/           # Architecture diagrams & setup guides
```bash
# Clone the repository
git clone [https://github.com/YOUR_USERNAME/cinegnosis.git](https://github.com/YOUR_USERNAME/cinegnosis.git)

# Install dependencies
npm install

# Start the Development Server
npm run dev
