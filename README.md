
🔐 MERN Authentication System

A full-stack MERN authentication system featuring email verification, secure login, password reset, protected routes, and JWT-based authentication using HTTP-only cookies.
Built with MongoDB, Express, React, Node.js, and Zustand for state management.

⚠️ Note: This project is currently configured to run locally and is not deployed.

✨ Features

User signup & login

Email verification with OTP

Protected routes (verified users only)

Password reset flow

JWT authentication using HTTP-only cookies

Secure password hashing with bcrypt

State management using Zustand

Clean separation of frontend & backend

Environment-based configuration

Production-ready auth logic (email failures are non-blocking)

🛠️ Tech Stack
Frontend

React (Vite)

React Router

Zustand

Axios

Tailwind CSS

React Hot Toast

Backend

Node.js

Express.js

MongoDB (Mongoose)

JWT

bcrypt

Mailtrap (for email testing)



⚙️ Environment Variables
Backend (Backend/.env)
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=development
CLIENT_URL=http://localhost:5173

MAILTRAP_TOKEN=your_mailtrap_api_token
MAILTRAP_ENDPOINT=https://send.api.mailtrap.io/

Frontend (Frontend/.env)
VITE_API_URL=http://localhost:5000/api/auth

🚀 Running the Project Locally
1️⃣ Clone the repository
git clone https://github.com/your-username/mern-auth.git
cd mern-auth

2️⃣ Start Backend
cd Backend
npm install
npm run dev


Backend runs on:

http://localhost:5000

3️⃣ Start Frontend
cd Frontend
npm install
npm run dev


Frontend runs on:

http://localhost:5173

📧 Email Handling (Important)

This project uses Mailtrap (free/demo plan) for testing emails.

Limitations:

Emails can only be sent to the Mailtrap account owner

Verification emails to other addresses will fail (expected behavior)

How it’s handled:

Email sending is non-blocking

Signup/login works even if email fails

OTP can be logged or manually verified during development

🔐 Authentication Flow

User signs up

User is saved with isVerified = false

OTP is generated and sent via email

User verifies OTP

isVerified is set to true

Only verified users can access protected routes

B
