# 📚 StudyNotion – Full‑Stack EdTech Platform

**StudyNotion** is a MERN stack (MongoDB, Express.js, React.js, Node.js) based learning management system where **instructors can create and manage courses** and **students can browse, enroll, and consume course content**. It includes authentication, payment (via Razorpay), rating, and instructor dashboards.

---

## 🧱 Table of Contents

* [Features](#features)
* [Tech Stack](#tech-stack)
* [System Architecture](#system-architecture)
* [Getting Started](#getting-started)
* [API Endpoints](#api-endpoints)
* [Frontend Pages](#frontend-pages)
* [Environment Variables](#environment-variables)
* [Deployment](#deployment)
* [Future Enhancements](#future-enhancements)
* [Contributing](#contributing)
* [License](#license)

---

## ✅ Features

* User registration, login, OTP verification, and password reset via JWT
* Role-based access: **students**, **instructors**, and optional **admin**
* Course listing, detail pages, search, wishlist, and enrollment
* Instructor dashboard with insights (views, enrollments, ratings, income) using Chart.js
* Razorpay integration for payments
* Cloudinary for media uploads (course thumbnails, videos)
* Markdown support for course content authoring
* Redux-based state management, React Hooks, and Tailwind CSS styling

---

## 🛠 Tech Stack

| Component | Technologies                                        |
| --------- | --------------------------------------------------- |
| Frontend  | React.js, Redux, Tailwind CSS, React Hook Form      |
| Backend   | Node.js, Express.js, MongoDB, Mongoose, JWT, Bcrypt |
| Payments  | Razorpay integration                                |
| Media     | Cloudinary                                          |
| Data Viz  | Chart.js (for dashboards)                           |

---

## 🏗 System Architecture

StudyNotion follows a client-server architecture:

* **Frontend**: Single Page Application built with React
* **Backend**: REST API powered by Express.js & Node.js
* **Database**: MongoDB with structured schemas for users and courses
* **Connections**: Authenticated routes secured by JWT, payment flow via Razorpay

---

## 🚀 Getting Started

1. Clone the repository:

   ```bash
   git clone <repo-url>
   cd <repository>
   ```
2. Install backend dependencies:

   ```bash
   cd server
   npm install
   ```
3. Install frontend dependencies in another terminal:

   ```bash
   cd frontend
   npm install
   ```
4. Copy `.env.example` to `.env` in both backend and frontend and fill in keys
5. Start backend:

   ```bash
   cd server
   npm run dev
   ```
6. Start frontend:

   ```bash
   cd frontend
   npm start
   ```
7. Access the app at `http://localhost:3000`

---

## 📄 API Endpoints

| Endpoint                    | Method | Description                           |
| --------------------------- | ------ | ------------------------------------- |
| `/api/auth/signup`          | POST   | Register a new user                   |
| `/api/auth/login`           | POST   | Authenticate and get JWT              |
| `/api/auth/verify-otp`      | POST   | OTP verification                      |
| `/api/auth/forgot-password` | POST   | Reset password flow                   |
| `/api/courses`              | GET    | List all courses                      |
| `/api/courses/:id`          | GET    | Course details                        |
| `/api/courses`              | POST   | Create a new course (Instructor only) |
| `/api/courses/:id`          | PUT    | Update course                         |
| `/api/courses/:id`          | DELETE | Delete course                         |
| `/api/courses/:id/rate`     | POST   | Add rating to a course                |

---

## 🖥 Frontend Pages

### For Students:

* Homepage
* Course List & Course Details
* Wishlist & Cart Checkout
* Enrolled Courses & Progress Tracker
* Profile View & Edit

### For Instructors:

* Instructor Dashboard & Insights
* Course Management (CRUD)
* Profile Management

### (Future Admin scope)

* Platform overview with user, course, and revenue insights
* Admin-level course/instructor management

---

## ⚙️ Environment Variables

Use `.env.example` as a reference. Common variables include:

```
MONGODB_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
RZPAY_KEY_ID=your_razorpay_key_id
RZPAY_KEY_SECRET=your_razorpay_secret
CLOUDINARY_URL=your_cloudinary_config
```

---

## ☁ Deployment

* **Frontend**: Deploy on Vercel or Netlify
* **Backend**: Deploy on platforms like Render, Railway, or Heroku
* **Database**: Host via MongoDB Atlas
* **Media**: Cloudinary

---

## 🔭 Future Enhancements

* Add **Admin panel** for full platform moderation
* Incorporate **video streaming** and live sessions
* Build **subscription models** & recurring payments
* Extend **analytics dashboards** with more data insights
* Fully **multilingual UI support**

---

## 🤝 Contributing

Contributions are welcome! Fork the project, make changes in a feature branch, and submit a pull request for review.

---

