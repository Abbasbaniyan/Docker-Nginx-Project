# 🐳 Docker Nginx Demo

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Nginx-Web%20Server-009639?style=for-the-badge&logo=nginx&logoColor=white">
  <img src="https://img.shields.io/badge/HTML5-CSS3-JavaScript-orange?style=for-the-badge">
</p>

---

## 📌 Project Overview

This project demonstrates how to **containerize and deploy a static website using Docker and Nginx**.

The application is packaged inside a custom Docker image built from a Dockerfile and served through the lightweight **Nginx Alpine** image.

The project provides hands-on experience with Docker image creation, container deployment, port mapping, Docker logs, and container inspection.

---

# 🚀 Project Architecture

```text
                +----------------------+
                |     Docker Engine    |
                +----------+-----------+
                           |
                    Docker Image
                  docker-nginx-demo
                           |
                    Docker Container
                           |
                 Nginx Web Server
                           |
                    Port Mapping
                     8080  ---> 80
                           |
               http://localhost:8080
```

---

# 🛠 Technologies Used

- Docker
- Nginx
- HTML5
- CSS3
- JavaScript

---

# 📂 Project Structure

```text
Docker-nginx-demo/
│
├── Dockerfile
├── index.html
├── style.css
├── script.js
├── .dockerignore
├── README.md
└── screenshots/
```

---

# ⚙️ Dockerfile

```dockerfile
FROM nginx:alpine

COPY . /usr/share/nginx/html

EXPOSE 80
```

---

# 📦 Build Docker Image

```bash
docker build -t docker-nginx-demo .
```

This command creates a custom Docker image using the Dockerfile.

---

# ▶️ Run Docker Container

```bash
docker run -d --name docker-nginx-demo -p 8080:80 docker-nginx-demo
```

Explanation:

- **-d** → Run container in detached mode
- **--name** → Assign a custom container name
- **-p 8080:80** → Map host port 8080 to container port 80

---

# 🌍 Access the Website

Open your browser and navigate to:

```text
http://localhost:8080
```

The static website is now served directly from the Docker container through the Nginx web server.

---

# 📸 Screenshots

## 1️⃣ Pull Nginx Image

![Pull Nginx](screenshots/01-pull-nginx.png)

---

## 2️⃣ Run Nginx Container

![Run Container](screenshots/02-run-container.png)

---

## 3️⃣ Build Custom Docker Image

![Docker Build](screenshots/03-docker-build.png)

---

## 4️⃣ Verify Docker Images

![Docker Images](screenshots/04-docker-images.png)

---

## 5️⃣ View Docker Logs

![Docker Logs](screenshots/05-docker-logs.png)

---

## 6️⃣ Verify Website Files Inside Container

![Docker Exec](screenshots/06-docker-exec.png)

---

## 7️⃣ Dockerized Website Running Successfully

![Website Output](screenshots/07-website.png)

---

# 🔧 Docker Commands Used

Pull Image

```bash
docker pull nginx:latest
```

View Images

```bash
docker images
```

Build Image

```bash
docker build -t docker-nginx-demo .
```

Run Container

```bash
docker run -d --name docker-nginx-demo -p 8080:80 docker-nginx-demo
```

List Running Containers

```bash
docker ps
```

View Logs

```bash
docker logs docker-nginx-demo
```

Access Running Container

```bash
docker exec -it docker-nginx-demo sh
```

---

# 📖 What I Learned

Through this project I gained practical experience with:

- Docker Images
- Docker Containers
- Dockerfile
- Nginx Web Server
- Port Mapping
- Building Custom Images
- Container Deployment
- Docker Logs
- Docker Exec
- Docker Image Management
- Static Website Deployment using Docker

---

# 🎯 Key Features

✅ Custom Docker Image

✅ Dockerfile Implementation

✅ Lightweight Nginx Alpine Image

✅ Static Website Deployment

✅ Port Mapping

✅ Docker Logs

✅ Container File Verification

✅ Browser Testing

---

# 📈 Future Enhancements

- Docker Compose
- Docker Volumes
- Docker Networks
- Multi-Container Deployment
- CI/CD Integration using Jenkins
- AWS EC2 Deployment

---

# 💼 Resume Highlights

- Built and deployed a Dockerized static website using Docker and Nginx.
- Created a custom Docker image using Dockerfile.
- Implemented container deployment with port mapping.
- Verified container execution using Docker logs and Docker exec.
- Gained practical experience with Docker image management and container lifecycle.

---

# 👨‍💻 Author

## Abbas Baniyan

AWS Cloud & DevOps Engineer

### Skills

- AWS
- Docker
- Linux
- Git & GitHub
- Jenkins
- Nginx

---

## ⭐ If you found this project helpful, consider giving it a Star.
