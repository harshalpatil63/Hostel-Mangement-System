<p align="center">
  <img src="https://img.shields.io/badge/Flask-3.1.0-blue?style=for-the-badge&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3.x-yellow?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-Database-336791?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/SQLAlchemy-ORM-red?style=for-the-badge&logo=sqlalchemy&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

# 🏨 Hostel Management System

> A full-stack web application for discovering, comparing, and registering for hostels with an integrated feedback & rating system and a powerful admin dashboard.

---

## 📋 Table of Contents

- [About The Project](#-about-the-project)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Database Setup](#-database-setup)
- [Usage](#-usage)
- [Available Hostels](#-available-hostels)
- [API Routes](#-api-routes)
- [Contributing](#-contributing)
- [Author](#-author)

---

## 🎯 About The Project

The **Hostel Management System** is a comprehensive web application designed to simplify the process of finding, comparing, and registering for hostels. It provides students with detailed hostel information including facilities, room types, mess menus, and real-time feedback from other residents. The system also features a robust admin panel for managing hostels, students, and feedback.

### 🔑 Problem Statement
Students often struggle to find reliable information about hostels near their college. This system bridges that gap by providing a centralized platform with verified hostel details, genuine student reviews, and a seamless registration process.

---

## ✨ Key Features

### 👤 For Students
| Feature | Description |
|---------|-------------|
| 🔐 **User Authentication** | Secure signup & login with password hashing (Werkzeug) |
| 🏠 **Hostel Discovery** | Browse multiple hostels with detailed info, photos & facilities |
| 📝 **Online Registration** | Complete hostel registration with personal, parent & academic details |
| ⭐ **Feedback & Ratings** | Submit ratings (1-5 stars) and written reviews with media uploads |
| 📸 **Media Upload** | Upload images & videos (PNG, JPG, MP4, MOV, WebM) with feedback |
| 🔄 **Hostel-Specific Sessions** | Separate login sessions per hostel for secure feedback |

### 🛡️ For Admins
| Feature | Description |
|---------|-------------|
| 📊 **Admin Dashboard** | Centralized management panel with overview statistics |
| 👨‍🎓 **Student Management** | View, search, and manage all registered students |
| 🏢 **Hostel Management** | Add, edit, and configure hostel details dynamically |
| 💬 **Feedback Moderation** | Monitor and manage student feedback across all hostels |
| 🔒 **Role-Based Access** | Admin-only access with email-based role verification |

---

## 🛠️ Tech Stack

### Backend
| Technology | Purpose |
|-----------|---------|
| **Python 3.x** | Core programming language |
| **Flask 3.1.0** | Web framework |
| **Flask-SQLAlchemy 3.1.1** | ORM for database operations |
| **PostgreSQL** | Relational database |
| **Werkzeug 3.1.3** | Password hashing & security utilities |
| **Jinja2** | Server-side HTML templating |

### Frontend
| Technology | Purpose |
|-----------|---------|
| **HTML5** | Page structure & semantic markup |
| **CSS3** | Styling & responsive design |
| **JavaScript** | Client-side interactivity |

### Other Dependencies
| Package | Purpose |
|---------|---------|
| **psycopg2** | PostgreSQL adapter for Python |
| **Flask-CORS** | Cross-Origin Resource Sharing |
| **Flask-Mail** | Email functionality |

---

## 📁 Project Structure

```
Hostel-Mangement-System/
│
├── app.py                  # Main Flask application & routes
├── admin.py                # Admin blueprint with dashboard routes
├── Database.py             # SQLAlchemy models & database schema
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
│
├── templates/              # Jinja2 HTML templates
│   ├── landing.html        # Homepage / Landing page
│   ├── first.html          # Hostel listing page
│   ├── login.html          # User login page
│   ├── signup.html         # User registration page
│   ├── registration.html   # Hostel room registration form
│   ├── start_admin.html    # Admin login page
│   ├── RBoyshostel.html    # R Boys Hostel detail page
│   ├── vritteGirlshostel.html  # VRIITEE Girls Hostel detail page
│   ├── sunrisehostel.html  # Sunrise Hostel detail page
│   ├── SaiDarbar.html      # Sai Darbar Hostel detail page
│   ├── deccanspace.html    # Deccan Space Hostel detail page
│   ├── Jbhostel.html       # J B Hostel detail page
│   └── admin/              # Admin panel templates
│       ├── dashboard.html  # Admin dashboard
│       ├── students.html   # Student management
│       ├── hostels.html    # Hostel management
│       ├── hostel_form.html    # Add/Edit hostel form
│       ├── hostel_view.html    # View hostel details
│       └── feedbacks.html  # Feedback management
│
├── static/                 # Static assets
│   ├── css/
│   │   └── styles.css      # Main stylesheet
│   ├── assets/             # General hostel images
│   ├── Rboys/              # R Boys Hostel images
│   ├── virteehostel/       # VRIITEE Hostel images
│   ├── sunrisehostel/      # Sunrise Hostel images
│   ├── saidarbar/          # Sai Darbar Hostel images
│   ├── deccanspace/        # Deccan Space Hostel images
│   ├── uploads/            # User-uploaded media files
│   ├── food/               # Food & mess images
│   ├── hostel/             # General hostel photos
│   └── images/             # Miscellaneous images
│
└── uploads/                # Additional uploaded documents
```

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+** installed on your system
- **PostgreSQL** database server running
- **pip** package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/harshalpatil63/Hostel-Mangement-System.git
   cd Hostel-Mangement-System
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv

   # On Windows
   venv\Scripts\activate

   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure the database** (see [Database Setup](#-database-setup))

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Open in browser**
   ```
   http://127.0.0.1:5000
   ```

---

## 🗄️ Database Setup

### 1. Install PostgreSQL
Download and install PostgreSQL from [postgresql.org](https://www.postgresql.org/download/)

### 2. Create the Database
```sql
CREATE DATABASE hostel_finder;
```

### 3. Update Connection String
Edit the database URI in `app.py`:
```python
app.config["SQLALCHEMY_DATABASE_URI"] = "postgresql://your_username:your_password@localhost/hostel_finder"
```

### 4. Tables Auto-Created
The application automatically creates all required tables on first run using:
```python
with app.app_context():
    db.create_all()
```

### Database Models

| Model | Description |
|-------|-------------|
| `User` | Stores user accounts with hashed passwords |
| `Student` | Complete student registration details |
| `Feedback` | Generic hostel feedback & ratings |
| `FeedbackRboys` | R Boys Hostel specific feedback |
| `sunrise` | Sunrise Hostel specific feedback |
| `Deccan` | Deccan Space Hostel feedback |
| `saidarbar` | Sai Darbar Hostel feedback |
| `AdminRole` | Admin email-based role management |
| `Hostel` | Dynamic hostel configuration |

---

## 📖 Usage

### As a Student
1. Visit the **Landing Page** → Browse available hostels
2. Click on any hostel to view details, facilities, room types & mess menu
3. **Sign Up** → Create an account with your email
4. **Login** → Access hostel-specific features
5. **Submit Feedback** → Rate the hostel and write a review
6. **Register** → Fill in the registration form with personal & academic details

### As an Admin
1. Navigate to `/start-admin`
2. Login with admin credentials
3. Access the **Dashboard** with student & hostel statistics
4. Manage **Students**, **Hostels**, and **Feedback** from the admin panel

---

## 🏠 Available Hostels

| # | Hostel Name | Type | Route |
|---|------------|------|-------|
| 1 | R Boys Hostel | Boys | `/RBoyshostel` |
| 2 | VRIITEE Girls Hostel | Girls | `/vritteGirlshostel` |
| 3 | Sunrise Hostel | Co-ed | `/sunrisehostel` |
| 4 | Sai Darbar Hostel | Co-ed | `/saiDarbar` |
| 5 | Deccan Space Hostels | Co-ed | `/deccanspace` |
| 6 | J B Hostel | Co-ed | `/jbhostel` |

---

## 🛣️ API Routes

| Method | Route | Description |
|--------|-------|-------------|
| `GET` | `/` | Redirect to landing page |
| `GET` | `/landing` | Homepage |
| `GET` | `/first` | Hostel listing |
| `GET/POST` | `/login` | User login |
| `GET/POST` | `/signup` | User signup |
| `GET` | `/logout` | Logout & clear session |
| `GET/POST` | `/RBoyshostel` | R Boys Hostel page |
| `GET/POST` | `/vritteGirlshostel` | VRIITEE Girls Hostel page |
| `GET/POST` | `/sunrisehostel` | Sunrise Hostel page |
| `GET/POST` | `/saiDarbar` | Sai Darbar Hostel page |
| `GET/POST` | `/deccanspace` | Deccan Space Hostel page |
| `GET/POST` | `/jbhostel` | J B Hostel page |
| `GET/POST` | `/registration/<hostel>` | Student registration form |
| `GET/POST` | `/start-admin` | Admin login |
| `GET` | `/admin/dashboard` | Admin dashboard |
| `GET` | `/admin/students` | Student management |
| `GET` | `/admin/hostels` | Hostel management |
| `GET` | `/admin/feedbacks` | Feedback management |

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

---

## 👨‍💻 Author

**Harshal Patil**

[![GitHub](https://img.shields.io/badge/GitHub-harshalpatil63-181717?style=for-the-badge&logo=github)](https://github.com/harshalpatil63)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with ❤️ by <strong>Harshal Patil</strong>
</p>
