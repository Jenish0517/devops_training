# 📘 Docker Compose, Networks & Volumes – Learning Summary

## 📖 About This Learning

Today, I learned how to manage multi-container applications using **Docker Compose**. I also explored how Docker handles **networking** and **data persistence** using Docker networks and volumes.

Through this practice, I understood how multiple containers can communicate with each other and how data can be stored outside containers to persist even after containers stop or are removed.

---

## 🧠 Concepts Learned

### 🐳 Docker Compose

- What is Docker Compose
    
- Managing multi-container applications
    
- Writing a **docker-compose.yml** file
    
- Starting and stopping services using Compose
    

### 🌐 Docker Networks

Learned different Docker network drivers:

- **Bridge Network** – Default network used for communication between containers on the same host.
    
- **Host / General Networking** – Container shares the host's networking stack.
    
- **None Network** – Container runs without network access.
    

Commands practiced:

docker network ls  
docker network create <network-name>

---

### 💾 Docker Volumes

- What are Docker volumes
    
- Why volumes are used for **persistent data**
    
- How containers store data outside the container filesystem
    

Commands practiced:

docker volume ls  
docker volume create <volume-name>

---

## ⚙️ Docker Compose Example

Example `docker-compose.yml` structure learned:

version: "3"  
  
services:  
  web:  
    image: nginx  
    ports:  
      - "8080:80"  
  
  database:  
    image: mysql

---

## 🎯 Learning Outcome

- Learned how to run multiple containers using Docker Compose
    
- Understood container networking concepts
    
- Learned how Docker networks allow containers to communicate
    
- Understood how Docker volumes help persist data
    
- Gained hands-on experience managing containers using Compose
    

---