# Club Admin Panel

## 📌 One-Line Summary
A full-stack admin panel for managing clubs, members, and admins using Next.js and Django REST Framework.

---

## 📖 Project Description

This project is a comprehensive **Club Administration Platform** designed to manage multiple clubs, their respective members, and administrators. It offers an intuitive web interface (built with **Next.js**) backed by a powerful REST API (built using **Django REST Framework**). The system is ideal for educational institutions or organizations that need structured control over club operations, member data, and access management.

This project provides all essential CRUD (Create, Read, Update, Delete) operations for club entities and their members, with secure, role-based access. Admins can be added or removed, clubs can be registered with detailed information, and members can be updated as per organizational hierarchy.

---

## ⚙️ Technologies Used

### Frontend
- **Next.js** — for building a fast, server-rendered React frontend
- **React Hooks & Context API** — for state management
- **Tailwind CSS** — for responsive and clean UI styling (optional but assumed)

### Backend
- **Django** — as the web framework
- **Django REST Framework (DRF)** — for API development
- **Session Authentication** — using Django’s default session-based login system
- **CORS Headers & CSRF** — for secure cross-origin communication between frontend and backend

---

## 🔐 Features

### 🔒 Authentication
- Login and Logout using Django session-based authentication
- Cookie-based session handling with CSRF protection

### 👥 Member Management
- Add, update, and delete club members
- Fetch all members or filter them by specific clubs

### 🏢 Club Management
- Create new clubs with details like name, address, city, postal code, etc.
- List all clubs or update specific ones
- Delete clubs if needed

### 🛡️ Admin Management
- Add or remove admins
- View all registered admins
- Prevent unauthorized access with backend authentication

### 📦 API Routes (Backend)
- `POST /api/accounts/login/` – Log in an admin
- `POST /api/accounts/logout/` – Log out
- `GET /api/accounts/members/` – List members
- `PUT /api/accounts/members/:username/` – Update a member
- `POST /api/accounts/clubs/` – Create a club
- `GET /api/accounts/clubs/` – List all clubs
- `PUT /api/accounts/clubs/:id/` – Update club info
- `GET /api/accounts/admins/` – Get all admins

### 🌐 API Requests (Frontend)
- All requests use the `fetch` API with `credentials: 'include'` to support cookie-based sessions
- Full error handling and status-based messages

---

## 🛠️ Setup Instructions

### Prerequisites
- Node.js (>= 14)
- Python (>= 3.8)
- Django and DRF installed (`pip install -r requirements.txt`)
- A PostgreSQL or SQLite database (optional config)

### Frontend (Next.js)
```bash
cd frontend
npm install
npm run dev
Backend (Django)
bash
Copy
Edit
cd backend
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
Notes
Ensure CORS is correctly set in Django settings:

python
Copy
Edit
CORS_ALLOWED_ORIGINS = [
    "http://localhost:3000",
]
CSRF_TRUSTED_ORIGINS = [
    "http://localhost:3000",
]
🧪 Testing
Login through the Next.js frontend with a valid admin account

Try creating a new club and adding members

Use the developer console to track fetch requests and test error handling

Use Django admin panel (/admin) for debugging or superuser actions
