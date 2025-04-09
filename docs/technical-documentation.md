# 🧪 Kubernetes Test Plan (v1.0)

## 🎯 Objective  
Ensure the Kubernetes cluster functions as expected in a production-like environment, validating stability, networking, storage, and scaling.

## 🖥️ Test Environment  
- Kubernetes: v1.29  
- Nodes: 3x Ubuntu 22.04 (1 master, 2 workers)  
- CNI: Calico  
- Ingress: NGINX  
- Storage: Ceph RBD  

## ✅ Test Checklist

### 🧵 Core Components  
- [ ] kube-apiserver responds to health checks  
- [ ] kubelet is active on all nodes  
- [ ] CoreDNS resolves service names  

### 🌐 Networking  
- [ ] Pod-to-pod communication works across nodes  
- [ ] Pod-to-service communication works  
- [ ] External access via Ingress is functional  

### 📦 Storage  
- [ ] PVCs are created successfully (RWO & RWX)  
- [ ] Data persists after pod restart  
- [ ] Ceph backend shows I/O activity  

### 🧰 Workload  
- [ ] Deployments scale up/down properly  
- [ ] Rolling updates complete without downtime  
- [ ] Pods are scheduled evenly across nodes  

### 🛡️ Resilience  
- [ ] Node failure triggers pod rescheduling  
- [ ] etcd backup and restore verified  

### 🧩 Add-ons  
- [ ] Metrics Server provides resource data  
- [ ] Dashboard loads and authenticates  

