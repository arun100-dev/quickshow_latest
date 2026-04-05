# 🎬 QuickShow — Movie Ticket Booking System

<div align="center">

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-quickshow--latest.vercel.app-6D28D9?style=for-the-badge)](https://quickshow-latest.vercel.app)

</div>

---

## 📌 Overview

**QuickShow** is a full-stack movie ticket booking web application that supports both **user** and **admin** workflows. Users can browse movies, select seats, and book tickets — while admins can manage movies, shows, and bookings through a protected dashboard.

Built with the **MERN stack**, this project focuses on real-world engineering concerns: secure authentication, role-based access control, RESTful API design, and clean component architecture.

---

## ✨ Features

### 👤 User Side
- Browse available movies and shows
- Interactive seat selection with real-time availability
- Secure user registration & login (JWT-based)
- View and manage personal booking history

### 🛠️ Admin Side
- Protected admin dashboard (role-based access)
- Add, update, and delete movies & shows
- View all bookings across the platform

---

## 🏗️ System Architecture

```
quickshow_latest/
├── client/               # React frontend
│   ├── src/
│   │   ├── components/   # Reusable UI components
│   │   ├── pages/        # Route-level page components
│   │   ├── context/      # Global state via Context API
│   │   └── utils/        # Helpers & API call functions
│   └── ...
│
└── server/               # Node.js + Express backend
    ├── controllers/      # Route handler logic
    ├── middleware/        # Auth & role-based guards
    ├── models/            # Mongoose schemas
    ├── routes/            # API route definitions
    └── ...
```

---

## ⚙️ Engineering Highlights

### 🔐 Authentication & Authorization
- Stateless **JWT authentication** — tokens issued on login, verified via middleware
- **Role-based access control (RBAC)** — user vs admin roles enforced at the API level
- Protected routes on both frontend (React Router guards) and backend (middleware)

### 🎭 Seat Booking Logic
- Seat selection UI with live availability state
- Booking validation to prevent double-booking of the same seat
- Atomic booking flow — seat status updated only on confirmed payment

### 🌐 REST API Design
- Clean, resource-based URL structure (`/api/movies`, `/api/bookings`, etc.)
- Input validation and structured error responses on all endpoints
- Separation of concerns: routes → controllers → models

### 🧩 Frontend Architecture
- Built with **React Hooks** for local state management
- **Context API** for global auth state (user session, role)
- **React Router** for client-side navigation with protected route wrappers
- Fully **reusable component structure** — no duplicated UI logic

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React, React Router, Context API, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Auth | JWT (JSON Web Tokens) |
| Deployment | Vercel (Frontend), Render / Railway (Backend) |

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- MongoDB (local or Atlas)

### 1. Clone the repository
```bash
git clone https://github.com/arun100-dev/quickshow_latest.git
cd quickshow_latest
```

### 2. Setup the Backend
```bash
cd server
npm install
```

Create a `.env` file inside `/server`:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

```bash
npm start
```

### 3. Setup the Frontend
```bash
cd ../client
npm install
npm run dev
```

The app will run at `http://localhost:5173`

---

## 🔑 Environment Variables

| Variable | Description |
|---|---|
| `MONGO_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret key for signing JWT tokens |
| `PORT` | Port for the Express server (default: 5000) |

---

## 🧠 What I Learned

- How to implement **stateless authentication** with JWT and protect routes by role
- Designing a **MongoDB schema** that handles users, movies, shows, and bookings with references
- Managing **frontend state** across pages using Context API without Redux
- Structuring a **full-stack project** with clean separation between client and server
- Handling **real-world edge cases** like concurrent seat booking and invalid inputs

---

## 📫 Author

**Arun Sharma**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/arun-sharma-1bb097318)
[![Gmail](https://img.shields.io/badge/Gmail-janyalarun%40gmail.com-EA4335?style=flat-square&logo=gmail)](mailto:janyalarun@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-arun100--dev-181717?style=flat-square&logo=github)](https://github.com/arun100-dev)

---

<div align="center">

⭐ If you found this project useful, consider giving it a star!

</div>
