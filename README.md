# **🎮 Game Frontend Project (Dockerized)**

## **🚀 Tech Stack**

* React (Vite)  
* Docker  
* Nginx

---

## **📦 Project Setup**

### **1️⃣ Clone Repository**
```
git clone https://github.com/SACHIN-ST3/Game_Frontend_Project.git:
```
```
cd game-frontend-project
```
---

### **2️⃣ Run Without Docker**
```
npm install
```
```
npm run dev
```
App runs on: [http://localhost:5173](http://localhost:5173/)

---

### **3️⃣ Run With Docker 🐳**

#### **Build Image**
```
docker build -t game-frontend .
```
#### **Run Container**
```
docker run -d -p 8080:80 game-frontend
```
App runs on: [http://localhost:8080](http://localhost:8080/)

---

## **🧠 Concept**

This project uses a **multi-stage Docker build**:

* Node.js → Build React app  
* Nginx → Serve static files

---

## **📌 Author**

Sachin Rawat

