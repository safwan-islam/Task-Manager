<h1 align="center">📋 Task Manager</h1>

<p align="center">
  <strong>Full-Stack Task Management System</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" />
</p>

---

## 📌 About

Task Manager is a full-stack web application for managing tasks with **role-based authentication** supporting multiple user permission levels. The backend exposes a **REST API via Flask** secured with **JWT tokens**, while the frontend is built with **Django templates and Bootstrap** for a responsive user experience.

The architecture separates the API layer (Flask) from the rendering layer (Django), reducing page-load complexity and keeping concerns cleanly divided.

---

## ⚙️ Tech Stack

| Layer | Technology |
|:------|:-----------|
| **Language** | Python |
| **Backend API** | Flask |
| **Frontend** | Django Templates, Bootstrap |
| **Database** | MongoDB |
| **Auth** | JWT (JSON Web Tokens) |
| **API Style** | REST |

---

## 🚀 Features

- **Role-Based Authentication** — Multiple user permission levels with JWT security
- **REST API** — 5+ endpoints handling full CRUD for tasks and users
- **JWT Security** — Token-based auth on all protected endpoints
- **Responsive Frontend** — Django templates with Bootstrap
- **Separated Layers** — API (Flask) and rendering (Django) are decoupled
- **MongoDB Backend** — NoSQL document storage for flexible task schemas
- **Full CRUD** — Create, read, update, delete for both tasks and users

---

## 📡 API Endpoints

| Method | Endpoint | Description | Auth |
|:-------|:---------|:------------|:-----|
| `POST` | `/api/auth/register` | Register a new user | Public |
| `POST` | `/api/auth/login` | Login and receive JWT | Public |
| `GET` | `/api/tasks` | Get all tasks | JWT |
| `POST` | `/api/tasks` | Create a new task | JWT |
| `PUT` | `/api/tasks/:id` | Update a task | JWT |
| `DELETE` | `/api/tasks/:id` | Delete a task | JWT |

---

## 📦 Getting Started

### Prerequisites

- Python 3.8+
- MongoDB
- pip

### Setup

1. Clone the repo
   ```bash
   git clone https://github.com/safwan-islam/Task-Manager.git
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Make sure MongoDB is running
4. Run the Flask API
   ```bash
   python app.py
   ```
5. Run the Django frontend
   ```bash
   python manage.py runserver
   ```

---

## 👤 Author

**Safwan-Ahmed Islam** — [GitHub](https://github.com/safwan-islam) · [LinkedIn](https://linkedin.com/in/safwan-islam)
