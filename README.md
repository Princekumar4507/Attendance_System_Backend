# HRMS Lite – Backend

Employee & Attendance Management System (Backend API)

Live API:https://attendance-system-backend.onrender.com

---

## Features

* Add employee
* Get all employees
* Delete employee
* Check-in employee
* Check-out employee
* Get attendance by employee
* Prisma + PostgreSQL database
* Deployed on Render

---

## Tech Stack

* Node.js
* Express.js
* Prisma ORM
* PostgreSQL
* Render (deployment)
* CORS
* dotenv

---

## Project Structure


hrms-lite-backend/
 ├── prisma/
 │    └── schema.prisma
 ├── server.js
 ├── package.json
 └── .env (not committed)

---


##  Local Setup

### 1. Clone repo


git clone  https://github.com/Princekumar4507/Attendance_System_Backend
---

### 2. Install dependencies

npm install


### 3. Create `.env`


DATABASE_URL="postgresql://hrms_db_6crn_user:cXodwragnzVGqjExIZoU4oWejKgaot0a@dpg-d622jqvpm1nc73fkpk30-a.singapore-postgres.render.com/hrms_db_6crn"
PORT=5000


### 4. Run migrations
npx prisma migrate dev
npx prisma generate


### 5. Start server


npm start
```

Server runs on:

```
http://localhost:5000
```

---

## 🔗 API Endpoints

### Root test

```
GET /
```

### Employees

Add employee

POST /employees

Get all employees

GET /employees

Delete employee

DELETE /employees/:id

---

### Attendance

Check-in
POST /attendance/checkin


Check-out

POST /attendance/checkout

Get attendance by employee

GET /attendance/:employeeId

---

## Database

Using PostgreSQL + Prisma

Open Prisma Studio:

npx prisma studio
```

---

## Deployment (Render)

1. Push backend repo to GitHub
2. Create Web Service on Render
3. Add environment variable:


DATABASE_URL = [https://hrms-lite-backend-czi9.onrender.com]


4. Build command:


npm install && npx prisma generate
```

5. Start command:


node server.js
```

---

## Important

Never commit `.env` file.
Database credentials must stay private.

Add to `.gitignore`:


.env
node_modules
```

---

## Author

Prince
Full-Stack Assignment Submission (HRMS Lite)
