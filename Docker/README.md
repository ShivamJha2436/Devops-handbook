# 🐳 Docker

Docker is one of the most important tools in modern DevOps. It allows developers and operations teams to package applications into **lightweight, portable containers** that run the same way on any machine.

---

## 1. Before Docker

- **Physical Servers** → Each application ran on its own machine. Expensive, hard to scale, and often underutilized.  
- **Virtual Machines (VMs)** → Multiple apps could run on a single physical machine using virtualization. More efficient, but still heavy: every VM had a full OS, slow startup times, and high resource usage.  
- **Configuration Tools** → Tools like Ansible, Puppet, and Chef automated setup. Helpful, but applications still failed with the infamous:  
  > *“It works on my machine, but not on yours.”*

**Docker solved this problem.**  
It provided a way to package applications and all their dependencies into containers that can run **anywhere, consistently.**

---

## 2. Why Docker?

- 🚀 **Lightweight** → shares the host OS kernel, unlike VMs.  
- 📦 **Portable** → runs the same on laptops, servers, or cloud.  
- ⚡ **Fast startup** → containers launch in seconds.  
- 🔁 **Scalable** → containers can be replicated easily and orchestrated with tools like Kubernetes.  
- ✅ **Consistent** → no more “works on dev, fails in prod.”  

---

## 3. How Docker Works (Simple View)

- **Image** → A blueprint (like a recipe).  
- **Container** → A running instance of an image (like a meal cooked from the recipe).  
- **Docker Engine** → The runtime that manages containers.  
- **Dockerfile** → A text file with instructions to build an image.  

Under the hood, Docker relies on Linux kernel features like **namespaces** (isolation), **cgroups** (resource limits), and **layered filesystems** (efficient storage).  

---

## 4. What You’ll Learn Here

- [Tutorials](./tutorials.md) → Step-by-step learning path (beginner to advanced).  
- [Cheat Sheet](./cheat_sheets.md) → Quick reference for daily Docker use.  
- [Best Practices](./best_practices.md) → How professionals use Docker safely and efficiently.  

---

## 5. Resources

- 📖 [Official Docker Docs](https://docs.docker.com/)  
- 🎓 [Docker Curriculum](https://docker-curriculum.com/)  
- 🎥 [Docker in 7 Minutes](https://www.youtube.com/watch?v=pGYAg7TMmp0)  
- 🛠 [Play With Docker (Free Hands-On Lab)](https://labs.play-with-docker.com/)  
- 📘 [Containers vs VMs](https://www.docker.com/resources/what-container/)  

---
