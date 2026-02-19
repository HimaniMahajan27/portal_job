# 🚀 AI Backend API Configuration  
### Gemini + Groq Integration Guide

This document explains how to configure AI provider API keys for backend features.

---

## 📌 1. Environment Setup

Open the following file:

```
backend/.env
```

Add your API keys:

```env
GEMINI_API_KEY=your_gemini_api_key
GROQ_API_KEY=your_groq_api_key
```

> 💡 It is recommended to configure both keys for improved reliability.

---

## 🔄 2. Provider Fallback Strategy

The backend uses an automatic fallback mechanism:

| Feature | Provider Order |
|----------|----------------|
| Resume Analysis | Gemini → Groq → Template |
| Cover Letter Generation | Groq → Gemini → Template |
| Practice Test | Groq → Gemini → Template |

If one provider fails (quota, rate-limit, downtime), the next provider is used automatically.

---

## 🔑 3. Generate API Keys

### 🟢 Gemini
1. Visit: https://makersuite.google.com/app/apikey  
2. Create a new API key  
3. Add it inside `.env`  

### 🔵 Groq
1. Visit: https://console.groq.com/keys  
2. Create a new API key  
3. Add it inside `.env`  

---

## 🔁 4. Restart Backend Server

After modifying the `.env` file, restart the backend:

```bash
cd backend
npm run dev
```

Environment variables are loaded only when the server starts.

---

## ✅ 5. Verify Configuration

1. Start backend and frontend  
2. Login to the application  
3. Test the following features:
   - Resume Analyzer
   - Cover Letter Generator
   - Practice Test Module  

If setup is correct, AI responses should generate without errors.

---

## ⚙️ 6. Configuration Modes

- **Both Keys Configured** → Best reliability (Recommended)
- **Only Gemini** → Resume prioritizes Gemini
- **Only Groq** → Groq handles primary flows
- **No Keys** → Basic template responses only

---

## 🛠️ 7. Troubleshooting

### 401 – Invalid API Key
- Remove extra spaces or quotes
- Regenerate the key
- Confirm correct `.env` file

### 429 – Rate Limit
- Retry after some time
- Configure both providers

### No AI Output
- Confirm keys exist in `backend/.env`
- Restart backend
- Check server logs

---

## 🔒 8. Security Guidelines

- Never commit `.env` files to GitHub  
- Keep API keys confidential  
- Rotate keys immediately if exposed  

---

## 📄 Example `.env` File

```env
PORT=5000
NODE_ENV=development
MONGO_URI=mongodb://localhost:27017/job-portal

CLIENT_URL=http://localhost:3000
JWT_SECRET=your_secure_random_secret
SESSION_SECRET=your_secure_random_secret

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:5000/api/auth/google/callback

GEMINI_API_KEY=your_gemini_api_key
GROQ_API_KEY=your_groq_api_key
```
