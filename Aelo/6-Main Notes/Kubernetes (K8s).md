
2024-07-23 16:12

Status : #baby 

Tags : [[DevOps Tools]] 

# Kubernetes (K8s)

Kubernetes (often abbreviated as K8s) is an open-source container orchestration platform originally developed by Google and now maintained by the Cloud Native Computing Foundation (CNCF). 

Basically groups n no of containers into one logical unit for managing and deploying them easily. 

Kubernetes master controls everything, container wont be run on K8s master, but containers would be run on nodes. controls cluster and nodes in it.

master controls cluster and the nodes in it

nodes hosts pods, and there will be n no of containers in each pods. pods are logical collection of containers which need to interact with each other for an application.

Here are some key aspects and functionalities of Kubernetes:

1. **Container Orchestration**: Kubernetes automates the deployment, scaling, and management of containerized applications. It allows you to deploy containers across clusters of machines, handle scaling based on resource usage, and manage the life-cycle of containers (e.g., rolling updates, rollbacks).

2. **Architecture**: Kubernetes follows a client-server architecture where the components interact via a REST API. It consists of a master node (control plane) that manages the cluster and nodes (worker nodes) where containers are deployed.

3. **Key Components**:
   - **Master Components**: Core components that manage the cluster state and perform orchestration tasks, including `kube-apiserver`, `kube-controller-manager`, `kube-scheduler`, and `etcd` (a distributed key-value store for cluster data).
   - **Node Components**: Agents that run on each node and manage the containers, including `kubelet` (responsible for communication between the Kubernetes Master and the nodes) and `kube-proxy` (manages network connectivity to services in the cluster).
   - **Pods**: The smallest deployable unit in Kubernetes, consisting of one or more containers that share resources and a network namespace.
   - **Deployments**: A higher-level abstraction that manages deploying and updating applications declaratively.

4. **Features**:
   - **Automatic Bin Packing**: Kubernetes automatically places containers based on their resource requirements and constraints.
   - **Self-Healing**: Kubernetes can detect and replace containers that fail or become unresponsive.
   - **Service Discovery and Load Balancing**: Kubernetes can manage a network of services with automatic load balancing.
   - **Storage Orchestration**: Kubernetes allows you to automatically mount storage systems of your choice (local storage, public cloud providers, etc.) to your containers.

5. **Use Cases**: Kubernetes is widely used for deploying and managing containerized applications in production environments. It is favored for its scalability, resilience, and ability to manage complex microservices architectures.

In summary, Kubernetes provides powerful tools for automating the deployment, scaling, and operations of application containers across clusters of hosts, making it easier to manage and scale containerized applications in modern cloud-native environments.

# References