# Exercise 1: Your First Container

Welcome to your first hands-on Docker exercise! In this lab, you'll run your first container and understand the basics of container lifecycle.

## ? Objectives

By completing this exercise, you will:
- Run your first Docker container
- Understand container states and lifecycle
- Learn basic container management commands
- Practice with container inspection and logs

## ? Prerequisites

- Docker installed and running
- Basic command line knowledge
- Access to a terminal/command prompt

## ? Exercise Steps

### Step 1: Verify Docker Installation

First, let's make sure Docker is properly installed and running:

```bash
# Check Docker version
docker --version

# Verify Docker is running
docker info

# Test with hello-world
docker run hello-world
```

**Expected Output:**
```
Hello from Docker!
This message shows that your installation appears to be working correctly.
```

### Step 2: Run Your First Interactive Container

Let's run a Ubuntu container and interact with it:

```bash
# Run Ubuntu container interactively
docker run -it ubuntu:latest bash

# Inside the container, try these commands:
whoami
cat /etc/os-release
ls -la
echo "Hello from inside the container!"

# Exit the container
exit
```

### Step 3: Run Container in Background

Now let's run a container in detached mode (background):

```bash
# Run nginx web server in background
docker run -d --name my-nginx -p 8080:80 nginx:latest

# Check if container is running
docker ps

# Test the web server
curl http://localhost:8080
# Or open http://localhost:8080 in your browser
```

### Step 4: Container Management

Practice managing your containers:

```bash
# List all containers (running and stopped)
docker ps -a

# View container logs
docker logs my-nginx

# Inspect container details
docker inspect my-nginx

# Execute command in running container
docker exec -it my-nginx bash

# Inside nginx container:
ls /usr/share/nginx/html
cat /usr/share/nginx/html/index.html
exit

# Stop the container
docker stop my-nginx

# Start it again
docker start my-nginx

# Remove the container (stop first if running)
docker stop my-nginx
docker rm my-nginx
```

### Step 5: Working with Images

Understanding the relationship between images and containers:

```bash
# List local images
docker images

# Pull an image without running
docker pull alpine:latest

# Run alpine container
docker run -it alpine:latest sh

# Inside alpine:
apk update
apk add curl
curl --version
exit

# See the difference in image layers
docker history alpine:latest
```

## ? Challenge Tasks

Once you've completed the basic steps, try these challenges:

### Challenge 1: Multi-Container Setup
1. Run a MySQL database container
2. Run a WordPress container linked to the database
3. Access WordPress through your browser

```bash
# MySQL container
docker run -d --name mysql-db \
  -e MYSQL_ROOT_PASSWORD=rootpassword \
  -e MYSQL_DATABASE=wordpress \
  -e MYSQL_USER=wordpress \
  -e MYSQL_PASSWORD=wordpress \
  mysql:5.7

# WordPress container
docker run -d --name wordpress-site \
  -p 8080:80 \
  --link mysql-db:mysql \
  -e WORDPRESS_DB_HOST=mysql:3306 \
  -e WORDPRESS_DB_USER=wordpress \
  -e WORDPRESS_DB_PASSWORD=wordpress \
  -e WORDPRESS_DB_NAME=wordpress \
  wordpress:latest

# Access WordPress at http://localhost:8080
```

### Challenge 2: Container Persistence
1. Create a container with a volume
2. Write data to the volume
3. Delete the container and create a new one
4. Verify the data persists

```bash
# Create volume
docker volume create my-data

# Run container with volume
docker run -it --name data-container \
  -v my-data:/data \
  ubuntu:latest bash

# Inside container:
echo "This data should persist" > /data/myfile.txt
exit

# Remove container
docker rm data-container

# Create new container with same volume
docker run -it --name new-container \
  -v my-data:/data \
  ubuntu:latest bash

# Check if data persists:
cat /data/myfile.txt
exit
```

## ? Completion Checklist

Mark each task as completed:

- [ ] Successfully ran hello-world container
- [ ] Ran interactive Ubuntu container
- [ ] Started nginx in background
- [ ] Managed container lifecycle (start/stop/remove)
- [ ] Inspected container logs and details
- [ ] Executed commands in running container
- [ ] Worked with Docker images
- [ ] **Challenge 1**: Set up multi-container application
- [ ] **Challenge 2**: Demonstrated data persistence with volumes

## ? Next Steps

Congratulations! You've completed your first Docker exercise. You're now ready for:

1. **Exercise 2**: Building Your First Docker Image
2. **Exercise 3**: Writing Effective Dockerfiles
3. **Module 2**: Advanced Container Management

## ? Troubleshooting

### Common Issues

**Issue**: "Docker daemon not running"
**Solution**: Start Docker Desktop or Docker service

**Issue**: "Port already in use"
**Solution**: Use a different port or stop the conflicting service

**Issue**: "Permission denied"
**Solution**: Add your user to docker group (Linux) or run as administrator (Windows)

### Useful Commands for Debugging

```bash
# View system-wide Docker info
docker system info

# Check Docker resource usage
docker system df

# Clean up unused containers and images
docker system prune

# View real-time container stats
docker stats
```

## ? Additional Resources

- [Docker Official Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Docker Best Practices](https://docs.docker.com/develop/dev-best-practices/)

---

*Exercise created by: Docker Workshop Portal Team*
*Estimated completion time: 30-45 minutes*