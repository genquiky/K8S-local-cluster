
# KUBERNETES
In this practical exercise, a learning environment was created using and old macOS workstation to install an all-in-one local Kubernetes cluster with worker nodes -isolated by a Docker container-, and using Minikube to manage the clusters.

Requirements for this test environment:

* At least 2 CPU cores (or virtual CPUs), 2 GB of RAM memory (4GB recommended), and 20 GB of disk storage.
* Docker Desktop (v4.15.0)
* Minikube (v1.37.0)
<br>

## 1. Creating a local cluster with 1 node (Control Plane)

Steps:

<b>1.1 Installing Docker Desktop for mac</b>

<br>
<br>
<br>

<b>1.2 Installing Minikube</b>

<br>
<br>
<br>

<b>1.3 Run Minikube</b>

The minikube <b>start</b> command generates a default minikube cluster with the standard specifications and it will store these specs so that we can restart the default cluster whenever desired. The object that stores the specifications of our cluster is called 'profile', in this case named 'minikube'.

Once the node is provisioned, it bootstraps the Kubernetes control plane (with the default kubeadm tool), and it installs the latest version of the default container runtime -Docker-. That will serve as a running environment for the containerized applications we will deploy to the Kubernetes cluster.

<br>
<br>
<br>

<b>1.4 Cheking the status</b>



<br>
<br>
<br>

<b>1.5 Cheking the cluster</b>

The minikube <b>profile list</b> command allows us to view the status of all our clusters in a table formatted output.
The table displays the number of nodes: 1 by default, the private IP address of the minikube cluster's control plane 'Docker' and other outputs.

<b>1.6 Stopping the cluster</b>




## 2. Creating a new cluster with 2 nodes
In this exercise a cluster with 2 nodes were created (Control Plane + Worker node) using the Docker runtime, and the Kubernetes <b>containerd</b> runtime.
The minikube start command allows us to create custom profiles with the --profile or -p flags.

<b>2.1 Adding a new cluster</b>

Driver: docker<br>
Nodes: 2<br>
Runtime: containerd<br>
CNI: calico<br>
Profile name: 'genbox'<br>

<b>2.2 Decommissioning a cluster</b>

If a cluster is no longer needed, the container can be easily removed.

## 3. GUI monitoring dashboards

<b>3.1 Minikube Dashboard</b>

By default a dashboard is included in the minikube tool (add-on).



<b>3.2 Docker Desktop</b>

