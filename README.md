<h1 align="center">📋 Task Manager</h1>

<p align="center">
  <strong>Full-Stack Task Management System</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white" />
</p>

---

## 📌 About

Task Manager is a full-stack task management app split into two parts: a **Flask REST API backend** secured with **JWT tokens** and a **Django frontend** with Bootstrap. Users can sign up, log in, create tasks, assign them to other users, and track tasks created by or assigned to them.

The architecture fully separates the API layer (Flask + MongoDB) from the rendering layer (Django templates), keeping concerns cleanly divided.

---

## ⚙️ Tech Stack

| Layer | Technology |
|:------|:-----------|
| **Backend API** | Flask (Blueprints) |
| **Frontend** | Django Templates, Bootstrap |
| **Database** | MongoDB |
| **Auth** | JWT (JSON Web Tokens) |
| **Language** | Python |
| **Architecture** | MVC (Models / Views / Controllers) |

---

## 🏗️ Project Structure

```
Task-Manager/
│
├── Backend (Flask API)
│   ├── app.py                      # Flask app entry point
│   ├── app_config.py               # Configuration
│   ├── controllers/
│   │   ├── user_controller.py      # User signup, login, fetch
│   │   └── task_controller.py      # Task CRUD logic
│   ├── models/
│   │   ├── user_model.py           # User schema
│   │   └── task_model.py           # Task schema
│   ├── views/
│   │   ├── user_view.py            # User API routes (Blueprint)
│   │   └── task_view.py            # Task API routes (Blueprint)
│   ├── helpers/
│   │   └── token_validation.py     # JWT token validation
│   └── database/
│       └── db.py                   # MongoDB connection
│
└── Frontend (Django)
    ├── manage.py
    ├── django_frontend/
    │   ├── settings.py
    │   └── urls.py
    └── main/
        ├── views.py                # Django views consuming Flask API
        ├── urls.py
        └── templates/main/
            ├── base.html           # Base layout
            ├── login.html
            ├── signup.html
            ├── task_list.html      # Tasks created by user
            ├── assigned_tasks.html # Tasks assigned to user
            ├── create_task.html
            └── update_task.html
```

---

## 📡 API Endpoints

### Users

| Method | Endpoint | Description | Auth |
|:-------|:---------|:------------|:-----|
| `POST` | `/v0/users/signup` | Register a new user | Public |
| `POST` | `/v0/users/login` | Login, returns JWT | Public |
| `GET` | `/v0/users/all` | Get all users | JWT |

### Tasks

| Method | Endpoint | Description | Auth |
|:-------|:---------|:------------|:-----|
| `POST` | `/tasks/` | Create a new task | JWT |
| `GET` | `/tasks/createdby/` | Get tasks created by logged-in user | JWT |
| `GET` | `/tasks/assignedto/` | Get tasks assigned to logged-in user | JWT |
| `PATCH` | `/tasks/<taskUid>` | Update a task | JWT |
| `DELETE` | `/tasks/<taskUid>` | Delete a task | JWT |

---

## 🚀 Features

- **User Authentication** — Signup + login with JWT token generation
- **Token Validation** — All protected routes validate JWT before processing
- **Task Assignment** — Create tasks and assign them to other users by UID
- **Dual Task Views** — "Created by me" and "Assigned to me" views
- **Full CRUD** — Create, read, update, delete for tasks
- **Blueprint Architecture** — Flask routes organized with Blueprints (`user`, `task_view`)
- **Responsive Frontend** — Django templates with Bootstrap (login, signup, task list, create, update)
- **Separated Layers** — Flask API runs independently from Django frontend

---

## 📦 Getting Started

### Prerequisites

- Python 3.8+
- MongoDB running locally
- pip

### Setup — Backend

1. Clone the repo
   ```bash
   git clone https://github.com/safwan-islam/Task-Manager.git
   ```
2. Install dependencies
   ```bash
   pip install flask pymongo pyjwt bcrypt
   ```
3. Make sure MongoDB is running on `localhost:27017`
4. Run the Flask API
   ```bash
   python app.py
   ```

### Setup — Frontend

1. Navigate to the Django frontend folder
2. Install Django
   ```bash
   pip install django requests
   ```
3. Run the Django server
   ```bash
   python manage.py runserver
   ```

---

## 👤 Author

**Safwan-Ahmed Islam** — [GitHub](https://github.com/safwan-islam) · [LinkedIn](https://linkedin.com/in/safwan-islam)
