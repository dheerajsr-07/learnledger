# AI-Powered Resume Parser Engine

Full-stack resume parser web app with a white and green UI theme, animated alien logo, JWT authentication, resume uploads, parser/ATS analysis, dashboard analytics, jobs, templates, notifications, profile, settings, and admin screens.

## Stack

- Frontend: React + Vite + custom CSS
- Backend: Node.js + Express
- Database: MongoDB
- Auth: JWT + bcrypt
- Uploads: Multer
- Parsing: `pdf-parse`, `mammoth`, and heuristic AI-ready parsing services

## Run Locally

```bash
npm install
cp server/.env.example server/.env
npm run dev
```

Frontend: `http://localhost:5173`

Backend: `http://localhost:5000`

For the file-open static website, open `index.html`. If the backend is running on port `5000`, login/register/upload will use the backend automatically; if it is not running, the browser-only local demo still works.

On Windows PowerShell, use `npm.cmd` if `npm.ps1` is blocked:

```bash
npm.cmd install
npm.cmd run start --workspace server
```

## Backend APIs

- `GET /api/health`
- `POST /api/auth/register`
- `POST /api/auth/login`
- `POST /api/resumes/upload`
- `GET /api/resumes`
- `GET /api/ats`
- `GET /api/jobs`
- `GET /api/notifications`
- `GET /api/users/me`
- `GET /api/admin/stats`

## Environment

Set these values in `server/.env`:

```bash
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/resume_parser_engine
JWT_SECRET=change_this_secret
CLIENT_URL=http://localhost:5173
```

Leave `MONGO_URI` empty for in-memory development mode, or set a MongoDB Atlas/local MongoDB URI for real persistence.

## Deployment

- Frontend: Vercel (`client`)
- Backend: Render (`server`)
- Database: MongoDB Atlas
