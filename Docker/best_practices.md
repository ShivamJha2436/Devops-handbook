# 📚 Docker Tutorials

This guide takes you from **zero to advanced**, with practical examples.

---

## Beginner

### Step 1: Install Docker
- [Linux Install Guide](https://docs.docker.com/engine/install/)  
- [Docker Desktop for Windows/Mac](https://docs.docker.com/desktop/)  

### Step 2: Run Your First Container
```bash
docker run hello-world
```

👉 This pulls the hello-world image and runs a container that prints a message.

### Step 3: Run a Web Server
```bash
docker run -d -p 8000:80 nginx
```
Now open http://localhost:8080 → you’re serving a website with just one command!

## Intermediate

### Dockerfile Basics
A Dockerfile is a recipe for building images. Example for a Python app:
```dockerfile
FROM python:3.9
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "app.py"]
```