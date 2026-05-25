<div align="center">

<br />

<img src="https://raw.githubusercontent.com/sultannafis/SkyraAI/main/public/logo.png" alt="SkyraAI Logo" width="80" height="80" />

# SkyraAI

**Your intelligent AI chat companion — built for speed, designed for humans.**

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-skyraai.vercel.app-000000?style=for-the-badge)](https://skyraai.vercel.app/)
&nbsp;
[![React](https://img.shields.io/badge/React%2018-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript%205-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite%205-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vite.dev/)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)](https://supabase.com/)
[![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)](https://vercel.com/)

<br />

> A full-stack AI chat application with authentication, conversation history,  
> image analysis, and a clean modern UI — deployed and production-ready.

<br />

[**🚀 Try Live Demo**](https://skyraai.vercel.app/) &nbsp;·&nbsp; [**📖 Documentation**](#getting-started) &nbsp;·&nbsp; [**🐛 Report Bug**](https://github.com/sultannafis/SkyraAI/issues) &nbsp;·&nbsp; [**✨ Request Feature**](https://github.com/sultannafis/SkyraAI/issues)

</div>

---

## What is SkyraAI?

SkyraAI is a modern, full-stack AI chat application that lets users have natural conversations with an AI assistant through a clean, responsive interface. Built with a focus on developer experience and real-world patterns — it goes beyond the typical "Hello World" AI demo.

The app handles the full product lifecycle: authentication, persistent chat history, image uploads, serverless API integration, and production deployment — all the things that actually matter when shipping a real product.

---

## Features

**🤖 AI Chat Interface**  
Clean, interactive chat with real-time AI responses. Minimal, distraction-free design focused on the conversation.

**🖼️ Image Upload & Analysis**  
Send images alongside your messages and have the AI analyze, describe, or discuss them.

**📜 Chat History**  
All conversations are saved to your account. Pick up where you left off, anytime.

**🔐 Authentication**  
Full login and register flow powered by Supabase — secure and production-ready.

**📱 Fully Responsive**  
Works seamlessly across desktop, tablet, and mobile.

**🔒 Secure by Default**  
API keys stay on the server via Vercel Serverless Functions. Nothing sensitive is exposed to the client.

**🧩 Component-Driven UI**  
Modals, sidebars, and panels built as reusable components — easy to extend.

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 18, TypeScript 5, Vite 5 |
| **Styling** | Custom CSS |
| **Routing** | React Router DOM |
| **Animation** | Framer Motion |
| **Icons** | React Icons |
| **HTTP** | Axios |
| **Serverless API** | Vercel Functions |
| **Auth & Database** | Supabase |
| **AI Provider** | OpenRouter API |
| **Deployment** | Vercel |

---

## Project Structure

```
skyra-ai/
├── api/
│   ├── chat.js              # Serverless endpoint for text chat
│   └── vision.ts            # Serverless endpoint for image analysis
│
├── src/
│   ├── components/
│   │   ├── AboutModal.tsx
│   │   ├── HelpModal.tsx
│   │   ├── ImageWarningModal.tsx
│   │   ├── ProfileModal.tsx
│   │   ├── SettingsModal.tsx
│   │   ├── Sidebar.tsx
│   │   └── UserPanel.tsx
│   │
│   ├── pages/
│   │   ├── ChatPage.tsx
│   │   ├── LoginPage.tsx
│   │   ├── RegisterPage.tsx
│   │   └── ProtectedRoute.tsx
│   │
│   ├── lib/
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
│
├── supabase/
├── public/
├── vercel.json
├── vite.config.ts
└── package.json
```

---

## Getting Started

### Prerequisites

- Node.js 18+
- A [Supabase](https://supabase.com/) project
- An [OpenRouter](https://openrouter.ai/) API key

### 1. Clone the Repository

```bash
git clone https://github.com/sultannafis/SkyraAI.git
cd SkyraAI
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root of the project:

```env
# AI Provider
OPENROUTER_API_KEY=your_openrouter_api_key
REFERER=http://localhost:5173

# Supabase
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

> ⚠️ Never commit your `.env` file. Make sure `.gitignore` covers it.

### 4. Start Development Server

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) to see the app.

---

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |

---

## Deployment

SkyraAI is deployed on **Vercel** and live at [skyraai.vercel.app](https://skyraai.vercel.app/).

### Deploy via Vercel CLI

```bash
npm install -g vercel
vercel
```

### Deploy Manually

```bash
npm run build
```

Then upload the `dist/` folder or connect the repo to [Vercel's dashboard](https://vercel.com/dashboard).

### Environment Variables on Vercel

Add these in your Vercel project settings under **Settings → Environment Variables**:

```
OPENROUTER_API_KEY
REFERER
VITE_SUPABASE_URL
VITE_SUPABASE_ANON_KEY
```

---

## Application Flow

```
User opens app
     ↓
Login / Register  (Supabase Auth)
     ↓
Chat Page
     ↓
User sends message or uploads image
     ↓
Request goes to Vercel Serverless Function
     ↓
Function calls OpenRouter AI API  (key never exposed to client)
     ↓
AI response streams back
     ↓
Response displayed in chat
     ↓
Conversation saved to Supabase
```

---

## Roadmap

- [ ] Streaming responses (real-time word-by-word output)
- [ ] Dark mode & theme customization
- [ ] Multi-model selector (GPT-4, Claude, Gemini, etc.)
- [ ] Export conversations to PDF or TXT
- [ ] Chat search & filtering
- [ ] Voice input support
- [ ] Admin dashboard
- [ ] Unit & integration tests

---

## Author

**Sultan Nafis** — Fresh Graduate Software Developer

Focused on building modern web applications with clean architecture, interactive UIs, and AI integrations.

[![GitHub](https://img.shields.io/badge/GitHub-@sultannafis-181717?style=flat-square&logo=github)](https://github.com/sultannafis)
[![Live App](https://img.shields.io/badge/Live%20App-skyraai.vercel.app-000000?style=flat-square&logo=vercel)](https://skyraai.vercel.app/)

---

## License

This project is open for learning, portfolio reference, and personal experimentation.

---

<div align="center">

Made with ☕ and TypeScript by **Sultan Nafis**

⭐ If this project helped or inspired you, consider giving it a star!

</div>
