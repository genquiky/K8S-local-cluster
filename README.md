
# KUBERNETES
In this practical exercise, a learning environment was created using and old macOS workstation to install an all-in-one local Kubernetes cluster with worker nodes -isolated by a Docker container-, and using Minikube to manage the clusters.

## 1. Creating a local cluster

Requirements for this test environment:

* At least 2 CPU cores (or virtual CPUs), 2 GB of RAM memory (4GB recommended), and 20 GB of disk storage.
* Docker Desktop (v4.15.0)
* Minikube (v1.37.0)

Steps:

<b>1.1 Installing Docker Desktop for mac</b>


<img width="872" height="395" alt="image" src="https://github.com/user-attachments/assets/c5db002d-3211-4d34-874e-140c9fa3ce3a" />

'$ sudo hdiutil attach /path/to/Docker.dmg'
$ sudo /Volumes/Docker/Docker.app/Contents/MacOS/install
$ sudo hdiutil detach /Volumes/Docker


<b>1.2 Installing Minikube</b>


<img width="834" height="223" alt="image" src="https://github.com/user-attachments/assets/1e45b46b-b530-48d9-9138-6c32c9248448" />


$ curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-darwin-amd64

$ sudo install minikube-darwin-amd64 /usr/local/bin/minikube

<b>1.3 Run Minikube</b>

The minikube start command generates a default minikube cluster with the specifications described and it will store these specs so that we can restart the default cluster whenever desired. The object that stores the specifications of our cluster is called 'profile'.

<img width="840" height="360" alt="image" src="https://github.com/user-attachments/assets/23c33209-8231-479f-85ab-02aae3df9acf" />
