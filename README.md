# Frontend Developer Intern Task - Dashboard Web App

## Overview

This project is a **Scalable Dashboard Web Application** built with **Next.js (React) and Tailwind CSS** for the frontend and **Node.js + Express + MongoDB** for the backend.
It features **JWT-based authentication**, **CRUD operations for tasks**, and a **responsive user interface**.

---

## Features

### Frontend

* Built with **Next.js** and **TypeScript**
* **Responsive design** using Tailwind CSS
* **Protected routes** for dashboard (login required)
* **Add, edit, delete, and mark tasks complete**
* User profile displayed (name and email)
* Logout functionality

### Backend

* **Node.js + Express** API
* **MongoDB** database for storing users and tasks
* **JWT authentication** (signup/login)
* CRUD APIs for tasks
* Password hashing using **bcrypt**
* Error handling and validation

---

## Installation

### Prerequisites

* Node.js (v18+ recommended)
* MongoDB (local or Atlas)

### Steps

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd <your-repo-folder>
   ```

2. **Backend Setup**

   ```bash
   cd backend
   npm install
   ```

   * Create a `.env` file with:

     ```
     PORT=5000
     MONGO_URI=<your-mongodb-connection-string>
     JWT_SECRET=<your-jwt-secret>
     ```

   * Start backend server:

     ```bash
     npm run dev
     ```

3. **Frontend Setup**

   ```bash
   cd frontend
   npm install
   npm run dev
   ```

   * Frontend runs on: `http://localhost:3000`
   * Backend runs on: `http://localhost:5000`

---

## Usage

1. Open the frontend in your browser: `http://localhost:3000`
2. **Register/Login** to access the dashboard
3. **Add, edit, delete, and complete tasks**
4. Logout using the button in the header

---

## API Documentation

A simple API documentation is included in `ai_docs.txt` file, describing all backend routes and request/response formats.

---

## Project Structure

```
/frontend      # Next.js frontend code
/backend       # Node.js + Express backend code
ai_docs.txt    # API documentation
README.md      # Project documentation
```

---

## Notes

* Make sure **MongoDB** is running and accessible via the URI in `.env`
* JWT tokens are stored in `localStorage` for session management
* Passwords are hashed before saving to the database
* Code is structured to allow **easy scaling** and modular expansion

---

## Author

**Your Name** – Maithri
Email:smaithri039@gmail.com