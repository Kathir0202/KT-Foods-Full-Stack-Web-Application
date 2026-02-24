#KT-Foods Full-Stack Web Application

KT Foods is a full-stack restaurant web application built using Node.js, Express.js, and PostgreSQL with a static frontend served via Express.

The project demonstrates server-side routing, REST handling, static asset serving, and database integration for handling user-submitted contact data.

---

## Architecture Overview

- Express server handles routing and middleware.
- Static frontend served from /public.
- REST endpoint processes contact form submissions.
- PostgreSQL used for persistent storage.
- Server acts as both API layer and static file host.

---

## Tech Stack

Backend
- Node.js
- Express.js
- pg (PostgreSQL client)

Frontend
- HTML5
- CSS3
- Vanilla JavaScript

Database
- PostgreSQL

---

## Project Structure

kt-foods/
│
├── public/                 # Static frontend files
│   ├── index.html
│   ├── about.html
│   ├── menu.html
│   ├── service.html
│   ├── contact.html
│   └── assets/
│
├── index.js                # Express server entry point
├── package.json            # Dependencies & scripts
└── README.md
---

## Backend Flow

1. Express initializes middleware.
2. Static assets served using:
  
   app.use(express.static("public"));
   
3. Contact form sends POST request.
4. Server inserts data into PostgreSQL using parameterized queries.
5. Response/redirect handled after successful insertion.

---

## Database Design

**Table: list**

| Column      | Type         | Description              |
|------------|-------------|--------------------------|
| id         | SERIAL PK   | Unique identifier        |
| name       | VARCHAR     | User name                |
| email      | VARCHAR     | User email               |
| description| TEXT        | Message content          |

---

## Key Concepts Implemented

- Express routing
- Middleware usage
- Static file serving
- PostgreSQL connection pooling
- Parameterized SQL queries (basic injection protection)
- Form handling with backend validation

---

## Author

Kathir
