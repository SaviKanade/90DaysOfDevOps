# StatefulSet Notes

## What StatefulSets are and when to use them vs Deployments

-> StatefulSets are like deployment & it used to manage stateful applications that require stable network identity, persistent storage & ordered deployment.
We can use them with databases (mysql, postgresql), Kafka, zookeeper & Redis (cluster mode).

---

## The comparison table

| Feature      | Deployment       | StatefulSet        |
| ------------ | ---------------- | ------------------ |
| App type     | Stateless        | Stateful           |
| Pod identity | Random           | Fixed              |
| Storage      | Shared/ephemeral | Persistent per pod |
| Scaling      | Parallel         | Ordered            |

---

## How Headless Services, stable DNS, and volumeClaimTemplates work

-> Headless service works once we mention 'clusterIP: None' in our service yaml.
Stable DNS means each Pod gets unique DNS name.
volumeClaimTemplates are basically like PVC where we are claiming the volume.

---

## Screenshots of pods, PVCs, and DNS resolution

### Pods:

![Pods](https://github.com/user-attachments/assets/3ed4e16c-773c-41ca-ac75-ec4718b443a7)

### PVC:

![PVC](https://github.com/user-attachments/assets/fe141fd3-d437-480b-8a63-6a64fa04d714)

### DNS resolution:

![DNS](https://github.com/user-attachments/assets/a283eb57-b090-4e90-909f-7c9f0d257f9a)
