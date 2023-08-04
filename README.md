##### Status of Last Deployments:

###### &emsp; Deployment infrastructure:<br> &emsp; ![Build Status](https://github.com/DAChirkov/test_project_0001/actions/workflows/azure_terraform.yml/badge.svg)

###### &emsp; Deployment configuration:<br> &emsp; ![Build Status](https://github.com/DAChirkov/test_project_0001/actions/workflows/azure_ansible.yml/badge.svg)

##### Required prerequisites for Azure:
```  
Step1 - Create SSH keys
--------
AZURE_SSH_KEY: generate new SSH keys and add client private SSH key 
Change:
- "variable "resource_ssh_servers_public_key" string in main variables.tf
- "variable "resource_ssh_clients_public_key" string in main variables.tf

Step2 - Create a Service Principal  
--------
AZURE_CLIENT_ID: client id value of your service principal
AZURE_CLIENT_SECRET: client secret value of your service principal  
AZURE_SUBSCRIPTION_ID: subscription id value of your service principal  
AZURE_TENANT_ID: tenant id value of your service principal
>>> \pre-requisites\terraform\Service_principal.ps1  

Step3 - Create a Storage Account  
--------
AZURE_STORAGE_SECRET: secret value of your storage account
>>> \pre-requisites\terraform\Service_storage.ps1

Step4 - Add Docker's Secrets  
--------
DOCKER_USERNAME: secret value of your repo
DOCKER_PASSWORD: secret value of your token
```
