# Healthcare Backend System

A backend REST API project built using Django, Django REST Framework (DRF), PostgreSQL, and JWT Authentication.

---

# Project Objective

The objective of this project is to build a secure healthcare backend system where:

* Users can register and log in
* Authenticated users can manage patient records
* Authenticated users can manage doctor records
* Patients can be assigned to doctors
* Data is securely stored in PostgreSQL
* APIs are protected using JWT authentication

---

# Technologies Used

| Technology            | Purpose               |
| --------------------- | --------------------- |
| Django                | Backend Framework     |
| Django REST Framework | REST API Development  |
| PostgreSQL            | Database              |
| JWT (SimpleJWT)       | Authentication        |
| Postman               | API Testing           |
| Python Decouple       | Environment Variables |

---


<img width="2541" height="1599" alt="image" src="https://github.com/user-attachments/assets/4382c556-29e0-40e1-9439-80e5c79d784d" />

<img width="2003" height="1415" alt="image" src="https://github.com/user-attachments/assets/546b60a4-a4d1-4700-9925-d1c88d6a359c" />

<img width="969" height="1280" alt="djangoBackend" src="https://github.com/user-attachments/assets/4d02d642-de37-44b5-b4c9-5c1250e64b5b" />

<img width="2350" height="1565" alt="image" src="https://github.com/user-attachments/assets/d5839d90-2a6c-402e-a1e4-866bf874e222" />




# Features Implemented

## Authentication APIs

* User Registration
* User Login using JWT
* Token-based authentication

## Patient APIs

* Add patient
* Get all patients
* Get single patient
* Update patient
* Delete patient

## Doctor APIs

* Add doctor
* Get all doctors
* Get single doctor
* Update doctor
* Delete doctor

## Patient-Doctor Mapping APIs

* Assign doctor to patient
* Get mappings
* Delete mapping

---

# Project Structure

```bash
healthcare_backend/
│
├── authentication/
├── patients/
├── doctors/
├── mappings/
├── config/
├── manage.py
├── .env
└── venv/
```

---

# Database Used

PostgreSQL is used as the database for storing:

* User data
* Patient records
* Doctor records
* Mapping relationships

---

# Authentication System

JWT Authentication is implemented using:

```bash
rest_framework_simplejwt
```

Two tokens are generated:

* Access Token
* Refresh Token

Protected APIs require a valid Bearer Token.

---

# API Endpoints

## Authentication APIs

| Method | Endpoint            | Description   |
| ------ | ------------------- | ------------- |
| POST   | /api/auth/register/ | Register user |
| POST   | /api/auth/login/    | Login user    |

---

## Patient APIs

| Method | Endpoint            | Description        |
| ------ | ------------------- | ------------------ |
| POST   | /api/patients/      | Add patient        |
| GET    | /api/patients/      | Get all patients   |
| GET    | /api/patients/<id>/ | Get single patient |
| PUT    | /api/patients/<id>/ | Update patient     |
| DELETE | /api/patients/<id>/ | Delete patient     |

---

## Doctor APIs

| Method | Endpoint           | Description       |
| ------ | ------------------ | ----------------- |
| POST   | /api/doctors/      | Add doctor        |
| GET    | /api/doctors/      | Get all doctors   |
| GET    | /api/doctors/<id>/ | Get single doctor |
| PUT    | /api/doctors/<id>/ | Update doctor     |
| DELETE | /api/doctors/<id>/ | Delete doctor     |

---

## Mapping APIs

| Method | Endpoint            | Description              |
| ------ | ------------------- | ------------------------ |
| POST   | /api/mappings/      | Assign doctor to patient |
| GET    | /api/mappings/      | Get all mappings         |
| DELETE | /api/mappings/<id>/ | Delete mapping           |

---

# How To Run The Project

## Step 1: Clone Repository

```bash
git clone <repository-link>
cd healthcare_backend
```

---

## Step 2: Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## Step 3: Install Dependencies

```bash
pip install django djangorestframework psycopg2-binary djangorestframework-simplejwt python-decouple
```

---

## Step 4: Configure PostgreSQL

Create PostgreSQL database:

```sql
CREATE DATABASE healthcare_db;
```

---

## Step 5: Create .env File

Create `.env` file in root directory.

```env
SECRET_KEY=django_secret_key

DB_NAME=healthcare_db
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
```

---

## Step 6: Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## Step 7: Run Server

```bash
python manage.py runserver
```

Server will run at:

```bash
http://127.0.0.1:8000/
```

---

# API Testing

APIs were tested using Postman.

JWT Bearer Token authentication was used for protected endpoints.

---

# Important Concepts Used

## Django ORM

Used for database interaction without writing raw SQL queries.

## Serializers

Used to convert Django model instances into JSON format.

## ModelViewSet

Used for automatic CRUD functionality.

## ForeignKey Relationships

Used to establish:

* User → Patient relationship
* Patient → Doctor relationship

## JWT Authentication

Used to secure APIs using token-based authentication.

---

# Future Improvements

* Swagger API Documentation
* Role-based Authentication
* Docker Deployment
* Pagination
* Search & Filtering
* Appointment Scheduling

---

# Conclusion

This project demonstrates the implementation of a secure healthcare backend system using Django REST Framework and PostgreSQL with JWT authentication.

The project includes:

* Authentication System
* CRUD APIs
* Relational Database Modeling
* Protected Endpoints
* PostgreSQL Integration
* RESTful API Architecture
