# 🎨 CardAssist-AI — Frontend Development Branch (`frontend`)

> **Domain Branch for Web UI Application, React Components, Custom Hooks, and Client Services.**

---

## 📌 Branch Focus: Frontend Subsystem

This branch (`frontend`) is dedicated to building and refining the user interface of CardAssist-AI. Developers working on this branch focus on UI components, state management, API service client integration, theme tokens, and user experience.

---

## 📂 Frontend Subsystem Map (`frontend/`)

```
frontend/
├── app/          # Next.js App Router / Page definitions & layout templates
├── components/   # UI components (Card Visualizer, Chat Widget, Modal Dialogs)
├── hooks/        # React Hooks (useAuth, useAgentStream, useCardActions)
├── lib/          # Utilities, formatters, and client-side helper functions
├── services/     # API integration service modules (Backend HTTP/WebSocket clients)
├── public/       # Static assets (images, icons, fonts, site manifest)
└── styles/       # Global styles, CSS modules, design tokens, and theme configs
```

---

## 🚀 Quick Start for Frontend Developers

1. **Navigate to the frontend directory:**
   ```bash
   cd frontend
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Run local dev server:**
   ```bash
   npm run dev
   ```
   Open `http://localhost:3000` in your browser.

4. **Detailed Frontend Documentation:**
   See [frontend/README.md](file:///c:/Users/svija/Downloads/CardAssist-AI/frontend/README.md) for full architecture specifications.

---

## 🌿 Git Workflow Rules for `frontend`
- Always pull the latest changes from `develop` before creating new UI features:
  ```bash
  git pull origin develop
  ```
- Push UI updates to `frontend` and open a Pull Request to merge into `develop`.
