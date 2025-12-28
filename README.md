# Realtime Chat App – Docker & CI/CD

A full-stack real-time chat application built with **Node.js and Socket.IO**, containerized using **Docker**, orchestrated with **Docker Compose**, and deployed automatically to **AWS EC2** using **GitHub Actions CI/CD**.

This project demonstrates practical DevOps skills: containerization, automation, and cloud deployment.

---

## 🛠 Tools & Technologies Used

- **Frontend**: HTML, JavaScript, Nginx  
- **Backend**: Node.js, Express, Socket.IO  
- **Containerization**: Docker  
- **Orchestration**: Docker Compose  
- **CI/CD**: GitHub Actions  
- **Container Registry**: Docker Hub  
- **Cloud Platform**: AWS EC2 (Ubuntu)  
- **Version Control**: Git & GitHub  

---

## 📦 Project Structure

realtime-chat-docker-ci-cd/
├── backend/ # Node.js backend (Socket.IO)
├── frontend/ # Nginx-based frontend
├── docker-compose.yml
└── .github/workflows # GitHub Actions CI/CD

yaml
Copy code

---

## 🔄 CI/CD Workflow (How It Works)

On every push to the `main` branch:

1. GitHub Actions builds Docker images  
2. Images are pushed to Docker Hub  
3. Pipeline connects to EC2 via SSH  
4. Docker Compose pulls latest images  
5. Containers restart automatically  

👉 **No manual deployment required**

---

## 🚀 Deployment

- Deployed on **AWS EC2**
- Multi-container setup using Docker Compose
- Application accessible via EC2 public IP

Frontend: http://<EC2_PUBLIC_IP>:8080
Backend : http://<EC2_PUBLIC_IP>:5001

yaml
Copy code

---

## 🎯 What This Project Shows

- Real-world Docker usage (not just Dockerfiles)
- Multi-container application design
- End-to-end CI/CD pipeline implementation
- Secure deployment using GitHub Secrets
- Practical cloud deployment experience

---

## 👤 Author

**Naveed Ali Khan**  
GitHub: https://github.com/naveedalikhan4177
