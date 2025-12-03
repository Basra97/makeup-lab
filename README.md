# Makeup Lab: Infrastructure as Code & Configuration Management

## Overview
This project provisions AWS infrastructure using Terraform and configures Web and Database servers using Ansible.

## Steps Used to Complete the Lab

### 1. SSH Key Setup
Generated an SSH key pair locally and uploaded it to AWS using a custom Bash script.
bash
Generate Key
ssh-keygen -t ed25519 -f ~/.ssh/lab-key -C "lab-key"

Upload to AWS
chmod +x scripts/import_key.sh
./scripts/import_key.sh ~/.ssh/lab-key.pub

Enter the Terraform folder:

```
cd terraform
```

Initialize Terraform:

```
terraform init
```

Format:

```
terraform fmt
```

Validate:
```
terraform validate
```

Plan and Apply:
```
terraform plan
terraform apply
```


Configure Ansible

cd ../ansible

ansible-playbook -i hosts.ini playbook.yml


Web Server Output
![Description](./images/hello-from-web-proof.png)

Database Server Output
![Description](./images/hello-from-database-proof.png)
```
