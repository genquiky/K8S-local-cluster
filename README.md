
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

<img width="872" height="auto" alt="image" src="https://github.com/user-attachments/assets/f8846faa-6ce4-4bc9-9902-466afd7938d1" />

<br>
<br>
<br>
<br>

<b>1.2 Installing Minikube</b>

<img width="834" height="auto" alt="image" src="https://github.com/user-attachments/assets/a387d924-1b5a-490e-9e81-69dc17cd2cd6" />

<br>
<br>
<br>
<br>

<b>1.3 Run Minikube</b>

The minikube <strong>start</strong> command generates a default minikube cluster with the standard specifications and it will store these specs so that we can restart the default cluster whenever desired. The object that stores the specifications of our cluster is called 
'profile', in this case named 'minikube'.

Once the node is provisioned, it bootstraps the Kubernetes control plane (with the default kubeadm tool), and it installs the latest version of the default container runtime -Docker-. That will serve as a running environment for the containerized applications 
we will deploy to the Kubernetes cluster.

<br>

<img width="834" height="auto" alt="image" src="https://github.com/user-attachments/assets/7e3c7414-8646-4ba8-9a24-ec76cf33ed8b" />

<br>
<br>
<br>
<br>

<b>1.4 Checking the status</b>

<img width="350" height="auto" alt="image" src="https://github.com/user-attachments/assets/1a46ef21-a304-4522-bf3f-23d5ab6f05ed" />

<br>
<br>
<br>
<br>

<b>1.5 Checking the cluster</b>

The minikube <strong>profile list</strong> command allows us to view the status of all our clusters in a table formatted output.
The table displays the number of nodes: 1 by default, the private IP address of the minikube cluster's control plane 'Docker' and other outputs.

<img width="2372" height="auto" alt="image" src="https://github.com/user-attachments/assets/47062acf-ddc6-49d8-a8f9-df321050ecfc" />

<br>
<br>
<br>
<br>

<b>1.6 Stopping the cluster</b>

<img width="556" height="81" alt="image" src="https://github.com/user-attachments/assets/fe285924-6da5-46f9-afae-3fb9555db1ec" />

<br>
<br>
<br>
<br>
<br>

## 2. Creating a new cluster with 2 nodes
In this exercise a cluster with 2 nodes were created (Control Plane + Worker node) using the Docker runtime, and the Kubernetes <b>containerd</b> runtime.
The minikube start command allows us to create custom profiles with the --profile or -p flags.

<b>2.1 Adding a new cluster</b>

Driver: docker<br>
Nodes: 2<br>
Runtime: containerd<br>
CNI: calico<br>
Profile name: 'genbox'<br>

<br>

<img width="834" height="auto" alt="image" src="https://github.com/user-attachments/assets/e776851b-d622-4497-8eee-743a9e0ce889" />

<br>
<br>
<br>

<b>2.2 Checking the new cluster</b>

<img width="834" height="auto" alt="image" src="https://github.com/user-attachments/assets/cc5590cd-aade-49eb-a6bc-0b8cd528bc67" />

<br>
<br>
<br>

<img width="400" height="auto" alt="image" src="https://github.com/user-attachments/assets/ffc9bf1b-f1a2-4586-8b96-abbd7736a94f" />

<br>
<br>
<br>

<b>2.3 Decommissioning the cluster</b>

If a cluster is no longer needed, the container can be easily removed.

<br>

<img width="500" height="auto" alt="image" src="https://github.com/user-attachments/assets/d4c0788f-da4b-4316-9a5e-01b456bfbb01" />

<br>
<br>
<br>

## 3. GUI monitoring dashboards

<b>3.1 Minikube Dashboard</b>

By default a dashboard is included in the minikube tool (add-on).

<img width="650" height="auto" alt="image" src="https://github.com/user-attachments/assets/29055509-b63a-4ca1-8cc3-73fe1ac4f726" />

<br>
<br>

<img width="834" height="auto" alt="image" src="https://github.com/user-attachments/assets/de257805-4b30-413a-af4a-bbdf124c9b42" />

<br>
<br>
<br>
<br>

<b>3.2 Using Docker Desktop</b>

<img width="834" height="auto" alt="image" src="https://github.com/user-attachments/assets/df054a14-3c73-49a5-8f9c-ebc8ae8b29f7" />

