 Course Contents ⭐️
⌨️ (0:00:00) Kubernetes for Beginners Introduction


⌨️ (0:02:40) What is Kubernetes
 - kubernetes is container ochestration system. Kubernetes allow you to create different containers on different serverd either physical or virtual
 # what is kubernetes use for
 - Automatic deployment of containerized application across different servers
 - distribution of loads across multiple servers
 - Auto scaling of the deployed application
 - monitoring and health check of the containers
 - Replace of failed containers
 # supported containers runtime
 - Docker
 - CRI-O
 - containerd
⌨️ (0:06:46) What is Pod
- pod is the smallest unit in the kubernetes world
# pods can contains
- containers
- shared volumes 
- shared IP addresses
# All containers inside the same pods shares volumes and IP address
⌨️ (0:08:22) Kubernetes Cluster and Nodes
- kubernetes clusters consist of nodes
- Nodes are servers either physical or virtuall
- Nodes which belongs to the same clusted are located close to each other in other to perform all jobs more efficiently
- Nodes contains pods 
- in kubernetes cluster thare is master node and all other nodes are worker nodes 
- Master nodes manages workers node. Master Node is actually control plane, and it does not run your client application
- A worker node comprises of: kubelet, kube-proxy, and container runtime.
- so a Master nodes can conatins several groupped (kubelet,kube-proxy,container runtime) 
- container runtime actual runs the containers inside each node e.g (docker, CRI-O, containerd)
- kubelet on each worker nodes communicate with the API server of the Master Node 
- cube-proxy which is present on each node is responsible for network communication inside of each node and between nodes 
# Master Node consist of 
- API server - API server is the main point of communication in the kubernetes world
- Scheduler - Scheduler is responsible for planning and distribution of loads between different nodes in the clusters
- Kube Controller Manager - it controlls everything that happen in the cluster, controls what happen on each nodes in the cluster
- Cloud Controller Manager - its job is to interact with the cloud service provider where the kubernetes cluster are run
- etcd - it stores all logs related to kubernetes cluster and the logs are stored as key pairs.

⌨️ (0:10:40) Kubernetes Services
- kubenetes cluster can be managed using kubectl or kube control
⌨️ (0:14:17) What is kubectl
- kubectl is a command line which allows you connect to a specific kubenetes cluster and manages it remotely
- you can use it on your local system to connect using REST API to connect to API server on Master node and such communication happpens over https
⌨️ (0:17:23) Software required for this course
⌨️ (0:21:49) Installing kubectl
⌨️ (0:25:03) Installing Minikube
⌨️ (0:29:38) Creating Kubernetes cluster using Minikube
⌨️ (0:33:50) Exploring the Kubernetes node
⌨️ (0:40:36) Creating just single Pod
⌨️ (0:45:57) Exploring Kubernetes Pod
⌨️ (0:52:44) Creating alias for the kubectl command
⌨️ (0:55:17) Creating and exploring Deployment
⌨️ (1:07:00) Connecting to one of the Pods using its IP address
⌨️ (1:09:23) What is Service
⌨️ (1:11:18) Creating and exploring ClusterIP Service
⌨️ (1:16:38) Connecting to the Deployment using ClusterIP Service
⌨️ (1:20:55) Deleting Deployment and Service
⌨️ (1:22:20) Creating Node web application
⌨️ (1:30:05) Dockerizing Node application
⌨️ (1:38:28) Pushing custom image to the Docker Hub
⌨️ (1:40:26) Creating deployment based on the custom Docker image
⌨️ (1:45:49) Scaling custom image deployment
⌨️ (1:49:14) Creating NodePort Service
⌨️ (1:53:51) Creating LoadBalancer Service
⌨️ (1:56:49) Rolling update of the deployment
⌨️ (2:05:30) What happens when one of the pods is deleted
⌨️ (2:06:31) Kubernetes Dashboard
⌨️ (2:10:49) Creating YAML deployment specification file
⌨️ (2:17:04) How to use Kubernetes documentation
⌨️ (2:20:35) Applying YAML deployment file
⌨️ (2:24:13) Creating YAML service specification file
⌨️ (2:27:59) Plan for the creation of the two deployments
⌨️ (2:31:16) Creating another web app with two endpoints
⌨️ (2:35:15) Building custom Docker image for the second web app
⌨️ (2:36:38) Creating YAML specification for the second web app
⌨️ (2:39:02) Creating YAML specification for the NGINX app
⌨️ (2:42:07) Applying specifications for both apps
⌨️ (2:44:09) Verifying connectivity between different deployments
⌨️ (2:47:05) Resolving Service name to IP address
⌨️ (2:49:52) Deleting both applications
⌨️ (2:51:00) Changing Container Runtime from Docker to CRI-O
⌨️ (2:54:49) Deploying apps using CRI-O container runtime
⌨️ (2:56:08) Verifying connectivity between deployments
⌨️ (2:57:11) Wrap-Up