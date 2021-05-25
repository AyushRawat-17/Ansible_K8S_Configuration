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
  2. Copy the Private key to the root Directory of the project.

# Usage

   ### Setting up the Roles Variables for Configuration
   - **For Role ayushrawat_17.k8s_aws_ec2**</br>
      1. In the root directory of the project execute</br>`cd ./roles/ayushrawat_17.k8s_aws_ec2/vars`
      2. Then open the **main.yml** using a text editor like **vim**</br>
          eg-> `vim main.yml` 
      3. Variable to be updated are 
         - **no_of_slave** - To upate the number to slave node you required
         - **aws_cli_profile** - Update it to your AWS CLI profile
         Rest of variables remain same
         
  - **For role ayushrawat_17.k8s_aws_master**</br>
         In this role there is no variable update is required
         
  - **For role ayushrawat_17.k8s_aws_slave**
       1. In the root directory of the project execute</br>`cd ./roles/ayushrawat_17.k8s_aws_slave/vars`
       2. Then open the **main.yml** using a text editor like **vim**</br>
          eg-> `vim main.yml`  
       3. Variable to be updated are
            **if you are using this role without the ayushrawat_17.k8s_aws_master role upadate the following variable else not required**
            - **hostvar_token_present** - Change it to no
            - **kube_join_token** - Put the Token in this variable
            - **ca_cert_hash**- Put the CA certificate hash
            - **master_ip** - Put the master node IP Address
            - **master_portno** - Put the master Port Number
       
     ### Now run the Playbook 
      1. Go back to Root directory of Project
      2. Then Execute the following Command</br>
         `ansible-playbook -v role.yml`
           
 # Contact
   **Ayush Rawat** - @rawatayush17 - ayushrawatkv@gmail.com</br>
   Project Link: https://github.com/AyushRawat-17/Ansible_K8S_Configuration 
 
