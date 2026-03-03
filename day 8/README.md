# 📘 Docker – Images, Containers & Networking Practice

## 📖 About This Learning

Today, I learned more advanced Docker concepts including creating a **Dockerfile**, building custom images, running containers, exposing applications through a device IP, monitoring container usage, and working with Docker networks.

This helped me understand how applications are containerized and made accessible over a network.

---

## 🧠 Concepts Learned

- What is a Dockerfile
    
- How Docker builds images from instructions
    
- Running containers with port mapping
    
- Exposing applications using device IP
    
- Monitoring container resource usage
    
- Docker networking basics
    

---

## 🐳 Commands Practiced

### 🔹 Build Docker Image

docker build -t my-app .

### 🔹 Run Container with Port Mapping

docker run -d -p 8080:81 my-app

Accessed in browser using:

http://<device-ip>:8080

---

### 🔹 View Running Containers

docker ps

### 🔹 Monitor Resource Usage

docker stats

### 🔹 Docker Networks

docker network ls  
docker network create my-network

---

## 📝 What I Practiced

- Created a Dockerfile for a simple application
    
- Built a custom Docker image
    
- Ran a container and mapped ports
    
- Accessed the application in Chrome using device IP
    
- Monitored CPU and memory usage with `docker stats`
    
- Created and listed Docker networks
    

---