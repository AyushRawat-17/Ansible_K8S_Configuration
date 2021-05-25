## Kubernetes AWS Master

This Role used to cofigure the Kubernetes Master on the Amazon Linux 2 with the Container Engine Docker and CNI Flannel.

## Requirements

- **boto3** Library is required to contact to the AWS

Dependencies
------------

 For provisioning of infrastructure `ayushrawat_17.k8s_aws_ec2` roles is required to configured the desired configuration but without this role infrastucture can also be created only requirement is the **Amazon Linux 2** .

## Example Playbook

```yaml
---
    - hosts: tag_type_master
      roles:
         role: ayushrawat_17.k8s_aws_master
```

## License

BSD

## Author Information
 - **Ayush Rawat** (ayushrawatkv@gmail.com)
     - https://twitter.com/rawatayush17