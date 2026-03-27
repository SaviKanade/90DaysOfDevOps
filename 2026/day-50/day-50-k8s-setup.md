# Challenge

## Task 1: Recall the Kubernetes Story

**Why was Kubernetes created? What problem does it solve that Docker alone cannot?**  
-> Due to auto scaling & healing.

**Who created Kubernetes and what was it inspired by?**  
-> developed by google & inspired by 'Borg'.

**What does the name "Kubernetes" mean?**  
-> It manages containers across many machines.

---

## Task 2: Draw the Kubernetes Architecture

### Control Plane (Master Node)
- API Server — the front door to the cluster, every command goes through it
- etcd — the database that stores all cluster state
- Scheduler — decides which node a new pod should run on
- Controller Manager — watches the cluster and makes sure the desired state matches reality

### Worker Node
- kubelet — the agent on each node that talks to the API server and manages pods
- kube-proxy — handles networking rules so pods can communicate
- Container Runtime — the engine that actually runs containers (containerd, CRI-O)

![IMG_8451](https://github.com/user-attachments/assets/19ddeb39-abfd-418a-b1ac-bb83d9f66641)


### After drawing, verify your understanding:

**What happens when you run `kubectl apply -f pod.yaml`?**  
Trace the request through each component.

**What happens if the API server goes down?**  
-> If API server goes down then the components won't be able to communicate with each other. Besides, you cannot create new requests but the already running workloads will keep on running but they won't get scaled or healed until API comes up.

**What happens if a worker node goes down?**  
-> Controller manager will immediately detects the failure & then scheduler assigns the new worker node.

---

## Task 3: Install kubectl

kubectl is the CLI tool you will use to talk to your Kubernetes cluster.

![Screenshot](https://github.com/user-attachments/assets/12ad1b2c-105d-44dd-ac82-966cc1d05229)

---

## Task 4: Set Up Your Local Cluster

Choose one of the following. Both give you a fully functional Kubernetes cluster on your machine.

### Option A: kind (Kubernetes in Docker)

![Screenshot](https://github.com/user-attachments/assets/12a5deb8-d3e4-49f7-9e37-4fcbc48abb52)

**Which one did you choose and why?**  
-> KIND because it seems easy & understandable as commands are quite like linux. Also, it uses docker which we had learned in earlier sessions.

---

## Task 5: Explore Your Cluster

### See cluster info
```bash
kubectl cluster-info
