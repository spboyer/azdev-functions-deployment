# Deploy Azure Function linked to GitHub Repo

<!--
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fazure%2Fazure-quickstart-templates%2Fmaster%2F201-web-app-github-deploy%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-web-app-github-deploy%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>
--> 
[Docs](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-template-deploy-cli)

Example parameters
```javascript
 {
   "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentParameters.json#",
   "contentVersion": "1.0.0.0",
   "parameters": {
      "appName": {
          "value": "myappname"
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