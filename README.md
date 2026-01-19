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

## 🖼️ Screenshots

> Login Page
<img width="839" height="630" alt="image" src="https://github.com/user-attachments/assets/34649e6e-fa68-47d4-b29e-3c3e58356789" />
> SignUp Page
<img width="1478" height="801" alt="image" src="https://github.com/user-attachments/assets/547d2006-edd9-4ad7-9a9e-5bac0c9e7b52" />
> OTP Verification
<img width="1138" height="658" alt="image" src="https://github.com/user-attachments/assets/8336e47a-b9d9-496f-ad63-68bdc4aebc29" />
> Verification Email
<img width="1752" height="890" alt="image" src="https://github.com/user-attachments/assets/2547e639-0179-4e3e-a7d5-fd4555492aa6" />
> DashBoard
<img width="1189" height="723" alt="image" src="https://github.com/user-attachments/assets/4b1b468d-6631-4e80-8e36-32809d5a202a" />
> Forgot Password
<img width="1218" height="620" alt="image" src="https://github.com/user-attachments/assets/a7250574-0e65-4a0d-b93e-a7bd5b2cd12c" />
> Password Reset Mail
<img width="1663" height="852" alt="image" src="https://github.com/user-attachments/assets/f82fd2ed-98fb-441f-998a-430ebf5d71e9" />
> Password Reset Window
<img width="1259" height="669" alt="image" src="https://github.com/user-attachments/assets/b903ec0b-ae7f-4a9f-b199-78a3e76f455a" />

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
