### Challenge Tasks

## What Helm is and the three core concepts

-> A package manager for k8s.

### 3 main concepts:

1. **Chart** - A package of k8s manifests.
2. **Release** - A running instance of a chart in the cluster.
3. **Repository** - A storage location for charts.

---

## How to install, customize, upgrade, and rollback

### Install :

```bash
helm list
helm install my-redis bitnami/redis
helm list
```

### Customize:

```bash
helm install my-tomcat bitnami/tomcat -f custom-values.yaml
helm list
helm get values my-tomcat
```

### Upgrade :

```bash
helm upgrade my-redis bitnami/redis --set replicaCount=5
kubectl get pods
helm history my-redis
```

### Rollback :

```bash
helm history my-redis
helm rollback my-redis 1
helm history my-redis
```

---

## The structure of a Helm chart:

A chart is a directory created using:

```bash
helm create chart_name
```

Under the chart directory, there are:

* **Chart.yaml** (metadata)
* **values.yaml** (default configuration)
* **charts/** (dependencies)
* **templates/** (Kubernetes manifests)

Under the **templates/** directory, there will be main manifests like:

* Service
* Deployment
* HPA

---

## How Go templating works:

```
Templates + Values → Final Kubernetes manifests
```

---

## Your custom-values.yaml with explanations

![custom values](https://github.com/user-attachments/assets/99955504-cbde-4f5f-916f-418fc4c002f2)
