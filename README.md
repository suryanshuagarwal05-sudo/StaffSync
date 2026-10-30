# StaffSync — HR Management System (MERN Stack)

**StaffSync** is a full-stack Human Resource Management System built using the MERN stack (MongoDB, Express.js, React.js, and Node.js). It helps organizations manage employees, attendance, leave requests, and workplace announcements through a centralized dashboard.

## 🌐 Live Application

**Visit StaffSync:** https://staffsyncnccc-iskelnjd6-000-bb72.vercel.app

**Backend API Health Check:** https://staffsync-backend-pwf1.onrender.com/api/health

Frontend is deployed on **Vercel**, backend on **Render**, and the database is hosted on **MongoDB Atlas**.

## 🚀 Features

- **Authentication:** User registration and login with JWT authentication.
- **Role-Based Access:** Three user roles:
  - `hr`
  - `manager`
  - `employee`
- **Employee Management:** Employee directory accessible to HR/admin users.
- **Attendance Management:** Check-in, check-out, and attendance history.
- **Leave Management:** Submit leave requests and manage approval or rejection workflows.
- **Announcements:** HR can publish announcements, and signed-in users can view them.
- **Dashboard:** Centralized interface for HR and employees.
- **API Health Check:** Endpoint to monitor backend availability.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| React.js | Frontend user interface |
| Node.js | Backend runtime |
| Express.js | REST API and server |
| MongoDB Atlas | Cloud database |
| Mongoose | MongoDB object modeling |
| JWT | Authentication |
| Vercel | Frontend deployment |
| Render | Backend deployment |

## 💻 Run Locally

### Prerequisites

- Node.js LTS
- npm
- MongoDB local installation or MongoDB Atlas account
- Visual Studio Code (recommended)
- Git

### 1. Clone the repository

```bash
git clone https://github.com/suryanshuagarwal05-sudo/StaffSync.git
```

Navigate into the project:

```bash
cd StaffSync
```

### 2. Configure the backend

Navigate to the server folder:

```bash
cd server
```

Install dependencies:

```bash
npm install
```

Create a `.env` file using `.env.example` as a reference.

Configure your environment variables:

```env
PORT=5001
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_long_random_secret
CLIENT_ORIGIN=http://localhost:5173
```

Use your own MongoDB connection string and a strong, randomly generated JWT secret. Never commit your `.env` file to GitHub.

Start the backend:

```bash
npm run dev
```

Backend health check:

http://localhost:5001/api/health

### 3. Configure the frontend

Open a second Terminal window and navigate to the client folder:

```bash
cd client
```

Install dependencies:

```bash
npm install
```

Create a `.env` file and configure:

```env
VITE_API_URL=http://localhost:5001/api
```

Start the frontend:

```bash
npm run dev
```

Open the local Vite URL displayed in your Terminal, usually:

http://localhost:5173

If Vite uses a different port, update `CLIENT_ORIGIN` in the backend `.env` file to match the frontend origin and restart the backend.

## ☁️ Deployment Architecture

StaffSync is deployed using the following services:

| Component | Hosting Service |
|---|---|
| Frontend | Vercel |
| Backend | Render |
| Database | MongoDB Atlas |
| Source Code | GitHub |

### Production Environment Variables

**Render Backend:**

```env
MONGODB_URI=your_mongodb_atlas_uri
JWT_SECRET=your_secure_random_secret
CLIENT_ORIGIN=your_vercel_frontend_url
```

**Vercel Frontend:**

```env
VITE_API_URL=your_render_backend_url/api
```

Configure these values in the respective hosting dashboards. Never expose database credentials or JWT secrets in frontend code.

## 👥 User Roles

| Role | Access |
|---|---|
| HR | Employee management, announcements, and leave management |
| Manager | Managerial leave decision workflow |
| Employee | Attendance, leave requests, and announcements |

For this MVP, role selection is available during registration for local demonstration purposes.

**Security note:** Before production use, remove public HR role selection and provision HR accounts securely.

## ⚠️ Project Limitations

StaffSync is currently a functional portfolio/demo MVP and is not intended to be used as production-ready HR software.

Further improvements recommended:

- Comprehensive automated testing.
- Secure HR account provisioning.
- Audit logs and activity tracking.
- Email verification.
- Password reset functionality.
- Policy-aware leave balances.
- CSRF protections if cookie-based authentication is introduced.
- Security review and stronger production authentication practices.

The current demo stores JWT tokens in browser `localStorage` for simplicity.

## 📁 Project Structure

```text
StaffSync/
│
├── client/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── .env.example
│
├── server/
│   ├── src/
│   ├── package.json
│   └── .env.example
│
├── README.md
└── package-lock.json
```

## 👨‍💻 Developer

**Project:** StaffSync — HR Management System  
**Architecture:** MERN Stack  
**Deployment:** Vercel + Render + MongoDB Atlas

---

⭐ If you find this project useful, consider giving the repository a star!

**Live Demo:** https://staffsyncnccc-iskelnjd6-000-bb72.vercel.app

**GitHub Repository:** https://github.com/suryanshuagarwal05-sudo/StaffSync
