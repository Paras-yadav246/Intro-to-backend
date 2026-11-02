# Intro to Backend Development

A backend RESTful API built with **Node.js**, **Express.js**, and **MongoDB Atlas**. This project implements secure user authentication with password hashing (`bcrypt`) and complete CRUD (Create, Read, Update, Delete) operations following the Model-Route-Controller (MRC) architecture.

---

## 🚀 Features

- **User Authentication**: Secure user registration, login, and logout endpoints with password hashing via `bcrypt`.
- **Full CRUD API**: Create, read, update, and delete posts.
- **Database Integration**: Connected to MongoDB Atlas cloud database with Mongoose schemas and models.
- **Modular MRC Architecture**: Clean separation of concerns across config, models, controllers, and routes.
- **Environment Management**: Secure configuration using `.env`.

---

## 🛠️ Tech Stack

- **Runtime Environment**: Node.js
- **Web Framework**: Express.js
- **Database & ODM**: MongoDB Atlas, Mongoose
- **Security & Authentication**: bcrypt
- **Development Tooling**: nodemon, dotenv

---

## 📁 Project Structure

```text
Intro-to-backend/
├── backend/
│   ├── .env
│   └── src/
│       ├── config/
│       │   ├── constants.js       # App constants
│       │   └── database.js        # MongoDB connection setup
│       ├── controllers/
│       │   ├── post.controller.js # Post CRUD controllers
│       │   └── user.controller.js # Auth controllers (register, login, logout)
│       ├── models/
│       │   ├── post.model.js      # Post Mongoose schema & model
│       │   └── user.model.js      # User schema with bcrypt hooks
│       ├── routes/
│       │   ├── post.route.js      # Post router
│       │   └── user.route.js      # User router
│       ├── app.js                 # Express app configuration & middleware
│       └── index.js               # Server entry point
├── .env                           # Environment variables
├── .gitignore                     # Git ignore rules
├── package.json                   # Dependencies and npm scripts
├── start.bat                      # Quick-launch batch script for Windows
└── README.md                      # Project documentation
```

---

## ⚙️ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- A [MongoDB Atlas](https://www.mongodb.com/atlas) cluster (or local MongoDB instance)

### Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Paras-yadav246/Intro-to-backend.git
   cd Intro-to-backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**:
   Create a `.env` file in the root directory:
   ```env
   PORT=4000
   MONGODB_URI="your_mongodb_connection_string"
   ```

4. **Start the server**:
   ```bash
   npm run dev
   ```
   *(Or on Windows, simply double-click `start.bat`)*

The server will be running on `http://localhost:4000`.

---

## 📡 API Reference

### Authentication Endpoints (`/api/v1/users`)

| Method | Endpoint | Description | Sample Payload |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/v1/users/register` | Register new user | `{"username": "paras", "email": "paras@example.com", "password": "securepassword"}` |
| `POST` | `/api/v1/users/login` | Authenticate user | `{"email": "paras@example.com", "password": "securepassword"}` |
| `POST` | `/api/v1/users/logout` | End user session | `{"email": "paras@example.com"}` |

### Post Endpoints (`/api/v1/posts`)

| Method | Endpoint | Description | Sample Payload |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/v1/posts/create` | Create a post | `{"name": "Post Title", "description": "Post description text", "age": 20}` |
| `GET` | `/api/v1/posts/getPosts` | Retrieve all posts | *None* |
| `PATCH` | `/api/v1/posts/update/:id` | Update post by ID | `{"description": "Updated text"}` |
| `DELETE` | `/api/v1/posts/delete/:id` | Delete post by ID | *None* |

---

## 👨‍💻 Author

**Paras Yadav**
- GitHub: [@Paras-yadav246](https://github.com/Paras-yadav246)
