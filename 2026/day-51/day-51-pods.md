# 🚀 Challenge Tasks

## Task 1: Create Your First Pod (Nginx)

**Can you see the Nginx welcome page when you curl from inside the pod?**  
-> Yes, I can able to see the welcome page.

<img width="1006" height="755" alt="Screenshot 2026-03-27 at 2 22 16 PM" src="https://github.com/user-attachments/assets/96731950-f820-4b58-afbf-12819ade3a5c" />

---

## Task 2: Create a Custom Pod (BusyBox)

**Can you see "Hello from BusyBox" in the logs?**  
-> Yes, it shows in the logs.

<img width="948" height="377" alt="Screenshot 2026-03-27 at 2 28 19 PM" src="https://github.com/user-attachments/assets/4662198d-fdac-45f3-8961-ddebc2a4db08" />

---

## Task 3: Imperative vs Declarative

You have been using the declarative approach (writing YAML, then kubectl apply). Kubernetes also supports imperative commands.

**Verify:**  
Save the dry-run output to a file and compare its structure with your nginx-pod.yaml. What fields are the same? What is different?

-> K8s generated yaml doesnot have port.

<img width="795" height="557" alt="Screenshot 2026-03-27 at 2 35 49 PM" src="https://github.com/user-attachments/assets/6b463167-d6ca-427d-8627-622785c084e6" />

**Observation:**  
-> Its quite easy with imperative as its automatically create manifest file whereas in declarative we have to create it which is quite difficult & time consuming with the indentation issues.

---

## Task 4: Validate Before Applying

Before applying a manifest, you can validate it:

Verify:
What error does Kubernetes give when the image field is missing?

-> Yes, it does show the error when we use dry-run=server.

<img width="1470" height="472" alt="Screenshot 2026-03-27 at 2 42 30 PM" src="https://github.com/user-attachments/assets/759de42d-cb07-4a1a-8346-2c3be04f909c" />

## Task 5: Pod Labels and Filtering

Labels are how Kubernetes organizes and selects resources. You added labels in your manifests — now use them.

Write a manifest for a third pod with at least 3 labels (app, environment, team). Apply it and practice filtering.

<img width="954" height="674" alt="Screenshot 2026-03-27 at 2 51 53 PM" src="https://github.com/user-attachments/assets/f292cf75-182e-4ee3-b7a9-c7d4dacb706a" />

## Task 6: Clean Up

Delete all the pods you created.

Running Pods:

<img width="719" height="164" alt="Screenshot 2026-03-27 at 2 52 32 PM" src="https://github.com/user-attachments/assets/e60738dc-ea57-40d7-92be-616a1170f260" /> ```
