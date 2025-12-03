# Lets Chat – MERN Real‑Time Chat Platform

A full‑stack real‑time messaging application with secure authentication, online presence, typing indicators, emoji support, and media/file sharing.

- Live Demo: https://letschatapp-3jfz.onrender.com
- Repository: https://github.com/ranjeety8840/Lets_chat

## Features
- Real‑time 1:1 and group chat using Socket.IO
- Online presence and typing indicators
- Secure auth with JWT, bcrypt hashing, and cookie sessions
- Media/file upload via Multer + Cloudinary
- Responsive UI with React, Tailwind CSS, and emoji picker
- State management with Redux Toolkit and routing via React Router
- RESTful API with Express and MongoDB (Mongoose)

## Tech Stack
- Frontend: React (Vite), Redux Toolkit, React Router, Tailwind CSS, Axios, emoji‑picker‑react
- Backend: Node.js, Express, Socket.IO, Mongoose, Multer, Cloudinary, JWT, cookie‑parser, CORS, dotenv
- Database: MongoDB (Atlas or local)
- Deployment: Render (backend), Vercel/Netlify (frontend)

## Monorepo Structure
```
Lets_chat/
├─ backend/
│  ├─ index.js
│  ├─ src/... (controllers, models, routes)
│  └─ package.json
└─ frontend/
   ├─ src/
   └─ package.json
```

## Prerequisites
- Node.js 18+
- MongoDB Atlas account (recommended) or local MongoDB
- Cloudinary account (for media uploads)

## Environment Variables
Create a `.env` file in `backend/`:
```
# Server
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI="your_mongodb_connection_string"

# Auth
JWT_SECRET="a_strong_random_secret"
JWT_EXPIRES_IN="7d"

# CORS / Client
CLIENT_URL="http://localhost:5173"

# Cloudinary
CLOUDINARY_CLOUD_NAME="your_cloud_name"
CLOUDINARY_API_KEY="your_api_key"
CLOUDINARY_API_SECRET="your_api_secret"
```

Create a `.env` (or `.env.local`) in `frontend/` for Vite:
```
VITE_API_URL="http://localhost:5000"
VITE_SOCKET_URL="http://localhost:5000"
# If used in the UI for direct image transformations
VITE_CLOUDINARY_CLOUD_NAME="your_cloud_name"
```

## Local Development
1) Install dependencies
```
# Backend
cd backend
npm install

# Frontend (in a new terminal)
cd frontend
npm install
```

2) Start the servers
```
# Backend (http://localhost:5000)
npm run dev

# Frontend (http://localhost:5173)
npm run dev
```

3) Update environment variables with your own values.

## Build
```
# Frontend production build
cd frontend
npm run build

# Serve preview (optional)
npm run preview
```

## Deployment
### Backend (Render)
- Create a new Web Service on Render
- Connect repo and select `backend/` as root
- Build Command: `npm install`
- Start Command: `node index.js`
- Add Environment Variables from backend `.env`
- Set `PORT` to the Render provided value (Render sets it automatically)

### Frontend (Vercel or Netlify)
- Vercel: import the repo, set `frontend/` as root
  - Build Command: `npm run build`
  - Output Directory: `dist`
  - Env: `VITE_API_URL` set to your deployed backend URL
- Netlify: same values as above


## Scripts
- Backend
  - `npm run dev` – start Express with nodemon
- Frontend
  - `npm run dev` – start Vite dev server
  - `npm run build` – production build
  - `npm run preview` – preview production build

## Roadmap
- Message read receipts
- Push notifications
- Better group admin controls



