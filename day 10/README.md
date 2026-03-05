# 📘 Kubernetes Environment Setup – Learning Summary

## 📖 About This Learning

Today, I started learning **Kubernetes** by setting up a local environment. I installed **Oracle VirtualBox**, created a **Ubuntu Server virtual machine**, and configured it to practice Kubernetes.

I connected to the Ubuntu server from the **Windows command line using SSH**, which allowed me to manage the server remotely. After setting up the server, I began preparing the system for Kubernetes by installing container runtime and Kubernetes tools.

---

## 🧠 What I Learned

- Installing **VirtualBox** for virtualization
    
- Creating and configuring an **Ubuntu Server VM**
    
- Connecting to the server remotely using **SSH from Windows CLI**
    
- Preparing the server for Kubernetes installation
    
- Understanding the basic components required for Kubernetes setup
    

---

## ⚙️ Kubernetes Setup Commands Practiced

System update and required packages:

apt update  
apt install -y apt-transport-https ca-certificates curl gpg

Add Kubernetes repository and key:

mkdir -p /etc/apt/keyrings  
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.29/deb/Release.key | gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg  
echo "deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.29/deb/ /" | tee /etc/apt/sources.list.d/kubernetes.list

Install container runtime:

sudo apt install -y containerd  
sudo mkdir -p /etc/containerd  
sudo containerd config default | sudo tee /etc/containerd/config.toml  
sudo systemctl restart containerd  
sudo systemctl enable containerd

Install Kubernetes tools:

apt update  
apt install -y kubelet kubeadm kubectl  
apt-mark hold kubelet kubeadm kubectl

Disable swap (required for Kubernetes):

sudo swapoff -a  
free -m

These commands were used to prepare the Ubuntu server for running a **Kubernetes master node**.

---

## 🎯 Learning Outcome

- Understood how to create a virtual environment for Kubernetes
    
- Learned how to connect to a Linux server using SSH
    
- Installed container runtime (**containerd**)
    
- Installed Kubernetes components (**kubelet, kubeadm, kubectl**)
    
- Prepared the system for Kubernetes cluster initialization