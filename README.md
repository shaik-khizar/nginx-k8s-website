NGINX K8s Website Deployment

This project demonstrates how to deploy a static HTML website using **NGINX** inside a Kubernetes cluster using **Minikube**. It helps beginners understand how Kubernetes **Deployments**, **Services**, **Volumes**, and **ConfigMaps** work together.

---

Technologies Used

- Kubernetes
- Minikube
- NGINX
- YAML
- Git

---

Project Structure

nginx-k8s-website/
│
├── index.html # Static HTML page
├── nginx-deployment.yaml # K8s Deployment with volume mount
├── nginx-service.yaml # NodePort Service to expose the website
├── README.md # Project documentation


---

Prerequisites

- ✅ Minikube installed and running
- ✅ `kubectl` configured to point to Minikube cluster
- ✅ Git installed

---

How to Deploy

1. **Start Minikube**

   minikube start
Deploy the NGINX Pod
kubectl apply -f nginx-deployment.yaml

Expose NGINX via NodePort
kubectl apply -f nginx-service.yaml

Get Minikube IP
minikube ip

Access the Website
Visit in your browser:
http://<minikube-ip>:<node-port>

Example:
http://192.168.49.2:30080
