🧭 How to Run This Project (Step-by-Step)

Follow these steps to run the project locally or deploy it on an EC2 instance.

1️⃣ Prerequisites

Make sure you have the following installed:

Git

Docker

Docker Compose

(For cloud deployment) An AWS EC2 instance with Ubuntu

Check installation:

docker --version
docker-compose --version

2️⃣ Clone the Repository
git clone https://github.com/naveedalikhan4177/realtime-chat-docker-ci-cd.git
cd realtime-chat-docker-ci-cd

3️⃣ Project Overview

The application consists of two services:

Frontend → Nginx container serving the chat UI

Backend → Node.js + Socket.IO for real-time messaging

Docker Compose manages both services.

4️⃣ Run the Application Using Docker Compose

Start all services with one command:

docker-compose up -d


Verify containers are running:

docker ps


You should see:

chat-backend

chat-frontend

5️⃣ Access the Application

Open your browser:

Frontend: http://localhost:8080
Backend : http://localhost:5001


(If deployed on EC2, replace localhost with the EC2 public IP.)

Open two browser tabs to test real-time chat.

6️⃣ CI/CD Deployment (Automated)

This project includes a GitHub Actions CI/CD pipeline.

How CI/CD Works:

Every push to the main branch triggers the pipeline

Docker images are built for frontend and backend

Images are pushed to Docker Hub

EC2 instance pulls the latest images

Containers restart automatically using Docker Compose

No manual deployment is required after setup.

7️⃣ Required GitHub Secrets (For CI/CD)

To enable CI/CD, the following GitHub repository secrets must be configured:

DOCKER_USERNAME

DOCKER_PASSWORD (Docker Hub access token)

EC2_HOST

EC2_USER

EC2_KEY

These secrets are used securely by GitHub Actions.

8️⃣ Stop the Application

To stop all running containers:

docker-compose down

🧪 Optional Improvements

Add environment variables using .env

Enable container restart policies

Add health checks

Secure application with HTTPS

Migrate deployment to Kubernetes

🧠 Why This Project Matters

This project demonstrates:

Practical Docker usage

Multi-container orchestration

Real CI/CD automation

Secure cloud deployment

DevOps best practices in action

🔥 WHY THIS SECTION IS IMPORTANT (BRUTAL TRUTH)

Without this:

Your repo looks like a demo

Recruiters can’t run it

Interviewers can’t trust it

With this:

Anyone can reproduce your work

Your repo becomes portfolio-grade

You look like someone who finishes projects properly

✅ WHAT YOU SHOULD DO NOW

Paste this section into your README.md

Commit & push:

git add README.md
git commit -m "Add step-by-step project setup instructions"
git push
