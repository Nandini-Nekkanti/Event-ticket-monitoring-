Event Ticket Monitoring System

A very simple project where you can create events, track total tickets, buy tickets, and view basic metrics.

This project contains:

Backend → Node.js + Express

Frontend → HTML + JavaScript

Metrics → /metrics endpoint

Data stored in-memory (no database needed)

🚀 How to Run (Easiest Way – Without Docker)
✅ 1. Start Backend

Open PowerShell / CMD

Go to backend folder:

cd backend


Install dependencies:

npm install


Start backend:

node index.js


You should see:

Backend running on http://localhost:4000

✅ 2. Start Frontend

Option A — using Python (recommended):

cd frontend
python -m http.server 3000


Open:

http://localhost:3000


Option B — open index.html directly

Go to the frontend folder

Double-click index.html

Option C — using Node:

cd frontend
npx serve -l 3000

🔧 API Endpoints (Backend)
➤ Create event
POST /api/events
Body:
{
  "name": "Event1",
  "total": 10
}

➤ List events
GET /api/events

➤ Buy a ticket
POST /api/events/:id/buy

➤ Metrics
GET /metrics


Example output:

etm_total_events 1
etm_total_sold 3

🌐 Frontend Usage

Enter:

Event name

Total tickets

Click Create Event

Click Buy to increase sold count

Metrics refresh automatically

📁 Project Structure
project/
│
├── backend/
│   ├── index.js
│   ├── package.json
│   └── Dockerfile
│
├── frontend/
│   ├── index.html
│   └── Dockerfile
│
└── docker-compose.yml

🐳 Running With Docker (Optional)

Make sure Docker Desktop is running, then:

Go to project root:

cd project-folder


Run:

docker compose up --build


Open:

Frontend → http://localhost:3000

Backend → http://localhost:4000

Metrics → http://localhost:4000/metrics

✔️ Requirements

Node.js installed

(Optional) Python installed for simple static server

(Optional) Docker Desktop installed

📦 Features

Event creation

Ticket purchase

Real-time ticket updates

Basic monitoring metrics

Very lightweight (no database)
