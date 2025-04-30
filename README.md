
markdown
Copy
Edit
# Public Speaking Franchise/Club Management System

## 📌 One-Line Summary
A Franchise and Club Management System for a company focused on teaching public speaking.

---

## 📖 Project Description

This project is a comprehensive full-stack **Franchise and Club Management System** designed for a public speaking education company. The platform enables smooth administration and monitoring of clubs and franchise centers that operate across different cities and states.

It facilitates centralized control over club creation, member registration, and admin assignments, allowing efficient scaling and streamlined data access. Club admins can manage speaker data and organizational details through a secure, role-based interface.

Built using **Next.js** for the frontend and **Django REST Framework** for the backend, this system ensures seamless data handling, modern UI/UX, and secure access control via session-based authentication.

---

## ⚙️ Technologies Used

### Frontend
- **Next.js**
- **React**
- **Tailwind CSS** (optional)
- **React Context API**

### Backend
- **Django**
- **Django REST Framework (DRF)**
- **SQLite** (default) / **PostgreSQL**
- **Session Auth + CSRF**

---

## 🔐 Features

### 🔒 Admin Login System
- Secure login and logout for admins
- Session & CSRF protected authentication

### 🏢 Club & Franchise Management
- Create new clubs with city/state/postal/country details
- Edit and delete existing clubs

### 👤 Member Handling
- View all members by club
- Update member details (e.g., name, club assignment)
- Search/filter functionality

### 🛡️ Admin Dashboard
- View and manage all system admins
- Assign or revoke admin privileges

---

## 🧱 API Endpoints

- `POST /api/accounts/login/` – Admin login
- `POST /api/accounts/logout/` – Logout
- `GET /api/accounts/clubs/` – List all clubs
- `POST /api/accounts/clubs/` – Add new club
- `PUT /api/accounts/clubs/:id/` – Update club
- `GET /api/accounts/members/` – Fetch all members
- `PUT /api/accounts/members/:username/` – Update member
- `GET /api/accounts/admins/` – Get admin list

---

## 🚀 Getting Started

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
Backend Setup
bash
Copy
Edit
cd backend
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
Important Django Settings
python
Copy
Edit
CORS_ALLOWED_ORIGINS = ["http://localhost:3000"]
CSRF_TRUSTED_ORIGINS = ["http://localhost:3000"]
🧪 Test Workflow
Log in as an admin.

Create a new club using city/state/postal info.

Add or update members in the club.

Assign other users as admins.

View and test all functionalities in the admin dashboard.
