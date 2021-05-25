# MultiNode Kubernetes Cluster Using Ansible

This Ansible Project is used to configure the **Multinode Kubernetes cluster** on **AWS** on the **AMI Amazon Linux 2** with Container Engine **Docker** and CNI **Flannel** using the Ansible playbook and roles.</br>
It first Launches an instance on AWS  Master node and Worker node according to our choice. Then it contacted this contact to the Instances and configures the Master node after that Worker Nodes.

# Getting Started

This how you may start using this Project.

### Prerequisites
   - Install Python 3 on your System.
   - Install Ansible using **pip**.</br>
       > `pip3 install ansible`
   - Install **boto3** python Library using **pip**.</br>
       > `pip3 install boto3` 
   - Install and Configure **AWS CLI 2** (also create a profile).
   -  Create a AWS private key by the name of **awskey**.
   
### Installation

  1. Clone the Repository </br>
    `git clone https://github.com/AyushRawat-17/Ansible_K8S_Configuration.git`
  2. Copy the Private key to the root Directory of the repo.



 
