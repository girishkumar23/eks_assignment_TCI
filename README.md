# EKS ASSIGNMENT TCI
* Language Used :   
Terraform
* Prerequisites :   
Aws EC2 Instance with any configuration (like any AMI,Storage capacities,and
Install Terraform
Install Aws Cli 
Install Git
## Overview :
Deploying a Kubernetes cluster on local machine with 2 worker nodes and hosting nginix Web Server. Scripts are written in Terraform.
## Steps to Run the Code
* Step 1 : Clone all the committed files by using given url (Command : clone ------url--------).
* Step 2 : Create dirctory as "TerraformDir" and then inside of TerraformDir directory create one more directory as "assign" change the current directory to "assign". 
* Step 3 : Move all comitted files to respective path as TerraformDir/assign directory (by mv command).
* Step 4 : vi the main.tf file and Pass your own "vpc id and subnet id" at cluster module.
* Step 5 : Hit command as "terraform init".
* Step 6 : After Successful completion of step-5, Hit command as "terraform plan" (provide aws region, where you want to create your infra just like "ap-south-1") 
* Step 7 : After Succssful completion  of step-6, Hit command as "terraform apply" (Pass Yes, when it asks)
* Step 8 : Check your Infra at aws by GUI.
* Step 9 : Use terraform destroy, to destroy all your infra at any time.
## Accessing EKS using AWS CLI
* Hit following three command seqentially in master to access EKS by CLI.
* aws eks --region region update-kubeconfig --name cluster_name
* kubectl get pods --kubeconfig ./.kube/config
* kubectl get svc
## Deploy the Applications using YAML Files
* Hit following commands in master to deploy our desired application in respective nodes
* kubectl create -f Name.yaml
* kubectl get pods
* 
