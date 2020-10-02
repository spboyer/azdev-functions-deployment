# Deploy Azure Function linked to GitHub Repo
<!--
<a href="https://portal.azure.com/?WT.mc_id=azdevfunctionsdeployment-github-shboyer#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fazure%2Fazure-quickstart-templates%2Fmaster%2F201-web-app-github-deploy%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-web-app-github-deploy%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>
--> 
[Docs](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-template-deploy-cli?WT.mc_id=azdevfunctionsdeployment-github-shboyer)

Example parameters

```javascript
 {
   "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentParameters.json?WT.mc_id=azdevfunctionsdeployment-github-shboyer#",
   "contentVersion": "1.0.0.0",
   "parameters": {
      "appName": {
          "value": "myappname"
      },
      "storageAccountName": {
          "value": "myStorage"
      },
      "storageAccountType": {
          "value": "Standard_LRS"
      },
      "repoURL": {
          "value": "https://github.com/spboyer/azdev-superhero-api.git"
      },
      "branch": {
          "value": "master"
      },
      "location": {
          "value": "East US"
      }
   }
 }
```

Deploy using parameters file

```bash
az group create --name MyResourceGroup --location "East US"

az group deployment create --name MyDeployment --resource-group MyResourceGroup --template-file azuredeploy.json --parameters @parameters.json
```

Deploy using command line parameters

```bash
az group create --name MyResourceGroup --location "East US"

az group deployment create --name MyDeployment --resource-group MyResourceGroup --template-file azuredeploy.json \
     --parameters '{"appName":{"value":"myfunckytestdeploy"},"storageAccountName":{"value":"myStorageName"},"storageAccountType":{"value":"Standard_LRS"},"repoURL":{"value":"https://github.com/spboyer/azdev-superhero-api.git"},"branch":{"value":"master"},"location":{"value":"East US"}}'

```


---

> [tattoocoder.com](https://tattoocoder.com) &nbsp;&middot;&nbsp;
> GitHub [@spboyer](https://github.com/spboyer) &nbsp;&middot;&nbsp;
> Twitter [@spboyer](https://twitter.com/spboyer)