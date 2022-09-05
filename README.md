# Summary
### k8s version : 1.22.12
### CRI : docker
### CNI : flannel
### OS : CentOS 7.9 GNOME DESKTOP
### provisioner : nfs
### kubeflow version : 1.6
### kustomize : 3.2.0
#
# Simple Explanation about this repository
### 1. create_cluster.sh creates 1 master and multiple worker nodes
### 2. create_cluster.sh can be executed only on master node
### 3. create_cluster.sh enables both root and one administrator account to use kubectl auto completion
### 4. craete_cluster.sh installs gpu operator. If your cluster doesn't have any gpus, please comment the gpu operator installation line in create_cluster.sh"
### 5. create_kubeflow.sh must be executed after create_cluster.sh which means k8s and gpu operator should have already been installed
### 6. create_kubeflow.sh uses nfs provisioner
#
# How to use this repository
### 1. fix ips and change hostnames of every node
### 2. install sshpass on every node
### 3. use same account and password through all nodes(optional but recommended)
### 4. make groups 'nodes', 'master', 'worker' and write ips in /etc/ansible/hosts
### 5. input right values into 'admin', 'master_ip', 'nfs_ip', 'nfs_path' in create_cluster.sh & create_kubeflow.sh
