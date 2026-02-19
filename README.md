# 🚀 AI-Powered Job Portal

> Where Talent Meets Opportunity, Enhanced by Intelligence

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-Latest-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-4.0-010101?style=for-the-badge&logo=socket.io&logoColor=white)

[Features](#-features) • [Quick Start](#-quick-start) • [Tech Stack](#-tech-stack) • [Contact](#-contact)

</div>

---

## 📋 Overview

<div align="center">
  
<img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="400">

</div>

A next-generation job portal that bridges the gap between job seekers and employers with cutting-edge AI capabilities. Built with modern web technologies and powered by artificial intelligence, this platform revolutionizes the job search and recruitment process.

### 🎯 Key Highlights

<table>
  <tr>
    <th>👨‍💼 Job Seekers</th>
    <th>🏢 Employers</th>
    <th>🤖 AI Features</th>
  </tr>
  <tr>
    <td>🔍 Advanced Search & Filters</td>
    <td>📝 Easy Job Posting</td>
    <td>🧠 Resume Analysis</td>
  </tr>
  <tr>
    <td>📄 Profile Builder</td>
    <td>📊 Applicant Analytics</td>
    <td>✍️ AI Cover Letter Generator</td>
  </tr>
  <tr>
    <td>💬 Real-time Chat</td>
    <td>👥 Candidate Management</td>
    <td>🎯 Interview Practice</td>
  </tr>
  <tr>
    <td>🎓 Skill Tracking</td>
    <td>🔔 Smart Notifications</td>
    <td>💡 Intelligent Insights</td>
  </tr>
</table>

---

## ✨ Features

### 👨‍💼 For Job Seekers

- **🔐 Authentication**: Email/password & Google OAuth
- **🔍 Job Discovery**: Advanced search, category filters, real-time updates
- **📝 Application Management**: One-click apply, resume upload, status tracking
- **💬 Real-time Messaging**: Direct chat with employers, typing indicators
- **🤖 AI Tools**:
  - Resume analysis with instant feedback
  - Personalized cover letter generation
  - Interview practice with AI questions
  - Intelligent answer evaluation
- **🎓 Experience Sharing**: Read & share anonymous interview experiences

### 🏢 For Employers

- **📋 Job Management**: Create, edit, and track job listings
- **👥 Candidate Review**: View applicants, filter candidates, review documents
- **📊 Analytics**: Track views, applications, and candidate pipeline
- **💬 Direct Messaging**: Real-time communication with job seekers
- **🔔 Notifications**: Stay updated on applications and activities

### 🤖 AI Capabilities

<div align="center">
  
<img src="https://media.giphy.com/media/3o7qDSOvfaCO9b3MlO/giphy.gif" width="300">

</div>

Our AI features use an intelligent fallback chain to ensure **100% uptime**:

| Feature | Primary | Secondary | Fallback |
|---------|---------|-----------|----------|
| Resume Analysis | Google Gemini | Groq | Template |
| Cover Letter | Groq | Google Gemini | Template |
| Interview Practice | Groq | Google Gemini | Template |

**Benefits**: ✅ Always available ✅ No API key required ✅ Graceful degradation

---

## 💻 Tech Stack

### Frontend
- **React** 18.x - UI Framework
- **React Router** 6.x - Navigation
- **Socket.io Client** 4.x - Real-time Communication
- **Axios** - HTTP Client
- **Framer** - Animations

### Backend
- **Node.js** 18+ - Runtime
- **Express** 4.x - Web Framework
- **MongoDB** - Database
- **Socket.io** 4.x - WebSocket Server
- **JWT** - Authentication

### AI & Services
- 🔷 **Google Gemini** - Resume Analysis
- ⚡ **Groq AI** - Cover Letter & Interview
- 🔐 **Google OAuth** - Social Authentication
- 📄 **PDFMake/PDFReader** - PDF Operations

---

## 🚀 Quick Start

### Prerequisites

- Node.js 18+
- npm 9+
- MongoDB (Local or Atlas)

### Installation

#### 1️⃣ Clone Repository
```bash
git clone https://github.com/yourusername/job-portal-ai.git
cd job-portal-ai
```

#### 2️⃣ Backend Setup
```bash
cd backend
npm install
cp .env.example .env
```

**Configure `.env`:**
```env
# Database
MONGODB_URI=mongodb://localhost:27017/job-portal

# JWT
JWT_SECRET=your-super-secret-jwt-key-here
JWT_EXPIRE=7d

# Google OAuth (Optional)
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
GOOGLE_CALLBACK_URL=http://localhost:5000/api/auth/google/callback

# AI APIs (Optional - fallback available)
GEMINI_API_KEY=your-gemini-api-key
GROQ_API_KEY=your-groq-api-key

# Server
PORT=5000
FRONTEND_URL=http://localhost:3000
```

#### 3️⃣ Frontend Setup
```bash
cd ../frontend
npm install
cp .env.example .env
```

**Configure `.env`:**
```env
REACT_APP_API_URL=http://localhost:5000/api
```

#### 4️⃣ Start Development

**Terminal 1 - Backend:**
```bash
cd backend
npm run dev
```

**Terminal 2 - Frontend:**
```bash
cd frontend
npm start
```

#### 5️⃣ Access Application

<div align="center">
  
<img src="https://media.giphy.com/media/26u4cqiYI30juCOGY/giphy.gif" width="300">

</div>

- 🌐 **Frontend**: http://localhost:3000
- 🔌 **Backend API**: http://localhost:5000/api
- 💬 **WebSocket**: http://localhost:5000

---

## 📁 Project Structure

```
job-portal-ai/
│
├── 📂 backend/
│   ├── 📂 config/           # Database, Passport, Socket.IO setup
│   ├── 📂 middleware/       # Authentication, role checks, uploads
│   ├── 📂 models/           # Mongoose schemas (User, Job, Application, etc.)
│   ├── 📂 routes/           # API endpoints
│   ├── 📂 utils/            # AI services, PDF parsing, validators
│   ├── server.js            # Main server file
│   └── .env                 # Environment variables
│
├── 📂 frontend/
│   ├── 📂 public/           # Static assets
│   ├── 📂 src/
│   │   ├── 📂 components/   # Reusable UI components
│   │   ├── 📂 context/      # React Context (Auth, Socket)
│   │   ├── 📂 pages/        # Page components
│   │   ├── App.js           # Main app component
│   │   └── index.js         # React entry point
│   └── .env                 # Environment variables
│
└── README.md
```

---

## 🔧 Configuration

### MongoDB Setup

**Local MongoDB:**
```bash
# Start MongoDB
mongod --dbpath /path/to/data

# Connection string
MONGODB_URI=mongodb://localhost:27017/job-portal
```

**MongoDB Atlas:**
1. Create free cluster at [mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
2. Get connection string
3. Update `MONGODB_URI` in `.env`

### API Keys (Optional)

#### Google Gemini
1. Visit [ai.google.dev](https://ai.google.dev)
2. Get API key
3. Add to `.env`: `GEMINI_API_KEY=your_key`

#### Groq
1. Visit [console.groq.com](https://console.groq.com)
2. Get API key
3. Add to `.env`: `GROQ_API_KEY=your_key`

#### Google OAuth
1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Create OAuth 2.0 credentials
3. Add authorized redirect: `http://localhost:5000/api/auth/google/callback`
4. Add to `.env`:
   ```
   GOOGLE_CLIENT_ID=your_id
   GOOGLE_CLIENT_SECRET=your_secret
   ```

---

## 🐛 Troubleshooting

### Common Issues

**❌ MongoDB Connection Failed**
```bash
# Check if MongoDB is running
mongod --version

# Check connection string in .env
MONGODB_URI=mongodb://localhost:27017/job-portal
```

**❌ CORS Errors**
```javascript
// backend/server.js - Verify CORS config
app.use(cors({
  origin: process.env.FRONTEND_URL,
  credentials: true
}));
```

**❌ JWT Authentication Fails**
```env
# Ensure JWT_SECRET is set in .env
JWT_SECRET=your-secret-key-minimum-32-chars
```

**❌ AI Features Not Working**
- AI features work without API keys (fallback mode)
- Check console for specific error messages
- Verify PDF upload format (base64 encoding)

---

## 🤝 Contributing

We welcome contributions! Here's how:

1. **🐛 Report Bugs**: Open an issue with detailed description
2. **✨ Suggest Features**: Share your ideas and use cases
3. **🔧 Submit PRs**: Fork → Create feature branch → Submit PR
4. **📖 Improve Docs**: Fix typos, add examples, create tutorials

---



## 📧 Contact

**Developer**: Himani Mahajan  
**Email**: himanimahajan2709@gmail.com  
**GitHub**: [himaniMahajan27](https://github.com/himaniMahajan27)

---

<div align="center">

### ⭐ Star us on GitHub!

Made with ❤️ by Himani Mahajan


</div>
