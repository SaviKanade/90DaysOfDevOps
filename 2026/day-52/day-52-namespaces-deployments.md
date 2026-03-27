
## 🔹 What namespaces are and why you would use them

-> Namespaces are isolated groups created for replicas of pods.  
-> Basically, different teams can work without conflicts.

---

## 🔹 Your Deployment manifest and an explanation of each section

<img width="1036" height="627" alt="Deployment Manifest" src="https://github.com/user-attachments/assets/10b3a2dd-5f7d-4dab-952d-e13ee67f5214" />

---

## 🔹 What happens when you delete a Pod managed by a Deployment vs a standalone Pod

-> When we delete a pod managed by deployment, it will recreate it again as the Deployment controller detects the replica count. If it is less than the desired count, it immediately recreates it.  

-> Whereas in a standalone pod, it gets permanently deleted/removed.

---

## 🔹 How scaling works (both imperative and declarative)

-> Scaling works the same for both imperative & declarative approaches. It works as per the mentioned replica count.  

-> For example: If initially replicas are set to 3 and later scaled to 2, then the Deployment controller will automatically terminate/delete one pod.

---

## 🔹 How rolling updates and rollbacks work

-> Rolling updates will update your specific input (like image version) gradually.  

-> Rollback will revert it back to the previous/original version.

---

## 🔹 Screenshot of your Deployment and Pods running

<img width="1229" height="507" alt="Deployment and Pods" src="https://github.com/user-attachments/assets/ed025b5b-2cf9-488e-b08c-486d4e164258" />
