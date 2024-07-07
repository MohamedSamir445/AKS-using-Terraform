# AKS-using-Terraform
# AKS-using-Terraform
Create Resources using Terraform 

terraform init –upgrade 

terraform plan -out main.tfplan

terraform apply main.tfplan
=========================================================================================================================
Verify the results

az login

az account set --subscription your-subscription-id 

az aks get-credentials --resource-group rg-your-rg-name --name cluster-your-cluster-name

Note: Replace these commands with your details or copy these commands directly from portal.
=========================================================================================================================
Deploy Application
Kubectl apply –f deployment.yaml

Kubectl apply –f service.yaml

 Kubectl get svc 
=========================================================================================================================
destroy infrastructure


kubectl get all

kubectl delete service/swiggy-app

kubectl delete deployment.apps/swiggy-app

terraform plan -destroy -out main.destroy.tfplan 

terraform apply "main.destroy.tfplan" 

