# Day54 Challenges

---

## 🧠 What ConfigMaps and Secrets are and when to use each

### 🔹 ConfigMap
- A ConfigMap stores **configuration data in plain text**
- Data is stored in **key-value pairs**
- Used for:
  - Application configs
  - Environment settings
  - Non-sensitive data

---

### 🔹 Secret
- A Secret stores **sensitive data** like:
  - Passwords
  - Tokens
  - Credentials
- Data is stored in **base64 encoded format** (not encrypted by default)

---

## ⚖️ Difference Between Environment Variables and Volume Mounts

| Environment Variables | Volume Mounts |
|----------------------|--------------|
| Used to pass configuration as key-value pairs | Used to mount files/directories into a container |
| Suitable for small config values | Suitable for large or structured data |

---

## 🔐 Why Base64 is Encoding, Not Encryption

- Base64 **converts binary data into ASCII format**
- It does **not use any key**
- Easily reversible using decoding

👉 Encryption:
- Requires a **key**
- Provides **security**

---

## 🔄 How ConfigMap Updates Propagate to Volumes but Not Env Vars

- **Environment Variables**
  - Set only once at container startup
  - Stored in process memory
  - Do **not update automatically**

- **Volume Mounts**
  - Kubernetes creates files from ConfigMap
  - Files are **kept in sync automatically**
  - Updates are reflected dynamically

---

## 📸 ConfigMaps & Secrets

![ConfigMaps & Secrets](https://github.com/user-attachments/assets/6330fce8-4785-4d01-946d-9635ec00fc53)

---
