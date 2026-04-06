# Day 55 - Persistent Volumes (Kubernetes)

---

## 🧠 Why Containers Need Persistent Storage

Containers are **ephemeral (temporary)** in nature:
- When a container restarts or crashes, its data is lost
- Pods can be deleted/recreated anytime

### ❌ Problem
- Data inside container filesystem is **not persistent**

### ✅ Solution
- Use persistent storage to:
  - Store databases
  - Save logs
  - Keep user uploads
  - Maintain application state

---

## 📦 What PVs and PVCs Are and How They Relate
### 🔹 PersistentVolume (PV)
- A **cluster-level storage resource**
- Created by admin or dynamically
- Represents actual storage (disk, NFS, cloud storage)

---

### 🔹 PersistentVolumeClaim (PVC)
- A **request for storage by a user**
- Defines:
  - Size
  - Access mode
  - Storage class

---

### 🔗 What PVs and PVCs are and how they relate
-> PVC requests storage.
Kubernetes binds it to a matching PV.

 ---


 ### 🔗 Static vs dynamic provisioning
-> 
🔹 Static Provisioning
Admin manually creates PV
User creates PVC
Kubernetes matches PVC with existing PV
Manual work

🔹 Dynamic Provisioning
PVC requests storage with a StorageClass
Kubernetes automatically creates PV
Commonly used in cloud


 ### Access modes and reclaim policies
🔐 Access Modes
| Access Mode         | Description                             |
| ------------------- | --------------------------------------- |
| ReadWriteOnce (RWO) | Mounted as read-write by a single node  |
| ReadOnlyMany (ROX)  | Mounted as read-only by multiple nodes  |
| ReadWriteMany (RWX) | Mounted as read-write by multiple nodes |


♻️ Reclaim Policies
| Policy               | Description                         |
| -------------------- | ----------------------------------- |
| Retain               | Keeps data, manual cleanup required |
| Delete               | Deletes storage automatically       |
