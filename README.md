# makeup-lab


Steps Used to Complete the Lab
1. Generate an SSH key
ssh-keygen -t ed25519 -f ~/.ssh/lab-key -C "lab-key"

2. Upload key to AWS

`chmod +x import_key.sh
./import_key.sh ~/.ssh/lab-key.pub`

3. Deploy AWS resources with Terraform

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


Web Server Output


Database Server Output

