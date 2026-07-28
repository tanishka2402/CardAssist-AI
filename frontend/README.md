# 🎨 CardAssist-AI — Frontend Application

> **User Interface Portal for Cardholders & Customer Service Admin Dashboard.**

---

## 📋 Overview
The `frontend` module provides an intuitive, responsive web application for CardAssist-AI. It empowers cardholders to interact with AI agents, manage credit cards, request limit increases, view audit trails, and report fraudulent activities in real-time.

---

## 📂 Directory Structure

```
frontend/
├── app/          # Next.js App Router / Page definitions & layouts
├── components/   # Modular, reusable UI components (Buttons, Modals, Chat Widgets)
├── hooks/        # Custom React hooks (useAuth, useAgentStream, useCardDetails)
├── lib/          # Utilities, formatters, and client-side helper functions
├── services/     # API integration service modules (Backend HTTP/WebSocket clients)
├── public/       # Static assets (images, icons, fonts, site manifest)
└── styles/       # Global styles, CSS modules, design tokens, and theme configs
```

---

## 🛠️ Technology Stack
- **Framework:** React / Next.js (App Router)
- **Styling:** Vanilla CSS / Tailwind CSS Token System
- **State Management:** React Context & Custom Hooks
- **HTTP Client:** Axios / Native Fetch API
- **Real-Time Communication:** WebSockets for AI Agent streaming responses

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- pnpm / npm / yarn

### Installation & Development
```bash
cd frontend
npm install
npm run dev
```
Access the application at `http://localhost:3000`.

---

## 🧪 Testing
```bash
npm run test
```
