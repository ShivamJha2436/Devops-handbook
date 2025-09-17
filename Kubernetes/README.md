# Kubernetes Module

Kubernetes (often abbreviated as **K8s**) is the de facto standard for container orchestration.  
It was originally designed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF).  

This module is designed to give you:
- A **conceptual understanding** of why Kubernetes exists.
- A **practical guide** to creating and managing clusters, pods, deployments, and services.
- **Cheat sheets** for day-to-day productivity.
- **Helm guides** to package and manage applications at scale.
- **Labs** to practice real-world scenarios.

---

## 🌍 Why Kubernetes?
Before Kubernetes, teams used manual scripts or tools like **Docker Compose** to manage containers. This worked fine for a few containers, but became unmanageable when applications scaled into hundreds or thousands of services. Problems included:
- Restarting crashed containers.
- Scaling applications up/down automatically.
- Networking and load balancing across multiple hosts.
- Managing updates without downtime.

Kubernetes solves these by:
- **Automated container scheduling**.
- **Self-healing** (restarts failed containers).
- **Horizontal scaling** (based on load).
- **Service discovery and networking**.
- **Declarative deployments** and rollbacks.

---

## 📂 Folder Structure
- `tutorials.md` → Beginner to advanced learning guides.
- `cheat_sheets.md` → Quick reference commands for daily use.
- `helm_guides.md` → Managing applications using Helm.
- `labs.md` → Practical tasks to solidify your learning.

---

## 📚 Resources
- [Official Kubernetes Docs](https://kubernetes.io/docs/home/)
- [Kubernetes by Example](https://kubernetesbyexample.com/)
- [Play with Kubernetes](https://labs.play-with-k8s.com/)
- [Katacoda Kubernetes Scenarios](https://www.katacoda.com/courses/kubernetes)
- [Kubernetes The Hard Way by Kelsey Hightower](https://github.com/kelseyhightower/kubernetes-the-hard-way)
- [CNCF Landscape](https://landscape.cncf.io/) – see Kubernetes ecosystem tools

> 🚀 Tip: Start with Minikube or Kind (Kubernetes in Docker) for local experiments.
