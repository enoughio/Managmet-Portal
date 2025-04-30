
markdown
Copy
Edit
# Public Speaking Franchise/Club Management System

## 📌 One-Line Summary
A Franchise and Club Management System for a company focused on teaching public speaking.

---
# Franchise and Club Management System

## 🧾 Detailed Project Description

This project is a Franchise and Club Management System designed for a company focused on teaching public speaking across various cities and states through local clubs and franchises. It provides a robust administrative interface for managing clubs, members, and admins, ensuring smooth operation and scalability of the organization’s training and mentoring programs.

The system is built using a Next.js frontend and a Django REST Framework backend, offering a modern, fast, and secure web experience for organization admins.

## 🎯 Purpose and Objective

The core goal of this system is to help a public speaking company digitally manage and scale its network of clubs and franchises. These clubs function as local learning hubs where individuals improve their communication and public speaking skills. The system simplifies the otherwise manual and scattered process of:

- Creating and managing new club branches
- Registering and assigning members to clubs
- Assigning admin privileges to trusted users
- Updating and tracking speaker/member information

## 🧩 Key Modules and Features

### 1. **Admin Authentication System**
- Secure session-based login using Django’s authentication framework
- CSRF protection for safe form submissions and data updates
- Logout functionality with backend session destruction

### 2. **Club Management**
- Admins can create new clubs by providing city, state, postal code, and country
- View, edit, and delete club details
- Club listing with sorting and filtering options

### 3. **Member Management**
- Fetch and display all registered members
- Update a member’s personal information, including their assigned club
- Maintain clean separation between members of different clubs

### 4. **Admin Role Assignment**
- Promote existing members or users to admin role
- View the list of all current admins
- Control admin access to maintain organizational hierarchy

### 5. **Dashboard Interfaces**
- Admin-friendly views for quick access to clubs, members, and other admins
- Interfaces built with reusable and clean React components
- Client-side routing using Next.js pages

## 📁 Project Structure

- **Frontend (Next.js)**: Handles user interface, routing, and interaction.
- **Backend (Django REST Framework)**: Manages database, authentication, and API services.

## 🚀 Technologies Used
- **Frontend**: Next.js, React
- **Backend**: Django, Django REST Framework
- **Database**: SQLite or PostgreSQL (configurable)
- **Authentication**: Django’s built-in authentication system

## 🧱 API Endpoints

- `POST /api/accounts/login/` – Admin login
- `POST /api/accounts/logout/` – Logout
- `GET /api/accounts/clubs/` – List all clubs
- `POST /api/accounts/clubs/` – Add new club
- `PUT /api/accounts/clubs/:id/` – Update club
- `GET /api/accounts/members/` – Fetch all members
- `PUT /api/accounts/members/:username/` – Update member
- `GET /api/accounts/admins/` – Get admin list
AND MANY MORE...
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
