# Container Orchestration Knowledge
## Docker



### Docker Compose
### Docker Swarm

## Kubernates

### Fundamental concepts

<details>
  <summary>K8s components</summary>
  <br/>

 + Control Plane Components:

  1. **kube-apiserver:** The core component that exposes the Kubernetes API.
  2. **etcd:** A consistent and highly-available key-value store used for all cluster data.
  3. **kube-scheduler:** Assigns pods to nodes based on resource availability.
  4. **kube-controller-manager:** Runs various controllers to manage the state of the cluster.
  5. **cloud-controller-manager:** Integrates with cloud providers (optional).

  + Node Components

  1. **kubelet:** Ensures that containers are running in a pod.
  2. **kube-proxy:** Maintains network rules on nodes to facilitate communication between pods.
  3. **Container runtime:** Software responsible for running containers (e.g., Docker, containerd).

  + Additional Components

  1. **Pods:** The smallest deployable units in Kubernetes, which can contain one or more containers.
  2. **Services:** Define a logical set of pods and a policy to access them.
  3. **Ingress:** Manages external access to services, typically HTTP.
  4. **ConfigMaps and Secrets:** Store configuration data and sensitive information, respectively.
  5. **Persistent Volumes (PV):** Provide persistent storage for pods.

  ![](images/kubernetes-cluster-architecture.png)
  
</details>

### Service

<details>
  <summary>What is Service</summary>
  <br/>

  Service is an abstraction that defines a logical set of Pods and a policy by which to access them. 

  + **Network Access:** A Service provides a stable endpoint (IP address and DNS name) to access a set of Pods1.
  + **Load Balancing:** It can distribute traffic across multiple Pods, ensuring that the load is balanced and no single Pod is overwhelmed.
  
</details>
<details>
  <summary>Types of Services</summary>
  <br/>

  **ClusterIP** 
  + This is the default type
  + It exposes the Service on a cluster-internal IP. This means the Service is only **accessible within the cluster**.
  + Apply for internal communication between different components of an application that do not need to be exposed to the outside world.
  + For example, connecting a backend service to a frontend service **within the same cluster**.

  **NodePort:** 
  + Exposes your application on each Node’s IP at a static port. _Node’s IP refers to the IP address assigned to a node._
  + NodePort services use a port from a predefined range, typically between **30000** and **327671**.
  + Useful for development or testing environments where you need to access the application from your local machine.

  **LoadBalancer:**
  + Exposes the Service externally using a cloud provider’s load balancer.
  + Suitable for production environments where you need scalable access from the internet.

  **ExternalName**
  + Maps a Service to the contents of the `externalName` field.
  + Redirects traffic to an external service outside the Kubernetes cluster.
  + Integrating with external services that are not part of the Kubernetes cluster.
  
</details>

### Ingress

<details>
  <summary>Ingress</summary>
  <br/>
  
</details>
