<<<<<<< HEAD
# 🕐 AttendEase - Employee Attendance System

A full-stack Employee Attendance Management System built with the MERN stack (MongoDB, Express.js, React, Node.js).

## 📋 Project Information

<<<<<<< HEAD
- **Name:** [Sreeja Alle]
- **College:** [Vignan's lara institute of technology and science]
- **Contact:** [+91 7288 848 108]
=======
- **Name:** Alle Sreeja
- **College:** Vignan's Lara Institute of Technology and Science.
- **Contact:** 7288848108
>>>>>>> d1a4e26c5a3e98b2059f8a4b2992a9f0d39981f7
- **Project:** SDE Internship Task - Tap Academy

---

## 🚀 Features

### Employee Features
- ✅ Register/Login with secure authentication
- ✅ Mark daily attendance (Check In / Check Out)
- ✅ View attendance history (Calendar & Table view)
- ✅ View monthly summary (Present/Absent/Late/Half-day)
- ✅ Interactive dashboard with stats
- ✅ Profile management

### Manager Features
- ✅ Secure login with role-based access
- ✅ View all employees' attendance
- ✅ Filter by employee, date, status, department
- ✅ View team attendance summary
- ✅ Team calendar view
- ✅ Export attendance reports (CSV)
- ✅ Dashboard with team stats & charts

---

## 🛠️ Tech Stack

### Frontend
- **React 18** - UI Library
- **Zustand** - State Management (lightweight alternative to Redux)
- **React Router v6** - Navigation
- **Tailwind CSS** - Styling
- **Recharts** - Charts & Visualizations
- **React Hot Toast** - Notifications
- **date-fns** - Date formatting
- **Axios** - HTTP Client

### Backend
- **Node.js** - Runtime Environment
- **Express.js** - Web Framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **JWT** - Authentication
- **bcryptjs** - Password Hashing
- **json2csv** - CSV Export

---

## 📁 Project Structure

```
employee-attendance-system/
├── backend/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── attendanceController.js
│   │   └── dashboardController.js
│   ├── middleware/
│   │   └── auth.js
│   ├── models/
│   │   ├── User.js
│   │   └── Attendance.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── attendanceRoutes.js
│   │   └── dashboardRoutes.js
│   ├── .env.example
│   ├── package.json
│   ├── seed.js
│   └── server.js
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   └── layout/
│   │   ├── pages/
│   │   │   ├── auth/
│   │   │   ├── employee/
│   │   │   └── manager/
│   │   ├── redux/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── .env.example
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

## ⚙️ Environment Variables

### Backend (.env)
```env
MONGODB_URI=mongodb+srv://your-username:your-password@cluster.mongodb.net/attendance-system
JWT_SECRET=your-super-secret-jwt-key-change-this
JWT_EXPIRE=7d
PORT=5000
NODE_ENV=development
FRONTEND_URL=http://localhost:5173
```

### Frontend (.env)
```env
VITE_API_URL=http://localhost:5000/api
```

---

## 🚀 How to Run

### Prerequisites
- Node.js (v18 or higher)
- MongoDB Atlas account or local MongoDB installation
- npm or yarn

### Backend Setup

1. Navigate to backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file from example:
```bash
cp .env.example .env
```

4. Update `.env` with your MongoDB URI and JWT secret

5. Seed the database with sample data:
```bash
npm run seed
```

6. Start the server:
```bash
npm run dev
```

Server will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file from example:
```bash
cp .env.example .env
```

4. Start the development server:
```bash
npm run dev
```

Application will run on `http://localhost:5173`

---

## 🔐 Test Credentials

After running the seed script, you can use these credentials:

| Role | Email | Password |
|------|-------|----------|
| Manager | manager@company.com | password123 |
| Employee | alice@company.com | password123 |
| Employee | bob@company.com | password123 |

---

## 📡 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/auth/me` | Get current user |
| PUT | `/api/auth/profile` | Update profile |

### Attendance (Employee)
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/attendance/checkin` | Check in |
| POST | `/api/attendance/checkout` | Check out |
| GET | `/api/attendance/today` | Today's status |
| GET | `/api/attendance/my-history` | Attendance history |
| GET | `/api/attendance/my-summary` | Monthly summary |

### Attendance (Manager)
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/attendance/all` | All employees attendance |
| GET | `/api/attendance/employee/:id` | Specific employee |
| GET | `/api/attendance/summary` | Team summary |
| GET | `/api/attendance/today-status` | Today's team status |
| GET | `/api/attendance/export` | Export CSV |

### Dashboard
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/dashboard/employee` | Employee stats |
| GET | `/api/dashboard/manager` | Manager stats |
| GET | `/api/dashboard/employees` | All employees list |

---

## 📸 Screenshots

### Login Page
![Login Page](screenshcdots/login.png)

### Employee Dashboard
![Employee Dashboard](screenshots/employee-dashboard.png)

### Mark Attendance
![Mark Attendance](screenshots/mark-attendance.png)

### Attendance History
![Attendance History](screenshots/attendance-history.png)

### Manager Dashboard
![Manager Dashboard](screenshots/manager-dashboard.png)

### All Employees Attendance
![All Attendance](screenshots/all-attendance.png)

### Team Calendar
![Team Calendar](screenshots/team-calendar.png)

### Reports & Export
![Reports](screenshots/reports.png)

---

## 🎯 Key Features Explained

### Attendance Status Logic
- **Present**: Check-in within 15 minutes of standard time (9:00 AM)
- **Late**: Check-in between 15 minutes to 2 hours late
- **Half-Day**: Check-in more than 2 hours late
- **Absent**: No check-in recorded

### Role-Based Access
- **Employees** can only access their own data
- **Managers** have access to all employee data and reports

### Calendar Color Coding
- 🟢 Green - Present
- 🔴 Red - Absent
- 🟡 Yellow - Late
- 🟠 Orange - Half Day

---

## 🔧 Deployment

### Backend (Render/Railway)
1. Create a new Web Service
2. Connect your GitHub repository
3. Set environment variables
4. Deploy

### Frontend (Vercel/Netlify)
1. Import your repository
2. Set build command: `npm run build`
3. Set output directory: `dist`
4. Add environment variables
5. Deploy

---

## 📝 License

This project is created for educational purposes as part of the SDE Internship task.

---

## 🙏 Acknowledgments

- Tap Academy for providing this opportunity
- All open-source libraries used in this project

---


=======
# Attendance-system
Attenadnce System
>>>>>>> 46a9f1a5f551748b891ecc9aad6ea0e9b9c9e9e2
