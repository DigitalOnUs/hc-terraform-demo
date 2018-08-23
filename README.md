## ModuleTwo
NOTE 
- You will have to create an aws account and create and a key pair in EC2 or import your own key to AWS before you start


1. Create an AWS instance (nginx1) in a VPC
2. Update the tf template to include a 2nd instance nginx2 in a different subnet and add a ELB infront of the two nginx servers


### Requirement:
Need a terraform.tfvars file with AWS creds and private key path

```
$ cat ../terraform.tfvars 
aws_access_key = "your-aws-access-key"
aws_secret_key = "your-aws-secret-key"
private_key_path = "/Users/username/aws/keys"
key_name  = "your-aws-ssh-privatekey-filename"
```
### Terraform commands:
```
terraform plan -var-file='../terraform.tfvars'
terraform apply -var-file='../terraform.tfvars'
terraform destroy -var-file='../terraform.tfvars'
```
.

