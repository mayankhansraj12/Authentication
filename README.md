# 🔐 Authentication

A full-stack **Authentication system** featuring email verification, secure login, password reset, protected routes, and JWT-based authentication using HTTP-only cookies.
Built with **MongoDB, Express, React, Node.js**, and **Zustand** for state management.


---

## ✨ Features

* User signup & login
* Email verification with OTP
* Protected routes (verified users only)
* Password reset flow
* JWT authentication using HTTP-only cookies
* Secure password hashing with bcrypt
* State management using Zustand
* Clean separation of frontend & backend
* Environment-based configuration
* Production-ready auth logic (email failures are non-blocking)

---

## 🛠️ Tech Stack

### Frontend

* React (Vite)
* React Router
* Zustand
* Axios
* Tailwind CSS
* React Hot Toast

### Backend

* Node.js
* Express.js
* MongoDB (Mongoose)
* JWT
* bcrypt
* Mailtrap (for email testing)
  
---

## ⚙️ Environment Variables

### Backend (`.env`)

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=development
MAILTRAP_TOKEN=your_mailtrap_api_token
MAILTRAP_ENDPOINT=https://send.api.mailtrap.io/
```

---

## 🚀 Running the Project Locally

### 1️⃣ Clone the repository

```bash
git clone https://github.com/mayankhansraj12/Authentication.git
cd Authentication
```

---

### 2️⃣ Start Backend

```bash
cd Backend
npm install
npm run dev
```

Backend runs on:

```
http://localhost:5000
```

---

### 3️⃣ Start Frontend

```bash
cd Frontend
npm install
npm run dev
```

Frontend runs on:

```
http://localhost:5173
```

---

## 📧 Email Handling (Important)

This project uses **Mailtrap (free/demo plan)** for testing emails.

### Limitations:

* Emails can only be sent to the **Mailtrap account owner**
* Verification emails to other addresses will fail (expected behavior)

### How it’s handled:

* Email sending is **non-blocking**
* Signup/login works even if email fails
* OTP can be logged or manually verified during development

---

## 🔐 Authentication Flow

1. User signs up
2. User is saved with `isVerified = false`
3. OTP is generated and sent via email
4. User verifies OTP
5. `isVerified` is set to `true`
6. Only verified users can access protected routes

---
