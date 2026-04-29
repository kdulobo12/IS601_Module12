📦 Module 12: User Authentication + Calculation BREAD + Integration Testing + CI/CD
## 📌 Project Overview
This project implements a backend system using FastAPI and PostgreSQL that supports:
User registration and login
Secure password handling (hashing)
Full BREAD (Browse, Read, Edit, Add, Delete) functionality for calculations
Integration testing using pytest
Docker containerization and GitHub Actions CI/CD pipeline
Users can:
Register and log in
Create and manage their own calculations
Perform CRUD operations through REST APIs

## 🧩 Features Implemented
## 🔐 User Authentication (Backend)
POST /users/register → Register a new user
POST /users/login → Authenticate user
✔ Passwords are securely hashed before storing
✔ Duplicate users are prevented
✔ Pydantic validation ensures correct input format
✔ Login verifies hashed password before granting access

## 🧮 Calculation Endpoints (BREAD)
GET /calculations → Browse all calculations
GET /calculations/{id} → Read a specific calculation
POST /calculations → Add a new calculation
PUT/PATCH /calculations/{id} → Edit a calculation
DELETE /calculations/{id} → Delete a calculation
✔ Uses SQLAlchemy models
✔ Uses Pydantic schemas (CalculationCreate, CalculationRead)
✔ Proper request/response validation

## 🌐 OpenAPI Testing (Manual)
You can test all endpoints using FastAPI’s built-in UI:
Swagger Docs → http://localhost:8000/docs
ReDoc → http://localhost:8000/redoc
✔ Test user registration and login
✔ Test all calculation endpoints manually
✔ Verify request/response formats
🧪 Integration Testing (pytest)

## ✅ User Tests
Register new user
Login with correct credentials
Verify user stored in database

## ✅ Calculation Tests
Create calculation
Retrieve calculation
Update calculation
Delete calculation

## ❌ Negative Tests
Invalid input → returns error
Unauthorized access (if implemented)
Wrong data types → validation error
✔ Tests ensure full backend functionality
✔ Uses test database setup

## 🐳 DevOps (CI/CD)
Docker used for containerization
GitHub Actions pipeline automatically:
✔ Spins up PostgreSQL database
✔ Runs all pytest integration tests
✔ Builds Docker image
✔ Pushes image to Docker Hub

## 🛠️ Tech Stack
Python (FastAPI)
PostgreSQL
SQLAlchemy
Pydantic
pytest
Docker
GitHub Actions

## 🚀 Setup Instructions

🧩 1. Clone Repository
git clone <your-repo-link>
cd <repo-folder>

## 🧩 2. Create Virtual Environment
python3 -m venv venv
source venv/bin/activate  # Mac
venv\Scripts\activate     # Windows

## 🧩 3. Install Dependencies
pip install -r requirements.txt

## 🧩 4. Run Backend
uvicorn app.main:app --reload
Open:
API Docs → http://localhost:8000/docs

## 🧪 Running Tests
Run pytest:
pytest
✔ Runs all user + calculation integration tests
✔ Ensures endpoints work correctly

## 🐳 Docker Setup
Run with Docker
docker compose up --build
Build Image
docker build -t module12-app .
Run Container
docker run -p 8000:8000 module12-app

## 🔄 CI/CD Pipeline
GitHub Actions automatically:
Runs integration tests
Builds Docker image
Pushes image to Docker Hub

## 🐳 Docker Hub Repository
👉 Add your link here: https://hub.docker.com/r/kdulobo12/module12-web

👉 Docker Image Link: docker push kdulobo12/module12-web:tagname

![alt text](<Screenshot 2026-04-29 at 00.22.11-1.png>)


## 📸 Screenshots

✅ GitHub Actions workflow success

<img width="3354" height="1516" alt="image" src="https://github.com/user-attachments/assets/fb7d4408-3993-424e-a93f-88ce59f935aa" />

✅ API working in browser (/docs)

<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 38 15" src="https://github.com/user-attachments/assets/b5fd2d85-13c9-4923-bbed-e345645cb4a0" />

✅ User register/login working

<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 49 21" src="https://github.com/user-attachments/assets/033daa60-fce3-4fc3-a35e-2789f452c6cf" />


<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 49 27" src="https://github.com/user-attachments/assets/3ab8965b-50ee-4e8d-ba9c-07c2b5a7e9d0" />

<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 49 33" src="https://github.com/user-attachments/assets/cd8406d6-2ba4-4140-b14f-c43add337776" />


<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 51 31" src="https://github.com/user-attachments/assets/1eca64b6-66e5-4f0c-accd-5338f3e4c3f3" />


<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 51 37" src="https://github.com/user-attachments/assets/ac34568d-b4e7-44f8-bc79-24af02fb9aa4" />

<img width="1680" height="1050" alt="Screenshot 2026-04-29 at 00 51 42" src="https://github.com/user-attachments/assets/1b08489b-81e5-4e6c-8a5d-666863a5160f" />



✅ Calculation endpoints working

## 💡 Reflection 
This project helped me understand how backend systems work in a real-world application. I implemented user registration and login with secure password hashing, which showed me the importance of security in APIs. I also built full BREAD functionality for calculations, which helped me understand how CRUD operations work with databases using SQLAlchemy.
Writing integration tests using pytest was very useful because it allowed me to test the application as a whole instead of testing individual functions. I also learned how GitHub Actions can automate testing and deployment, which is important for real-world development workflows.
One challenge I faced was connecting all parts together, including models, schemas, routes, and tests. However, after debugging and testing step by step, I was able to complete the backend successfully. Overall, this project improved my understanding of APIs, databases, testing, and DevOps practices.

## 🔥 Quick Commands Cheat Sheet
Action	Command
Run backend	uvicorn app.main:app --reload
Run tests	pytest
Docker run	docker compose up --build
Build image	docker build -t module12-app .
Push code	git add . && git commit -m "msg" && git push

## 👩‍💻 Author
Krupa Dulobo
