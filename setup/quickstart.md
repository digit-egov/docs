---
description: >-
  Quickstart solutions give you the ability to try DIGIT out quickly. These are
  not meant for production use as is.
---

# Quickstart Guide

DIGIT is a distributed microservice-based platform that comprises many services which are containerized and can be run on any container supported orchestration platform like dockers, Kubernetes, etc,

Here in this Quickstart guide, we'll create a lightweight Kubernetes cluster called [k3d](https://github.com/rancher/k3d) on either a local machine or on a VM of a specific H/W requirement. The H/W requirements are listed below to ensure before we proceed further.

## **1. Infra Setup**

**To provision a lightweight Kubernetes cluster, please follow the instructions below in context to your OS and install the k3d on your machine.** 

### **H/W  or VM Size**

* 8 vCPUs \(recommended 8\)
* 16GiB of RAM \(recommended 16\)
* 30GiB of HDD \(recommended 30+\)

### **Tools**

* **Linux distribution running in a VM or bare metal**
  * Ubuntu 18.04 or Debian 10 \(VM or bare metal\)
  * Install [Docker](https://docs.docker.com/engine/install/ubuntu/)
  * [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/) on Linux
* **OSX or Mac**
  * [Docker Desktop](https://docs.docker.com/docker-for-mac/install/) local Kubernetes cluster enabled
  * [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/) on Mac
* **Windows 10 or above**
  * [Docker Desktop for windows](https://docs.docker.com/docker-for-windows/install/#system-requirements-for-wsl-2-backend) need to be installed
  * [Install Chocolatey](https://chocolatey.org) package manager for windows 
  * [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/) on Windows
  * Install [GitBash](https://git-scm.com/download/win) as an alternative command prompt that allows most of the Linux commands on windows.

### **Infra Creation**

**Once the above prerequisites are met, run the following tasks depending upon your OS.**

* [ ]  ****login/ssh into the machine, go to terminal/command prompt and run the following commands as an admin user.
* [ ] Create /Kube directory and change permission. To use this directory for persistent data mount. This means all the container logs, data will be stored here.

```text
 mkdir /kube
 chmod 777 /kube
```

* [ ] Create a cluster with a single master node and 2 agents \(Worker Nodes\) and mount the pre**-**created directory \(for data persistence\). 

```text
k3d cluster create --agents 2 -v /kube:/kube@agent[0,1] -v /kube:/kube@server[0]
```

* [ ] When cluster creation is successful, Get the kubeconfig file, which will allow you to connect the to the cluster at any time.

```text
k3d kubeconfig get k3s-default > k3dconfig
kubectl config use-context k3s-default --kubeconfig=k3dconfig
```

* [ ] Verify the Cluster creation by running the following commands from your local machine where the kubectl is installed. It gives you the sample output as below

```text
root@ip:/# kubectl cluster-info

OutPut:
Kubernetes control plane is running at https://0.0.0.0:33931
CoreDNS is running at https://0.0.0.0:33931/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
Metrics-server is running at https://0.0.0.0:33931/api/v1/namespaces/kube-system/services/https:metrics-server:/proxy
 
 
 
root@ip:/# k3d cluster list
NAME          SERVERS   AGENTS   LOADBALANCER
k3s-default   1/1       2/2      true
```

* [ ] You can verify the workers' nodes created by using the following command.

```text
kubectl get nodes
 
Output:
NAME                       STATUS   ROLES                  AGE     VERSION
k3d-k3s-default-agent-0    Ready    <none>                 3d18h   v1.21.1+k3s1
k3d-k3s-default-agent-1    Ready    <none>                 3d18h   v1.21.1+k3s1
k3d-k3s-default-server-0   Ready    control-plane,master   3d18h   v1.21.1+k3s1
 
 
kubectl top nodes

Output:
W0625 07:56:24.588781   12810 top_node.go:119] Using json format to get metrics. Next release will switch to protocol-buffers, switch early by passing --use-protocol-buffers flag
NAME                       CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%   
k3d-k3s-default-agent-0    547m         6%     1505Mi          9%        
k3d-k3s-default-agent-1    40m          0%     2175Mi          13%       
k3d-k3s-default-server-0   59m          0%     2286Mi          14%  
 
```

If the above steps are completed successfully, your Cluster is now up and running ready to proceed with the DIGIT Deployment.

## **2. DIGIT Setup**

Now that we have the Infra setup to proceed with the DIGIT Deployment. Following are the tools that need to be installed on the machine before proceeding with the DIGIT Services deployment.

### **Prerequisites**

1. DIGIT uses [golang](https://golang.org/doc/install#download) \(required v1.13.3\) automated scripts to deploy the builds on to Kubernetes - [Linux](https://golang.org/dl/go1.13.3.linux-amd64.tar.gz) or [Windows](https://golang.org/dl/go1.13.3.windows-amd64.msi) or [Mac](https://golang.org/dl/go1.13.3.darwin-amd64.pkg)
2. All DIGIT services are packaged using helm charts[ ![](https://helm.sh/img/favicon-152.png)Installing Helm](https://helm.sh/docs/intro/install/)
3. [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/) is a CLI to connect to the kubernetes cluster from your machine
4. [Install Visualstudio](https://code.visualstudio.com/download) IDE Code for better code/configuration editing capabilities
5. All the DIGIT services deployment configurations are in [GitRepo](https://github.com/egovernments/DIGIT-DevOps) which you would need to [install git](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository) and then [git clone](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository) it to your local.

```text
root@ip:/# git clone -b quickstart https://github.com/egovernments/DIGIT-DevOps 
```

  6. After cloning the repo CD into the folder DIGIT-DevOps and type the "code ." command that will open the visual editor and opens all the files from the repo DIGIT-DevOps

```text
root@ip:/# cd DIGIT-DevOps
root@ip:DIGIT-DevOps# code .
```

  7. Have look at the [sample deployment config file](https://github.com/egovernments/DIGIT-DevOps/blob/quickstart/deploy-as-code/helm/environments/quickstart-config.yaml) that needs to be configured as per any specific values according to your needs. \(For a quick start you can run as it is\)

```text
https://github.com/egovernments/DIGIT-DevOps/blob/quickstart/deploy-as-code/helm/environments/quickstart-config.yaml
```

 8. Add the following entries in your host file /etc/hosts depending on your OS, instructions can be found [here](https://phoenixnap.com/kb/how-to-edit-hosts-file-in-windows-mac-or-linux). 

```text
172.18.0.2 quickstart.local.digit
172.18.0.3 quickstart.local.digit
172.18.0.4 quickstart.local.digit
```

### Deployment

Once all the prerequisites set up is complete, go to the following repo, run the command and follow the instructions.

```text
root@ip:# cd DIGIT-DevOps/deploy-as-code/egov-deployer

root@ip:# go run digit_setup.go

#Be prepared for the following questions
1. Do you have the Kubernetes Setup?
2. Provide the path of the intented env kubeconfig file
3. Which version of the DIGIT that you want to install - Choose "Quickstart"
4. What DIGIT Modules that you choose to install
5. All, done, Now do you want to preview the deployment manifests 
6. Are you good to proceed with the DIGIT Installation

All Done.
```




