# QR-Based Lead Capture System (Coaching Center)

Production-ready full-stack lead capture application with QR form access and admin lead listing.

## Tech Stack
- Frontend: React + Bootstrap (Vite)
- Backend: Node.js + Express.js (REST API)
- Database: MongoDB + Mongoose

## Project Structure

```
.
├── backend
│   ├── src
│   │   ├── config
│   │   ├── controllers
│   │   ├── middleware
│   │   ├── models
│   │   ├── routes
│   │   ├── app.js
│   │   └── server.js
│   └── .env.example
├── frontend
│   ├── src
│   │   ├── api
│   │   ├── components
│   │   ├── pages
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── .env.example
└── package.json
```

## Setup

### 1) Install dependencies
```bash
npm run install:all
```

### 2) Configure environment variables

Backend:
```bash
cp backend/.env.example backend/.env
```

Frontend:
```bash
cp frontend/.env.example frontend/.env
```

### 3) Run backend
```bash
npm run dev:backend
```

### 4) Run frontend
```bash
npm run dev:frontend
```

## URLs
- Frontend: `http://localhost:3000` (Vite default may be 5173)
- Backend API: `http://localhost:5000/api`
- Lead form route: `/form`
- Admin lead list route: `/admin`

## REST API

### POST `/api/leads`
Create a new lead.

Payload:
```json
{
  "name": "Aarav Sharma",
  "mobile": "9876543210",
  "courseInterest": "JEE"
}
```

### GET `/api/leads`
Fetch all leads for admin view.

### GET `/api/health`
Health check endpoint.
