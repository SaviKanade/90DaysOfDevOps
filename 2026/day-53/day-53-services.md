#  Day 53 - Kubernetes services

---

## 🧠 What problem Services solve and how they relate to Pods and Deployments

Kubernetes provides **unstable IPs** — when a Pod gets restarted or replaced, it gets a new IP.

Also, if multiple Pods are running, deciding **which IP to connect to** becomes a problem.

### ✅ Solution: Services

- Services provide a **stable IP and DNS name** that never changes
- They act as an **abstraction layer** over Pods
- They expose a **group of Pods over a network**

---

## 🚀 Your Three Service Types

### 🔹 1. ClusterIP (Default)

- Provides a **stable internal IP**
- Accessible **only within the cluster**

![ClusterIP](https://github.com/user-attachments/assets/2d9b2ddc-33ca-41e5-bd94-0b668479d85f)

---

### 🔹 2. NodePort

- Exposes the application on a **port on every node**
- Allows access **from outside the cluster**

![NodePort](https://github.com/user-attachments/assets/f79bb58a-917a-4d34-b881-8a8a581a713a)

---

### 🔹 3. LoadBalancer

- Used in **cloud environments** (e.g., AWS EKS, Azure AKS)
- Provides an **external Load Balancer URL**

![LoadBalancer](https://github.com/user-attachments/assets/758d0f72-ba82-4a32-a5ae-9198bb7bd63f)

---

## ⚖️ Difference Between Service Types

| Feature        | ClusterIP              | NodePort                     | LoadBalancer                  |
|----------------|----------------------|-----------------------------|-------------------------------|
| Accessibility  | Internal only         | External via Node IP        | External via LB URL           |
| Use Case       | Internal services     | Testing / external access   | Production (cloud)            |

---

## 🌐 How Kubernetes DNS Works for Service Discovery

Kubernetes uses an **internal DNS system** to allow Pods to communicate with Services using **names instead of IP addresses**.

---

## 🔍 What Endpoints Are and How to Inspect Them

Endpoints are Kubernetes objects that store the **IP addresses of Pods** backing a Service and are used for routing traffic.

### 📌 Key Concepts

- **Service** = Stable entry point  
- **Endpoints** = Actual Pod IPs behind the Service  
- Service does **not directly know Pods** → it uses Endpoints

---

### 🔧 How to Inspect Endpoints

```bash
kubectl get endpoints
kubectl describe endpoints <service-name>
```


## 📸 Screenshot of Services and Test Output
<img width="1052" height="184" alt="Screenshot 2026-04-03 at 12 43 04 PM" src="https://github.com/user-attachments/assets/1a880e82-1ebf-4833-bdb6-e83258cc29f3" />
