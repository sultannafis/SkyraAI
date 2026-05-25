<div align="center">

# SkyAiTan

### Modern AI Chat Assistant built with React, TypeScript, Vite, Supabase, and OpenRouter API

SkyAiTan adalah aplikasi AI chat berbasis web yang dirancang dengan tampilan modern, responsif, dan ringan. Project ini dibuat sebagai eksperimen sekaligus showcase pengembangan aplikasi AI dengan frontend React, autentikasi, riwayat percakapan, fitur upload gambar, serta integrasi API AI.

<br />

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20Website-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://sky-aitan.vercel.app/)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vite.dev/)
[![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)

<br />

**Live Demo:** [https://sky-aitan.vercel.app/](https://sky-aitan.vercel.app/)

</div>

---

## Overview

**SkyAiTan** adalah aplikasi chat AI berbasis web yang memungkinkan pengguna berinteraksi dengan asisten AI melalui interface yang modern, bersih, dan nyaman digunakan.

Aplikasi ini dibangun menggunakan **React**, **TypeScript**, dan **Vite** sebagai frontend utama. Untuk kebutuhan autentikasi dan penyimpanan data, SkyAiTan menggunakan **Supabase**, sedangkan integrasi AI dilakukan melalui **OpenRouter API** dengan pendekatan serverless API agar key lebih aman dan tidak langsung terekspos di sisi client.

Project ini dibuat sebagai bagian dari pengembangan portofolio untuk menunjukkan kemampuan dalam membangun aplikasi web modern, mulai dari UI/UX, routing, reusable component, authentication flow, integrasi API, hingga deployment production menggunakan Vercel.

---

## Preview

> Tambahkan screenshot aplikasi lu di folder `public`, lalu ubah nama file-nya menjadi `preview.png`.

```md
![SkyAiTan Preview](./public/preview.png)
Key Features
AI Chat Interface

User dapat mengirim pesan dan menerima respons dari AI melalui tampilan chat yang sederhana, modern, dan interaktif.

Image Upload Support

Aplikasi mendukung upload gambar untuk kebutuhan interaksi berbasis visual atau analisis gambar menggunakan AI.

Chat History

Riwayat percakapan dapat disimpan sehingga user bisa melihat kembali sesi chat sebelumnya.

Authentication Pages

Tersedia halaman login dan register sebagai bagian dari alur autentikasi pengguna.

Responsive Layout

Tampilan aplikasi dibuat responsif agar nyaman digunakan di desktop, tablet, maupun mobile.

Sidebar Navigation

Sidebar digunakan untuk navigasi utama dan pengelolaan riwayat percakapan.

User Panel

Tersedia panel pengguna untuk mengakses menu profil, pengaturan, bantuan, dan informasi aplikasi.

Modal Components

Aplikasi memiliki beberapa modal pendukung seperti About, Help, Settings, Profile, dan Image Warning.

Serverless API Integration

API digunakan sebagai penghubung antara frontend dan layanan AI eksternal, sehingga API key tidak langsung terbuka di sisi client.

Tech Stack
Layer	Technology
Frontend	React, TypeScript, Vite
Styling	CSS Custom
Routing	React Router DOM
Animation	Framer Motion
Icons	React Icons
HTTP Client	Axios
Backend/API	Vercel Serverless Function
Database/Auth	Supabase
AI Provider	OpenRouter API
Deployment	Vercel
Project Structure
sky-aitan/
├── api/
│   ├── chat.js
│   └── vision.ts
│
├── public/
│
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── AboutModal.tsx
│   │   ├── HelpModal.tsx
│   │   ├── ImageWarningModal.tsx
│   │   ├── ProfileModal.tsx
│   │   ├── SettingsModal.tsx
│   │   ├── Sidebar.tsx
│   │   └── UserPanel.tsx
│   │
│   ├── lib/
│   ├── pages/
│   │   ├── ChatPage.tsx
│   │   ├── LoginPage.tsx
│   │   ├── ProtectedRoute.tsx
│   │   └── RegisterPage.tsx
│   │
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
│
├── supabase/
├── package.json
├── vite.config.ts
├── vercel.json
└── README.md
Getting Started

Ikuti langkah berikut untuk menjalankan project ini secara lokal.

1. Clone Repository
git clone https://github.com/sultannafis/sky-aitan.git
cd sky-aitan
2. Install Dependencies
npm install
3. Setup Environment Variables

Buat file .env di root project:

OPENROUTER_API_KEY=your_openrouter_api_key
REFERER=http://localhost:5173

VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key

Pastikan API key dan kredensial Supabase tidak di-commit ke GitHub.

4. Run Development Server
npm run dev

Aplikasi akan berjalan di:

http://localhost:5173
Available Scripts
Command	Description
npm run dev	Menjalankan development server
npm run build	Build project untuk production
npm run preview	Preview hasil build secara lokal
npm run lint	Menjalankan ESLint
Environment Variables
Variable	Description
OPENROUTER_API_KEY	API key untuk mengakses OpenRouter
REFERER	URL referer yang dikirim ke request API
VITE_SUPABASE_URL	URL project Supabase
VITE_SUPABASE_ANON_KEY	Public anon key dari Supabase
Deployment

Project ini dideploy menggunakan Vercel dan dapat diakses melalui:

https://sky-aitan.vercel.app/

Deploy Manual
npm run build

Lalu upload ke Vercel atau deploy langsung melalui dashboard Vercel.

Deploy with Vercel CLI
npm install -g vercel
vercel

Jangan lupa tambahkan environment variables di dashboard Vercel:

OPENROUTER_API_KEY
REFERER
VITE_SUPABASE_URL
VITE_SUPABASE_ANON_KEY
Main Flow
User membuka aplikasi
        ↓
User login / register
        ↓
User masuk ke halaman chat
        ↓
User mengirim pesan atau gambar
        ↓
Frontend mengirim request ke API
        ↓
API meneruskan request ke layanan AI
        ↓
AI mengirim respons
        ↓
Respons ditampilkan di halaman chat
        ↓
Percakapan tersimpan sebagai chat history
Why This Project Matters

SkyAiTan bukan sekadar project React biasa. Project ini menunjukkan implementasi aplikasi AI end-to-end dengan konsep yang cukup dekat dengan produk nyata.

Beberapa hal yang ditunjukkan dari project ini:

Membangun UI chat interaktif
Mengintegrasikan frontend dengan AI API
Menggunakan serverless function untuk menjaga keamanan API key
Mengelola routing halaman dengan React Router
Membuat reusable component
Menghubungkan aplikasi dengan Supabase
Menyusun struktur project yang rapi dan scalable
Melakukan deployment production menggunakan Vercel

Project ini bisa dikembangkan lebih lanjut menjadi personal AI assistant, chatbot edukasi, customer support bot, atau platform AI berbasis web.

Future Improvements

Beberapa pengembangan yang bisa ditambahkan ke versi berikutnya:

Streaming response agar jawaban AI muncul secara real-time
Dark mode dan theme customization
Export chat ke PDF atau TXT
Folder untuk mengelompokkan chat history
Search chat history
Multi-model selector
Voice input yang lebih stabil
Rate limit API
Admin dashboard
Better error handling
Unit testing dan integration testing
Author

Sultan Nafis

Fresh Graduate Software Developer yang berfokus pada pengembangan aplikasi web modern, UI interaktif, integrasi API, dan pemanfaatan teknologi AI dalam aplikasi berbasis web.

GitHub: @sultannafis
Live App: https://sky-aitan.vercel.app/
License

Project ini dibuat untuk kebutuhan pembelajaran, portofolio, dan pengembangan aplikasi AI berbasis web.

<div align="center">
Built with passion by Sultan Nafis
</div> ```
