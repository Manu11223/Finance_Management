# Finance Hive - Finance Management Application

A full-stack finance/chit fund management web application for lenders, borrowers, and administrators to manage financial accounts, track loans, record transactions, and generate analytics.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18, Ant Design, Recharts |
| **Backend** | Python FastAPI, SQLAlchemy |
| **Database** | PostgreSQL |
| **Auth** | JWT (HS256) + bcrypt |
| **Deployment** | Frontend on Vercel, Backend on Render.com |

## Features

### Admin Dashboard
- Add and manage admins
- View all lenders and borrowers
- Edit/delete admin records

### Lender Dashboard
- Registration & login
- Dashboard analytics with charts (bar, pie, line)
- Add and manage customers
- Record credit/debit transactions
- View customer details with search/sort
- Transaction history with CSV export

### Borrower Dashboard
- View lender listings

## Getting Started

### Prerequisites
- Node.js
- Python 3.10+
- PostgreSQL

### Frontend Setup
```bash
cd client
npm install
npm start
```

### Backend Setup
```bash
cd server
python -m venv .venv
.venv\Scripts\activate  # Windows
pip install -r requirements.txt
python main.py
```

### Backend (Node.js - stub)
```bash
cd server
npm install
npm run dev
```

## Environment Variables

### client/.env
```
REACT_APP_API_URL=https://finance-backend-8qum.onrender.com
```

### server/.env (create if not exists)
```
DATABASE_URL=postgresql://postgres:password@localhost/finance-hive
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/signup` | User registration |
| POST | `/login` | User login |
| POST | `/customers` | Add customer |
| GET | `/customers` | List customers |
| POST | `/transactions` | Add transaction |
| GET | `/dashboard` | Dashboard stats |

Default admin credentials: `admin@financehive.com` / `admin123`
