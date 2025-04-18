# 🐳 Docker Cheat Sheet

A quick reference to essential Docker commands and tips.

---

## 📦 Docker Basics

```bash
docker --version              # Check Docker version
docker info                   # Show system-wide info
docker help                   # Show help for Docker



⸻

🔧 Images

docker build -t name:tag .     # Build image from Dockerfile
docker images                  # List images
docker rmi <image>             # Remove image
docker pull <image>            # Download image
docker push <image>            # Push image to registry



⸻

🏃‍♂️ Containers

docker run -it <image>             # Run container interactively
docker run -d <image>              # Run container in background
docker run --name <name> <image>   # Name your container
docker exec -it <container> sh     # Access running container shell
docker ps                          # List running containers
docker ps -a                       # List all containers
docker stop <container>            # Stop a container
docker start <container>           # Start a container
docker restart <container>         # Restart a container
docker rm <container>              # Remove a container



⸻

📁 Volumes

docker volume create <name>          # Create a volume
docker volume ls                     # List volumes
docker run -v <vol_name>:/data ...   # Mount volume
docker volume rm <name>              # Remove volume



⸻

🕸️ Networks

docker network ls                    # List networks
docker network create <name>         # Create network
docker network connect <net> <cont>  # Connect container to network
docker network rm <name>             # Remove network



⸻

🧰 Docker Compose

docker-compose up                    # Start all services
docker-compose up -d                 # Start in detached mode
docker-compose down                  # Stop and remove containers
docker-compose build                 # Build or rebuild services
docker-compose logs                  # View logs

Example docker-compose.yml:

version: '3'
services:
  web:
    image: nginx
    ports:
      - "8080:80"



⸻

🔍 Useful Commands

docker logs <container>              # View logs
docker top <container>               # View running processes
docker stats                         # View usage stats
docker inspect <container/image>     # Detailed info
docker cp <container>:path hostpath  # Copy from container



⸻

🧹 Cleanup

docker system prune                  # Remove unused data
docker container prune               # Remove stopped containers
docker image prune                   # Remove unused images
docker volume prune                  # Remove unused volumes



⸻

🛠️ Dockerfile Example

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN npm install
CMD ["npm", "start"]



⸻

✅ Best Practices
	•	Use .dockerignore to exclude files during build.
	•	Tag your images with version (myapp:1.0).
	•	Keep images small with multi-stage builds.
	•	Use health checks in Docker Compose.
