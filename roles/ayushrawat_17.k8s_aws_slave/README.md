## Kubernetes AWS Slave

This Role used to configure the Kubernetes Worker Node on the AWS Linux 2 with the Container Engine **Docker** and CNI **Flannel**.If we use the `ayushrawat_17.k8s_aws_master` role before configuring master for this Worker Node it automatically gets the token from there else we can also provide the token and ca certificate Id manually.

## Requirements

- boto3 Library is required to contact to the AWS

## Role Variables

**If you are using this role without the Dependence `ayushrawat_17.k8s_aws_master` then updates this Variables**
  - **hostvar_token_present** &nbsp; Change value to *no*
  - **kube_join_token** &nbsp; Put your Kubernetes Join Token
  - **ca_cert_hash** &nbsp; Put your Kubernetes Join CA certificate hash
  - **master_ip** &nbsp; Provide the Master Node IP
  - **master_portno** &nbsp; Provide the Master node Port number

## Dependencies

- `ayushrawat_17.k8s_aws_ec2` Role is required for Provisioning of Desired Infrastructure
- `ayushrawat_17.k8s_aws_master` Role is required for configuring Master for this Worker Node

**Example Playbook**
----------------

```yaml
---
    - hosts: servers
      roles:
         - role: ayushrawat_17.k8s_aws_slave
```

## License
BSD

## Author Information
 - **Ayush Rawat** (ayushrawatkv@gmail.com)
     - https://twitter.com/rawatayush17