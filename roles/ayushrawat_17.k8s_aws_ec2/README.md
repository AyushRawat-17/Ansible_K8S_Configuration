# Kubernetes AWS EC2  

This role used for Provisioning of  Security Group and  EC2 instance on AWS Cloud for Kubernetes Master and Kubernetes Worker Nodes of AMI **Amazon Linux 2** in Region **ap-south-1**  with Instance type **t2.micro**. It launches 1 Master Node and Worker Nodes according to the specfied requirement.

## Requirements

- boto and boto3 python Library.
- AWS CLI must be configured in the OS with some profile.
- Precreated private key also required. 

## Role Variables

In vars/main.yml variables to be specfied
 - **key** Change the private key name you have created to attach to AWS instances.
 - **aws_cli_profile** Provide AWS CLI profile in this variable
 - **k8s_sg_name** Provide the security group name 
 - **no_of_slave** Provide the No. of worker Nodes as per the requirement  

## Example Playbook

```yaml
---
- hosts: localhost
  gather_facts: no
  roles:
    - role: ayushrawat_17.k8s_aws_ec2
```

## License
BSD
## Author Information
   - **Ayush Rawat** (ayushrawatkv@gmail.com)
     - https://twitter.com/rawatayush17
