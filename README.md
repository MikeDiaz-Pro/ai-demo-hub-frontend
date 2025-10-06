# 🧩 AI Demo Hub – Frontend

This repository contains the **React + Vite frontend** for the AI Demo Hub project, built to integrate seamlessly with the backend API (Spring Boot) and demonstrate advanced AI workflows (LangChain, LangGraph, Azure OpenAI, n8n).

---

## 🚀 Stack Overview

| Layer | Technology | Purpose |
|--------|-------------|----------|
| **Framework** | React 18 + Vite | Modern, fast frontend framework |
| **Styling** | TailwindCSS v3 | Utility-first CSS framework |
| **UI Components** | Material Tailwind | Pre-styled, responsive components |
| **State Management** | Redux Toolkit | Centralized global state handling |
| **HTTP Client** | Axios | Simplified HTTP requests to backend |
| **Notifications** | React Toastify | Clean, global toast notifications |
| **Routing** | React Router v6 | Declarative page navigation |
| **Env Management** | .env / import.meta.env | Environment configuration |

---

## 🏗️ Project Structure

```
ai-demo-hub-frontend/
│
├── src/
│   ├── assets/              # Static files (images, icons, etc.)
│   ├── components/          # Reusable UI elements (Button, Modal, etc.)
│   ├── features/            # Domain-based modules (auth, jobs, chat, etc.)
│   ├── pages/               # Route-level views (Dashboard, Login, etc.)
│   ├── redux/               # Redux store configuration
│   ├── services/            # Axios setup and API clients
│   ├── utils/               # Helpers (formatters, notifications)
│   └── main.jsx             # Entry point
│
├── public/                  # Static public assets
├── .env.example             # Environment variable template
├── index.html               # Main HTML entry
└── package.json             # Dependencies and scripts
```

---

## ⚙️ Environment Variables

All environment variables must begin with the `VITE_` prefix to be accessible in Vite.

### `.env.example`
```bash
# ==========================================
# 🌐 FRONTEND ENVIRONMENT VARIABLES - AI Demo Hub
# ==========================================

# Base API URL (Spring Boot service)
VITE_API_URL=http://localhost:8080/api

# Application mode: development | staging | production
VITE_APP_MODE=development

# Default language (future multilingual support)
VITE_DEFAULT_LANG=en

# Toast notifications theme (light | dark | colored)
VITE_TOAST_THEME=colored
```

Copy it into a real `.env` file for local development:
```bash
cp .env.example .env
```

---

## 🧠 Usage

### Install dependencies
```bash
npm install
```

### Run in development mode
```bash
npm run dev
```

### Build for production
```bash
npm run build
```

### Preview production build
```bash
npm run preview
```

---

## 🎨 Notifications with React Toastify

Global notifications are handled with **React Toastify**.

**Setup (already included in main.jsx):**
```jsx
import { ToastContainer, toast } from "react-toastify";
import "react-toastify/dist/ReactToastify.css";

// Example usage:
toast.success("Operation completed!");
toast.error("Something went wrong");
```

**Helper example (`src/utils/notify.js`):**
```js
import { toast } from "react-toastify";

export const notifySuccess = (msg) => toast.success(msg);
export const notifyError = (msg) => toast.error(msg);
```

---

## 📁 Git Workflow

| Action | Command Example |
|---------|----------------|
| Create branch | `git checkout -b feature/frontend-base-config` |
| Commit changes | `git commit -m "feat(frontend): initialize base structure"` |
| Push branch | `git push origin feature/frontend-base-config` |
| Merge to main | via Pull Request |
| Update local main | `git checkout main && git pull origin main` |

---

## 📘 Developer Notes

- All API URLs are configurable via `.env`.
- The project uses **TailwindCSS** for styling — no manual CSS required.
- Use **functional components and hooks** only (`useState`, `useEffect`, `useSelector`, etc.).
- Keep all reusable UI inside `/components`.
- Each feature (auth, users, chat, etc.) will have its own slice and API client.

---

## 🧩 Author

**Miguel Díaz**  
Fullstack Engineer / AI Integrations  
[GitHub Profile](https://github.com/MikeDiaz-Pro)
