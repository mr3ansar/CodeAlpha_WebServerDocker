## 🐳 CodeAlpha — Task 4: Web Server using Docker

A simple web server deployed inside a **Docker container** using **Nginx**, built as part of the CodeAlpha DevOps Internship Program.

---

## 📌 Task Overview

This project demonstrates the core concepts of Docker containerization by:

- Building a Docker image from a custom `Dockerfile`
- Deploying a web server (Nginx) inside a container
- Managing the container lifecycle (start, stop, restart, remove)
- Monitoring container health and logs
- Following container-based deployment best practices

---

## 🗂️ Project Structure

```
CodeAlpha_WebServerDocker/
├── index.html            # Web page served by Nginx
├── Dockerfile            # Instructions to build the Docker image
├── docker-compose.yml    # Container run configuration
└── README.md             # Project documentation
```

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Docker | Containerization platform |
| Nginx (Alpine) | Lightweight web server |
| Docker Compose | Container orchestration |
| GitHub Codespaces | Cloud development environment |
| HTML/CSS | Web page content |

---

## 🚀 Getting Started

### Prerequisites
- Docker installed (or use [GitHub Codespaces](https://github.com/features/codespaces) / [Play with Docker](https://labs.play-with-docker.com))
- Git installed

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/CodeAlpha_WebServerDocker.git
cd CodeAlpha_WebServerDocker
```

### 2. Build the Docker Image

```bash
docker build -t codealpha-webserver .
```

### 3. Run the Container

```bash
docker run -d -p 8080:80 --name codealpha_webserver codealpha-webserver
```

### 4. Access the Web Server

Open your browser and go to:

```
http://localhost:8080
```

---

## 🐙 Using Docker Compose (Alternative)

```bash
# Start the container
docker-compose up -d

# Stop the container
docker-compose down
```

---

## 🧪 Useful Docker Commands

```bash
# View running containers
docker ps

# View container logs
docker logs codealpha_webserver

# Monitor container resource usage
docker stats codealpha_webserver

# Stop the container
docker stop codealpha_webserver

# Start the container again
docker start codealpha_webserver

# Remove the container
docker rm -f codealpha_webserver

# Remove the image
docker rmi codealpha-webserver
```

---

## 📄 Dockerfile Explained

```dockerfile
# Pull official lightweight Nginx image
FROM nginx:alpine

# Copy our HTML file into Nginx's web directory
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80 for web traffic
EXPOSE 80

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]
```

---

## 💡 Key Concepts Learned

- **Docker Images** — Blueprints for creating containers
- **Docker Containers** — Running instances of images
- **Port Mapping** — Connecting host ports to container ports (`-p 8080:80`)
- **Container Lifecycle** — Build → Run → Stop → Remove
- **Docker Compose** — Managing multi-container setups with a YAML file
- **Nginx** — Serving static web content inside a container

---

## 📸 Screenshots

> *(Add your screenshots here after running the project)*

- Browser showing the deployed web page
- `docker ps` output showing running container
- `docker stats` output showing container metrics

---

## 👤 Author

**Your Name**
- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [your-linkedin](https://linkedin.com/in/your-linkedin)

---

## 🏢 Internship

This project was completed as part of the **CodeAlpha DevOps Internship Program**.

- 🌐 Website: [www.codealpha.tech](https://www.codealpha.tech)
- 📧 Email: services@codealpha.tech

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).