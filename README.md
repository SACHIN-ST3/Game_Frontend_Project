# 🎮 Game Frontend Project (Dockerized)

## 🚀 Tech Stack

* React (Vite)
* Docker
* Nginx

---

## 📦 Project Setup

### 1️⃣ Clone Repository

```bash
git clone https://github.com/SACHIN-ST3/Game_Frontend_Project.git
```
```
cd Game_Frontend_Project
```

---

### 2️⃣ Run Without Docker (Development Mode)

```bash
npm install
```
```
npm run dev
```

👉 App runs on: http://localhost:5173

---

### 3️⃣ Run With Docker 🐳 (Production Mode)

#### Build Image

```bash
docker build -t game-frontend .
```

#### Run Container

```bash
docker run -d -p 8080:80 game-frontend
```

👉 App runs on: http://localhost:8080

---

## 🧠 Concept

This project uses a **multi-stage Docker build**:

* Node.js → Build the React application
* Nginx → Serve static files efficiently

---

## 📁 Project Structure

```
├── src/
├── public/
├── Dockerfile
├── package.json
├── vite.config.js
```

---

## 📌 Author

Sachin Rawat

---
