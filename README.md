# 3-Tier Full Stack Application with Docker & NGINX

A production-style **3-tier architecture** project built using:

* **Frontend**: React
* **Backend**: Node.js + Express
* **Database**: MongoDB
* **Reverse Proxy**: NGINX
* **Containerization**: Docker & Docker Compose

---

## Architecture

```
Client (Browser)
       ↓
   NGINX (Reverse Proxy)
       ↓
 ┌───────────────┬───────────────┐
 │               │               │
Frontend      Backend        MongoDB
(React)      (Node API)      (Database)
```

---

## Features

*  NGINX Reverse Proxy routing
*  Dockerized multi-container setup
*  Inter-container communication via Docker network
*  REST API integration (`/api/users`)
*  Environment variables using `.env`
*  Secure `.env` handling using `.gitignore`
*  MongoDB integration with Mongoose

---

## Tech Stack

* React.js
* Node.js + Express
* MongoDB
* NGINX
* Docker
* Docker Compose

---

## Getting Started

### Clone Repository

```bash
git clone <your-repo-url>
cd project-folder
```

---

### Setup Environment Variables

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongo_connection_string
```

---

### Run with Docker

```bash
docker-compose up --build
```

---

###  Access Application

* Frontend → http://localhost:8081
* API → http://localhost:8081/api/users

---

## Important Learnings

* Fixed **NGINX reverse proxy path issue** (`/api` stripping bug)
* Understood **Docker networking between services**
* Handled **environment variable security**
* Debugged **real-world container logs**

---

## Security Best Practices

* `.env` file excluded using `.gitignore`
* Added `.env.example` for safe sharing
* No secrets committed to GitHub

---

## Future Improvements

*  Add JWT Authentication
*  Deploy on AWS / Render
*  CI/CD Pipeline (GitHub Actions)
*  Logging & Monitoring

Thanks!!!