# 🚀 Fullstack CRUD Application with Docker & CI/CD

A production-ready fullstack CRUD application built using Angular, Node.js, MongoDB, Docker, and Jenkins CI/CD.

This project demonstrates complete containerization, automated deployment, and real-world DevOps practices.

---

## 📌 Project Overview

This application allows users to:

- Create tutorials
- View tutorials
- Update tutorials
- Delete tutorials

The entire system is fully containerized and automatically deployed using a CI/CD pipeline.

---

## 🏗️ Architecture

Browser  
↓  
Frontend (Angular + Nginx Container)  
↓  
Backend (Node.js + Express Container)  
↓  
MongoDB (Database Container)  

All services run inside Docker containers.

---

## 🐳 Docker Implementation

### 🔹 Backend
- Node.js (Express)
- MongoDB connection
- CORS enabled
- Multi-stage Docker build
- Exposed on port 8080

### 🔹 Frontend
- Angular production build
- Served via Nginx
- Multi-stage Dockerfile
- Runs on port 80

### 🔹 Docker Compose
Used to orchestrate:
- Frontend container
- Backend container

Production deployment uses Docker Hub images.

---

## 🔁 CI/CD Pipeline (Jenkins)

The pipeline consists of 4 automated stages:

### 🟢 Stage 1 – Code Clone
Clones latest source code from GitHub repository.

### 🟢 Stage 2 – Build Docker Images
Builds:
- Backend Docker image
- Frontend Docker image

### 🟢 Stage 3 – Push to Docker Hub
Pushes newly built images to Docker Hub registry.

### 🟢 Stage 4 – Deploy
Pulls latest images and redeploys containers using Docker Compose.

---

## 🔔 Automated Trigger (Webhook Integration)

A GitHub Webhook is configured with Jenkins.

Whenever changes are pushed to the GitHub repository:
- Jenkins automatically triggers the pipeline
- New Docker images are built
- Images are pushed to Docker Hub
- Application is automatically redeployed

This ensures continuous integration and continuous deployment without manual intervention.

---

## 🌐 Live Application

You can access the live application here: http://35.208.126.145/tutorials
