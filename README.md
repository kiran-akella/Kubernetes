# ☸️ Kubernetes - The Power of Container Orchestration

Kubernetes, often abbreviated as **K8s**, is an open-source **container orchestration platform** designed to automate the deployment, scaling, and management of containerized applications. It was originally developed by Google and is now maintained by the **Cloud Native Computing Foundation (CNCF)**.

---

## 📌 Key Features of Kubernetes

### 🔄 1. Automated Container Orchestration
Kubernetes manages containerized applications automatically, ensuring smooth operations.

✅ **Automated deployment & rollback**

✅ **Self-healing** - Restarts failed containers

✅ **Horizontal scaling** - Scales applications dynamically

### ⚖️ 2. Load Balancing & Service Discovery
K8s provides built-in service discovery and load balancing.

🔗 **ClusterIP** - Internal service access

🌍 **NodePort** - Exposes services externally

🖧 **LoadBalancer** - Uses cloud provider’s LB

### 📦 3. Declarative Configuration & Desired State Management

With Kubernetes, you define your infrastructure as **YAML manifests**, making it easy to maintain and replicate.

📜 **Declarative Configuration:**
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
        - name: my-app
          image: my-app:v1
          ports:
            - containerPort: 80
```

### ☁️ 4. Multi-Cloud & Hybrid Cloud Support

Kubernetes works seamlessly across on-premise, public cloud, and hybrid cloud environments.

✅ **Cloud-Native** - Works with AWS, GCP, Azure

✅ **Edge Computing** - Deploy workloads at the edge

✅ **Hybrid Deployments** - Combine cloud and on-premises

---

## 🏗️ Kubernetes Architecture

### 1️⃣ **Master Node (Control Plane)**
The **Control Plane** manages the cluster and ensures the desired state is maintained.

🔹 **API Server (kube-apiserver)** - Frontend for Kubernetes API

🔹 **Controller Manager (kube-controller-manager)** - Maintains cluster state

🔹 **Scheduler (kube-scheduler)** - Assigns workloads to nodes

🔹 **etcd** - Stores cluster configuration

### 2️⃣ **Worker Nodes**

Worker nodes run application containers and report back to the master node.

🔹 **Kubelet** - Agent running on nodes

🔹 **Kube Proxy** - Manages networking

🔹 **Container Runtime** - Runs containers (Docker, containerd, CRI-O)

---

## 🔧 Kubernetes Components

### 🏷 **Pods**

The smallest deployable unit in Kubernetes that can contain one or more containers.

### 🎛 **Deployments**

Ensures application replicas run smoothly and handle updates.

### 🖧 **Services**

Exposes applications to internal and external networks.

### 🔑 **ConfigMaps & Secrets**

Manages configuration data and sensitive information.

### 🔄 **Ingress**

Manages external HTTP and HTTPS traffic to services.

---

## 🔒 Security Best Practices

### 🔐 1. Use Role-Based Access Control (RBAC)

Restrict user and application permissions.

### 🛡️ 2. Enable Network Policies

Control traffic between pods and external resources.

### 🏗️ 3. Use Namespaces

Isolate workloads using **Kubernetes Namespaces**.

---

## 📈 Monitoring & Logging

🔹 **Prometheus** - Metrics collection and alerting

🔹 **Grafana** - Data visualization

🔹 **Loki** - Log aggregation

🔹 **Jaeger** - Distributed tracing

---

## ☸️ Kubernetes in the Cloud - Amazon EKS

### 🌐 Amazon Elastic Kubernetes Service (EKS)

Amazon **EKS (Elastic Kubernetes Service)** is a managed Kubernetes service by AWS.

✅ **Fully managed control plane**

✅ **Seamless integration with AWS services**

✅ **Supports Fargate for serverless Kubernetes**
