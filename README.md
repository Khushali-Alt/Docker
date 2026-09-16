# 🐳 Docker Practice

A hands-on **Docker learning and practice repository** focused on containerizing full-stack applications and understanding Docker fundamentals through real implementation.

This repository contains Dockerized **Backend** and **Frontend** applications, along with Dockerfiles, ignore files, and practical commands used while learning containerization.

---

## 📌 Project Overview

The goal of this repository is to learn and practice how Docker can be used to:

* Containerize applications
* Build custom Docker images
* Run applications inside containers
* Map container ports to the local machine
* Manage dependencies inside containers
* Work with Dockerfiles
* Understand Docker build and run workflows
* Prepare full-stack applications for containerized environments

---

## 🏗️ Project Structure

```text
Docker_Practice/
│
├── Backend/
│   ├── Dockerfile
│   ├── .dockerignore
│   ├── .gitignore
│   ├── index.js
│   ├── package.json
│   └── package-lock.json
│
├── Frontend/
│   ├── Dockerfile
│   ├── .dockerignore
│   ├── .gitignore
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
└── README.md
```

---

## ⚙️ Technologies Used

### Backend

* Node.js
* Express.js
* PostgreSQL (`pg`)
* Docker

### Frontend

* React
* Vite
* JavaScript
* Docker

### DevOps / Tools

* Docker
* Dockerfile
* Git
* GitHub
* Linux / Fedora

---

# 🐳 Docker Concepts Practiced

This repository focuses on practical Docker concepts including:

### 1. Docker Images

Creating custom images from Dockerfiles.

```bash
docker build -t express-app .
```

### 2. Docker Containers

Running applications inside isolated containers.

```bash
docker run express-app
```

### 3. Port Mapping

Mapping a container port to a host port.

```bash
docker run -p 4000:3000 express-app
```

Here:

```text
4000 → Host machine
3000 → Docker container
```

### 4. Environment Variables

Passing configuration to containers.

```bash
docker run -p 4000:3000 -e PORT=3000 express-app
```

### 5. Dockerfile

Example backend Dockerfile:

```dockerfile
FROM node:24.14.0-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

ENV PORT=3000

EXPOSE 3000

CMD ["node", "index.js"]
```

---

# 🚀 Running the Backend

Navigate to the backend directory:

```bash
cd Backend
```

Build the Docker image:

```bash
docker build -t express-app .
```

Run the container:

```bash
docker run -p 4000:3000 -e PORT=3000 express-app
```

The backend will be available at:

```text
http://localhost:4000
```

---

# 🎨 Running the Frontend

Navigate to the frontend directory:

```bash
cd Frontend
```

Build the frontend Docker image:

```bash
docker build -t frontend-app .
```

Run the container:

```bash
docker run -p 5173:5173 frontend-app
```

The frontend can then be accessed through the mapped local port.

> The exact port depends on the port configured in the frontend Dockerfile/Vite configuration.

---

# 🔍 Useful Docker Commands

### Check Docker version

```bash
docker --version
```

### Check running containers

```bash
docker ps
```

### Check all containers

```bash
docker ps -a
```

### List images

```bash
docker images
```

### Build an image

```bash
docker build -t <image-name> .
```

### Run a container

```bash
docker run <image-name>
```

### Run with port mapping

```bash
docker run -p <host-port>:<container-port> <image-name>
```

### Stop a container

```bash
docker stop <container-id>
```

### Remove a container

```bash
docker rm <container-id>
```

### Remove an image

```bash
docker rmi <image-name>
```

### View container logs

```bash
docker logs <container-id>
```

---

# 🧠 Learning Journey

This repository is being developed as a practical Docker learning environment.

The learning progression includes:

```text
Docker Basics
     ↓
Images
     ↓
Containers
     ↓
Dockerfile
     ↓
Port Mapping
     ↓
Environment Variables
     ↓
Backend Containerization
     ↓
Frontend Containerization
     ↓
Full-Stack Containerization
     ↓
Docker Compose
     ↓
Production Deployment
```

---

# 🎯 Goals

The main goals of this repository are:

* Build a strong foundation in Docker
* Understand container-based application deployment
* Containerize full-stack applications
* Learn Docker networking and volumes
* Practice Docker Compose
* Integrate Docker into full-stack development workflows
* Build a foundation for DevOps and cloud deployment

---

# 📚 What I'm Practicing

```text
✅ Docker installation and setup
✅ Docker images
✅ Docker containers
✅ Docker commands
✅ Dockerfile
✅ .dockerignore
✅ Port mapping
✅ Environment variables
✅ Node.js application containerization
✅ Express.js backend containerization
✅ React/Vite frontend containerization
🔄 Docker Compose
🔄 Docker networking
🔄 Volumes
🔄 Multi-container applications
🔄 CI/CD integration
```

---

## 👩‍💻 Author

**Khushali Tiwari**

B.Tech CSE | Full-Stack Development | AI & Cloud/DevOps Enthusiast

GitHub: **[@Khushali-Alt](https://github.com/Khushali-Alt)**

---

## ⭐ Purpose

This repository is primarily created for **learning, experimentation, and hands-on practice with Docker and containerization**.

> Learning Docker by building, breaking, debugging, and rebuilding. 🐳
