# App Service with Terraform

Following the official how to

https://learn.microsoft.com/en-us/azure/app-service/provision-resource-terraform


export TF_VAR_AZURE_RESOURCE_GROUP=learn-0ab760e8-42da-4282-96c8-284aa60a8e7d
export TF_VAR_AZURE_APP_SERVICE_REPO_URL='https://github.com/mawadam/2023-25.IDT.UFS05'

terraform init

terraform import azurerm_resource_group.rg '/subscriptions/b7aef7d5-cb67-46b2-b7e3-464cdfc6a6f5/resourceGroups/learn-0ab760e8-42da-4282-96c8-284aa60a8e7d'

az webapp log tail --name '...' --resource-group $TF_VAR_AZURE_RESOURCE_GROUP


node-red-dashboard

terraform destroy --target azurerm_linux_web_app.python_webapp
