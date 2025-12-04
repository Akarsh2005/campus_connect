# 🎓 Campus Connect

A comprehensive **college communication platform** designed to unify interactions between **students**, **faculty**, **HODs**, and **alumni**.
Campus Connect streamlines messaging, assignments, attendance, announcements, and alumni-driven opportunities — all with **role-based access control**.

---

## 📋 Table of Contents

* [Features](#-features)
* [Tech Stack](#-tech-stack)
* [Project Structure](#-project-structure)
* [Prerequisites](#-prerequisites)
* [Installation](#-installation)
* [Configuration](#-configuration)
* [Running the Application](#-running-the-application)
* [Available Scripts](#-available-scripts)
* [API Documentation](#-api-documentation)
* [Testing](#-testing)
* [Authentication & Authorization](#authentication--authorization)
* [Database Models](#-database-models)

---

## ✨ Features

### 🎓 **Student & Academic Communication**

* Real-time messaging with faculty & classmates
* Access assignments, grades, attendance & announcements
* Raise academic queries and receive responses

### 👩‍🏫 **Faculty Tools**

* Create/manage assignments
* Track attendance
* Respond to student queries
* Post department announcements

### 🧑‍💼 **HOD & Admin Features**

* Manage departments, faculty, and student groups
* Oversee system-wide communication
* View analytics and activity logs

### 🎓 **Alumni Portal**

* Alumni can **share job opportunities**, internships & referrals
* Provide **career guidance** to students
* Participate in **discussion groups**
* Post **mentorship sessions** and Q&A
* Allow students to reach out to alumni securely
* Create alumni-specific announcements & events

### 🌐 **Global Features**

* Hierarchy-based group access
* JWT authentication
* Secure role-based authorization
* MongoDB scalable data models
* Department + course grouping
* Responsive and user-friendly interface

---

## 🛠 Tech Stack

### **Backend**

* Node.js, Express.js
* MongoDB (Mongoose)
* JWT authentication
* bcryptjs password hashing

### **Frontend**

* React.js
* React Router v7
* Axios
* Bootstrap 5 & React Bootstrap
* React Scripts (CRA)

---

## 📁 Project Structure

```
campus_connect/
├── Backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── scripts/
│   ├── tests/
│   ├── utils/
│   └── server.js
├── Frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── context/
│       ├── pages/
│       ├── services/
│       ├── styles/
│       ├── utils/
│       ├── App.jsx
│       └── index.js
├── scripts/
├── seeds/
├── package.json
└── vercel.json
```

---

## 📦 Prerequisites

* Node.js v14+
* npm or yarn
* MongoDB (local or Atlas)
* Git

---

## 🚀 Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Akarsh2005/campus_connect.git
cd campus_connect
```

### 2️⃣ Install dependencies

```bash
npm run install-all
```

Or install manually:

```bash
npm run install-backend
npm run install-frontend
```

---

## ⚙️ Configuration

### Backend `.env`

```env
PORT=5000
NODE_ENV=development

MONGODB_URI="your mongodb string"

JWT_SECRET=your_jwt_secret_key
CORS_ORIGIN=http://localhost:3001
```

### Frontend

Configure proxy or update API URLs in:

```
Frontend/src/services/api.js
```

---

## ▶️ Running the Application

### Full Development Mode

```bash
npm run dev
```

Runs **backend + frontend** concurrently.

### Backend Only

```bash
npm run server
```

### Frontend Only

```bash
npm run client
```

### Production Mode

```bash
npm start
```

---

## 📜 Available Scripts

### Installation

```
npm run install-backend
npm run install-frontend
npm run install-all
```

### Development

```
npm run dev
npm run client
npm run server
```

### Testing

```
npm run test
npm run test:watch
npm run test:memory
npm run test:atlas
```

---

## 📚 API Documentation

### 🔐 Authentication

* `POST /api/auth/register`
* `POST /api/auth/login`
* `POST /api/auth/logout`

### 👤 User Management

* `GET /api/users`
* `GET /api/users/:id`
* `PUT /api/users/:id`
* `DELETE /api/users/:id`

### 📘 Assignments

* `GET /api/assignments`
* `POST /api/assignments`
* `GET /api/assignments/:id`
* `PUT /api/assignments/:id`
* `DELETE /api/assignments/:id`

### 📨 Messaging

* `GET /api/messages`
* `POST /api/messages`
* `GET /api/messages/:id`

### 🧾 Attendance

* `GET /api/attendance`
* `POST /api/attendance`
* `PUT /api/attendance/:id`

### 🧑‍🤝‍🧑 Groups

* `GET /api/groups`
* `POST /api/groups`
* `GET /api/groups/:id`
* `PUT /api/groups/:id`

### 🎓 Alumni

* `GET /api/alumni/opportunities` – Job opportunities
* `POST /api/alumni/opportunities` – Alumni submit opportunities
* `GET /api/alumni/guidance` – Guidance posts
* `POST /api/alumni/guidance` – Alumni publish guidance

### ❓ Queries

* `GET /api/queries`
* `POST /api/queries`
* `GET /api/queries/:id`
* `POST /api/queries/:id/respond`

---

---

## 🔐 Authentication & Authorization

Campus Connect supports 4 roles:

| Role    | Capabilities                                  |
| ------- | --------------------------------------------- |
| Student | Assignments, queries, groups, alumni guidance |
| Faculty | Assignments, attendance, messaging            |
| HOD     | Department management                         |
| Alumni  | Opportunities, mentorship, guidance           |

Tokens are stored in **localStorage** and verified via middleware.

---

## 📊 Database Models

* **User**
* **Assignment**
* **Submission**
* **Message**
* **Group**
* **Query**
* **Attendance**
* **Grade**
* **AlumniOpportunity**
* **AlumniGuidance**

---

## 🤝 Contributing

1. Fork
2. Create feature branch
3. Commit & push
4. Open PR

---


