# Day58 challenge

---

## 📊 What the Metrics Server is and why HPA needs it

-> Metrics server is required to know the resource utilization of our application. HPA is a autoscaling type where it scales the pods based on observed metrics.

It works with:

* Deployment
* ReplicaSet
* StatefulSet

---

## ⚙️ How HPA calculates desired replicas

-> It works on a formula :

```
desiredReplicas = ceil(currentReplicas * (currentUsage / targetUsage))
```

---

## 🔄 The difference between autoscaling/v1 and v2

-> autoscaling/v1 works for CPU only whereas v2 works for CPU, memory & custom matrics as well.

---

## 📸 Screenshots of kubectl top, HPA events, and pod scaling

### 🖥️ Kubectl top:

<img width="753" height="328" alt="Screenshot 2026-04-14 at 11 15 03 PM" src="https://github.com/user-attachments/assets/0c49d536-ec91-4c81-9a08-fc5ccadfb83e" />

---

### 📈 HPA Events:

<img width="967" height="126" alt="Screenshot 2026-04-14 at 11 12 56 PM" src="https://github.com/user-attachments/assets/6be299a5-1232-432e-98f9-405842ce7ec7" />

<img width="1470" height="956" alt="Screenshot 2026-04-14 at 11 11 45 PM" src="https://github.com/user-attachments/assets/46548ce0-59e1-457b-97ab-b51bb3f64248" />

---

### 🔁 Pod scaling:

<img width="952" height="206" alt="Screenshot 2026-04-14 at 11 19 19 PM" src="https://github.com/user-attachments/assets/1bc4414d-05f9-4ad3-8a80-b6f03815461e" />
