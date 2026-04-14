# Challenge of Day57 

---

## 🧩 Requests vs Limits (Scheduling vs Enforcement)

### 🔹 Requests vs Limits

* **Requests** → Guaranteed minimum resources (used for scheduling)
* **Limits** → Maximum allowed resources (enforced by kubelet at runtime)

---

## ⚙️ What happens when CPU or Memory Limits are Exceeded?

* **CPU** → Gets **throttled (slowed down)**, container is NOT killed
  👉 CPU is **compressible**

* **Memory (RAM)** → Triggers **OOMKilled** and container is **immediately terminated**
  👉 Memory is **not compressible**

---

## 🩺 Liveness vs Readiness vs Startup Probes

| Probe Type    | Purpose                                                |
| ------------- | ------------------------------------------------------ |
| **Liveness**  | Checks if the container is **alive (healthy)**         |
| **Readiness** | Checks if the container is **ready to serve traffic**  |
| **Startup**   | Checks if the application has **started successfully** |

---

## 📸 Screenshots of OOMKilled, Pending, and Probe Events

### 🔴 OOMKilled

<img width="802" height="259" alt="OOMKilled Screenshot 1" src="https://github.com/user-attachments/assets/dd6eb97b-7ee0-462b-b7cf-83b31ffa62ae" />

<img width="1160" height="868" alt="OOMKilled Screenshot 2" src="https://github.com/user-attachments/assets/14455c7c-a0d2-4841-9fdd-fc440782a24f" />

---

### 🟡 Pending

<img width="732" height="232" alt="Pending Screenshot 1" src="https://github.com/user-attachments/assets/aacbc35e-1160-46fb-9aea-20d1d543abcc" />

<img width="1470" height="665" alt="Pending Screenshot 2" src="https://github.com/user-attachments/assets/1de3233f-bb5c-4849-a57b-a5fde38b6fe5" />

---

## 🔍 Probe Events

### ❤️ Liveness Probe

<img width="1470" height="364" alt="Liveness Screenshot 1" src="https://github.com/user-attachments/assets/707a885e-7502-4493-96df-fe8333e12ca4" />

<img width="1470" height="956" alt="Liveness Screenshot 2" src="https://github.com/user-attachments/assets/ae0c48db-cd43-4cab-b7c2-508e09b7990c" />

---

### 📞 Readiness Probe

<img width="944" height="332" alt="Readiness Screenshot 1" src="https://github.com/user-attachments/assets/3b3ae76b-e1f8-4488-bdae-f2f3dd481306" />

<img width="1468" height="229" alt="Readiness Screenshot 2" src="https://github.com/user-attachments/assets/3ee5791f-e7da-48bb-a2ea-2ae4961e791e" />

---

### 🚀 Startup Probe

<img width="1470" height="671" alt="Startup Screenshot" src="https://github.com/user-attachments/assets/c9b9658b-d546-48b8-aa02-03db177d3467" />

---

## 🔥 Quick Summary

* CPU → **Throttled (safe)**
* Memory → **Killed (OOMKilled)**
* Liveness → **Restarts unhealthy container**
* Readiness → **Controls traffic**
* Startup → **Handles slow startup apps**
