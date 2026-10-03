
# Employee Management & HRMS

A backend-based Employee Management and Human Resource Management System built using **Python, FastAPI, MySQL, and SQLAlchemy**. The application provides REST APIs for managing employee information and HR-related operations with authentication, validation, and database integration.

## 📌 Project Overview

The Employee Management & HRMS project is designed to simplify employee and HR data management through a RESTful API.

The system allows authorized users to manage employee records, departments, attendance, leave information, and other HR-related data through structured APIs.

## 🚀 Features

* User registration and login
* JWT-based authentication
* Role-based access control
* Employee management

  * Add employee
  * View employee
  * Update employee
  * Delete employee
* Department management
* Employee search and filtering
* Attendance management
* Leave management
* Input validation
* Error handling
* MySQL database integration
* RESTful API architecture
* Interactive API documentation using Swagger
* Unit testing with Pytest

## 🛠️ Tech Stack

### Backend

* Python
* FastAPI
* SQLAlchemy
* Pydantic

### Database

* MySQL

### Authentication

* JWT

### Testing

* Pytest

### Development Tools

* Visual Studio Code
* Git
* GitHub
* Postman / Swagger UI

## 🏗️ Project Architecture

```text
Client
   │
   ▼
FastAPI REST API
   │
   ├── Authentication
   ├── Employee Management
   ├── Department Management
   ├── Attendance
   └── Leave Management
   │
   ▼
SQLAlchemy
   │
   ▼
MySQL Database
```

## 📂 Project Structure

```text
employee-management-hrms/
│
├── app/
│   ├── routers/
│   ├── models/
│   ├── schemas/
│   ├── services/
│   ├── database/
│   └── auth/
│
├── tests/
│
├── .env.example
├── .gitignore
├── requirements.txt
├── main.py
└── README.md
```

> Update the structure above to match your actual project folders.

## 🗄️ Database

The application uses **MySQL** as the relational database.

Example entities:

```text
Users
   │
   └── Employees
          │
          ├── Departments
          ├── Attendance
          └── Leaves
```

The database uses relationships between tables to maintain consistent employee and HR information.

## 🔐 Authentication

The application uses **JWT-based authentication** to protect API endpoints.

The general authentication flow is:

```text
User Registration
       ↓
User Login
       ↓
Credentials Validation
       ↓
JWT Token Generated
       ↓
Authenticated API Requests
```

Sensitive credentials and secret keys are stored in environment variables rather than being committed to GitHub.

## 🔗 API Endpoints

Example endpoints:

### Authentication

```text
POST /auth/register
POST /auth/login
```

### Employees

```text
GET    /employees
GET    /employees/{employee_id}
POST   /employees
PUT    /employees/{employee_id}
DELETE /employees/{employee_id}
```

### Departments

```text
GET    /departments
POST   /departments
PUT    /departments/{department_id}
DELETE /departments/{department_id}
```

> Update these endpoints according to the APIs actually implemented in your project.

## 📖 API Documentation

FastAPI automatically provides interactive API documentation.

After starting the application, open:

```text
http://127.0.0.1:8000/docs
```

The Swagger interface can be used to test the available APIs.

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/employee-management-hrms.git
```

### 2. Navigate to the project

```bash
cd employee-management-hrms
```

### 3. Create a virtual environment

Windows:

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure MySQL

Create a MySQL database:

```sql
CREATE DATABASE employee_hrms;
```

Create your environment configuration using `.env`.

Example:

```env
DATABASE_URL=mysql+pymysql://username:password@localhost/employee_hrms
SECRET_KEY=your_secret_key
```

**Do not commit your `.env` file to GitHub.**

### 6. Run the application

```bash
uvicorn main:app --reload
```

The API will be available at:

```text
http://127.0.0.1:8000
```

Swagger documentation:

```text
http://127.0.0.1:8000/docs
```

## 🧪 Testing

Run the test suite using:

```bash
pytest
```

The tests cover the implemented API functionality and help verify application behaviour.

## 📸 Screenshots

Add screenshots of:

* Swagger API documentation
* Login API
* Employee creation
* Employee list
* MySQL database
* API responses

Example:

```text
screenshots/
├── swagger.png
├── login.png
├── employees.png
└── database.png
```

## 🔒 Security

The project follows basic security practices:

* Passwords should not be stored as plain text.
* JWT tokens are used for authenticated requests.
* Database credentials are stored using environment variables.
* `.env` is excluded from Git.
* API input is validated before processing.

## 🎯 Learning Outcomes

Through this project, I developed practical experience with:

* Python backend development
* Object-Oriented Programming
* FastAPI
* REST API development
* MySQL database integration
* SQLAlchemy ORM
* Authentication and authorization
* API validation
* Exception handling
* Unit testing
* Git and GitHub

## 🔮 Future Improvements

Possible future enhancements include:

* Employee performance management
* Payroll management
* Email notifications
* Advanced reporting
* File/resume uploads
* Docker containerization
* CI/CD pipeline
* Cloud deployment
* Automated database migrations

## 👨‍💻 Author

**Veligandla Harinath**


This project is a basic employee management system which supports registration and login of two roles; namely Junior HR and Senior HR. The Junior HR can submit various types of forms like payslip, offer letter, hike letter, etc. and the senior HR can generate a pdf out of it based on a pre-existing word template.

## Running the Server

Run both the shell scripts `start_backend.sh` and `start_frontend.sh` to start the server.

## Modifying the DB

Refer to `app/scripts/queries.py` and `app/scripts/create.py` to change the database structure.

## Modifying templates

The word templates are given in the `templates` folder and follow Jinja2 syntax.

## Screenshots

![login](https://github.com/parekh0711/employee-management/blob/main/screenshots/login.png)
![register](https://github.com/parekh0711/employee-management/blob/main/screenshots/register.png)
![jrhr dashboard](https://github.com/parekh0711/employee-management/blob/main/screenshots/jr_hr_dashboard.png)
![srhr dashboard](https://github.com/parekh0711/employee-management/blob/main/screenshots/sr_hr.png)
⭐ If you find this project useful, consider giving the repository a star.
![exp letter](https://github.com/parekh0711/employee-management/blob/main/screenshots/exp_letter_generate.png)
![exp_pdf](https://github.com/parekh0711/employee-management/blob/main/screenshots/pdf.png)
