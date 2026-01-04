# 💰 Personal Expense Tracker

A full-stack **Personal Expense Tracker** built using **Flask**, designed to help users securely track, categorize, and analyze their daily expenses.

This project focuses on **backend engineering fundamentals**, authentication, database modeling, and real-world deployment practices.

---

## 🚀 Live Demo

🔗 **Deployed on Render**  
👉 https://personal-expense-tracker-nandhu.onrender.com  

*(Free-tier deployment — data may reset on redeploy)*

---

## 🎯 Project Overview

The Personal Expense Tracker allows users to:

- Register and log in securely
- Add, edit, and delete expenses
- Organize expenses by categories
- View category-wise spending insights
- Manage categories independently
- Access their own data securely (multi-user support)

The project demonstrates how a real-world backend application is structured, deployed, and maintained.

---

## 🧠 Key Features

### 🔐 Authentication & Security
- User registration and login
- Password hashing with Werkzeug
- Session handling using Flask-Login
- Protected routes with `@login_required`

### 📊 Expense Management
- Add, update, and delete expenses
- Date-based expense tracking
- User-specific data isolation

### 🗂 Category Management
- Create, edit, and delete categories
- One-to-many relationship between categories and expenses

### 📈 Analytics
- Category-wise expense aggregation
- Visual representation using Chart.js
- Basic spending suggestions

### ☁️ Deployment
- Deployed on **Render**
- Production WSGI server using **Gunicorn**
- Environment variable–based configuration

---

## 🛠 Tech Stack

### Backend
- Python
- Flask
- Flask-Login
- Flask-SQLAlchemy
- Werkzeug

### Database
- SQLite (used for demo and development)

### Frontend
- Jinja2 Templates
- Bootstrap 5
- Chart.js

### Deployment
- Render
- Gunicorn

---

## 🗃 Database Design

### Entities

**User**
- id
- username
- password

**Category**
- id
- name
- description

**Expense**
- id
- title
- amount
- date
- user_id
- category_id

### Relationships
- One user → many expenses
- One category → many expenses

---

## ⚙️ Local Setup

```bash
git clone https://github.com/imNandini19/personal-expense-tracker.git
cd personal-expense-tracker

python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

pip install -r requirements.txt
python app.py

Open the app at:
http://127.0.0.1:5000
```

## ⚠️ Production Considerations

SQLite is used for simplicity in the demo.

Render’s filesystem is ephemeral, so data may reset on redeploy.

For real production usage:

Migrate to PostgreSQL

Use Flask-Migrate for schema migrations

Add structured logging and monitoring

These trade-offs are intentional and documented.

## 📌 What I Learned

Designing secure, multi-user Flask applications

Managing ORM relationships with SQLAlchemy

Handling authentication and authorization

Debugging real deployment issues

Understanding the difference between demo vs production systems

## 🔮 Future Improvements

PostgreSQL integration

Database migrations with Flask-Migrate

Pagination for large datasets

Password reset functionality

REST API version of the backend

Unit and integration testing

## 👩‍💻 Author

Nandini Mamillapalli
Computer Science Engineering
Aspiring Software Engineer







