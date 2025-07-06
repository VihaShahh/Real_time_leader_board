````markdown
# 🏆 Real-Time Leaderboard System

A powerful backend service to manage dynamic, **real-time leaderboards** across multiple games — built by [Viha Shah](https://github.com/VihaShahh) using modern backend technologies for performance, security, and scalability.

🔗 **Live Project URL**: [roadmap.sh project link](https://roadmap.sh/projects/realtime-leaderboard-system)  
📂 **GitHub Repo**: [github.com/VihaShahh/Real_time_leader_board](https://github.com/VihaShahh/Real_time_leader_board)

---

## 📌 Overview

This system allows users to sign up, log in, submit scores, and compete in real-time. It features **JWT authentication**, **role-based access**, **WebSocket live updates**, and a **Redis-powered leaderboard** engine. Whether you're building a competitive game or gamifying your app — this backend has you covered.

---

## 🚀 Core Features

### 🔐 Authentication & Authorization
- JWT-based access + refresh token flow
- Bcrypt-secured password hashing
- Role-based access control (admin/user)
- Redis-backed session management

### 👥 User & Social System
- Full CRUD for user profiles
- Friend request system (send, accept, reject)
- Private real-time messaging
- Unread/read tracking for messages

### 🎮 Game & Score Management
- Create/edit/delete games (admin only)
- Submit scores & track history
- Real-time leaderboard updates via WebSockets
- Filter scores by date, top player reporting

### 📊 Leaderboards & Rankings
- Global and game-specific leaderboards
- Top player ranking with Redis optimization
- Dynamic score updates with WebSocket integration
- Filtering by date ranges, users, or game titles

### 🛡️ Robust API Security
- Rate limiting for abuse prevention
- Custom exception handling
- Consistent API responses and request validation

---

## ⚙️ Tech Stack

| Layer        | Technology                     |
|--------------|---------------------------------|
| Language     | TypeScript                      |
| Backend      | Node.js, NestJS, TypeORM        |
| Database     | PostgreSQL                      |
| Caching      | Redis                           |
| Auth System  | Passport.js, JWT                |
| Real-Time    | WebSocket                       |
| Dev Tools    | Docker, Postman, .env config    |

---

## 🛠️ Installation Guide

### Prerequisites
- Node.js & npm
- PostgreSQL
- Redis
- Docker (optional for containerization)

### 🔧 Setup Steps

1. **Clone the repo**  
   ```bash
   git clone https://github.com/VihaShahh/Real_time_leader_board.git
   cd Real_time_leader_board
````

2. **Configure environment**
   Create a `.env` file with your database and JWT credentials:

   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_USERNAME=your_db_user
   DB_PASSWORD=your_db_password
   DB_DATABASE=leaderboard_db

   JWT_SECRET=your_jwt_secret
   ACCESSTOKEN_LIFETIME=3600
   REFRESHTOKEN_LIFETIME=86400
   REFRESH_TOKEN_SECRET=another_secret

   REDIS_HOST=localhost
   REDIS_PORT=6379
   REDIS_PASSWORD=your_redis_password
   ```

3. **Install dependencies**

   ```bash
   npm install
   ```

4. **Start the server**

   ```bash
   npm run start:dev
   ```

5. **Visit**:
   [http://localhost:3000](http://localhost:3000)

---

## 📡 API Endpoints

### ✅ Auth

| Method | Endpoint             | Description            |
| ------ | -------------------- | ---------------------- |
| POST   | `/auth/signup`       | Register new user      |
| POST   | `/auth/login`        | Log in                 |
| POST   | `/auth/refreshToken` | Refresh access token   |
| POST   | `/auth/logout`       | Log out user           |
| GET    | `/auth/protected`    | Protected route access |

### 👤 User

| Method | Endpoint              | Description                      |
| ------ | --------------------- | -------------------------------- |
| GET    | `/user`               | Get user by email                |
| PATCH  | `/user/:id`           | Update user                      |
| DELETE | `/user/:id`           | Delete user                      |
| GET    | `/user/me`            | Get current user info            |
| GET    | `/user/ranking`       | Get user’s game-specific ranking |
| GET    | `/user/ranking/:game` | Top players for a specific game  |

### 🎮 Game

| Method | Endpoint    | Description         |
| ------ | ----------- | ------------------- |
| POST   | `/game`     | Create game (admin) |
| GET    | `/game/:id` | Get game by ID      |
| GET    | `/game`     | Search game by name |
| PATCH  | `/game/:id` | Update game         |
| DELETE | `/game/:id` | Delete game         |

### 🧾 Score

| Method | Endpoint             | Description                       |
| ------ | -------------------- | --------------------------------- |
| POST   | `/score`             | Submit score for a game           |
| GET    | `/score`             | Get top scores for a game         |
| GET    | `/score/top-players` | Report top players (with filters) |

### 🏆 Leaderboard

| Method | Endpoint            | Description               |
| ------ | ------------------- | ------------------------- |
| GET    | `/leaderboard`      | Global leaderboard        |
| GET    | `/leaderboard/game` | Game-specific leaderboard |

---

📍 India
🔗 [LinkedIn](https://www.linkedin.com/in/viha-shah/) | 🐙 [GitHub](https://github.com/VihaShahh)

---
```
