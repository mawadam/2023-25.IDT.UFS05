# App Service with Terraform

Following the official how to

https://learn.microsoft.com/en-us/azure/app-service/provision-resource-terraform


export TF_VAR_AZURE_RESOURCE_GROUP=learn-ee597dd3-bff1-427c-b29c-3fca4db62cc0
export TF_VAR_AZURE_APP_SERVICE_REPO_URL='https://github.com/mawadam/2023-25.IDT.UFS05'

terraform init

terraform import azurerm_resource_group.rg '/subscriptions/45b351fe-c7e8-4cb4-82e4-ff3615698d8d/resourceGroups/learn-ee597dd3-bff1-427c-b29c-3fca4db62cc0'

az webapp log tail --name '...' --resource-group $TF_VAR_AZURE_RESOURCE_GROUP


node-red-dashboard

terraform destroy --target azurerm_linux_web_app.python_webapp
