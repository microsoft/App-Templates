Description: 

Creating a VueJS Single Page Application on a Static Web App, which queries CosmosDB data through a GraphQL endpoint hosted on an Azure Function
--
Tech stack:

- Azure
- Azure Cosmos DB
- Azure Functions
- Azure Front Door
- Github Actions
- Bicep
- GraphQL
- VueJS

---

## Introduction

This is a quickstart template. It deploys the following:

- CosmosDB instance with ToDo list sample content
- Azure Function exposing a GraphQL endpoint to retrieve ToDo lists and list items
- Single Page Application (VueJS) that shows the content of the to-do lists
- Azure Front Door instance exposing endpoints to the outside world

> Refer to the [App Templates](https://github.com/microsoft/csu-digiapps-p-azaccel) repo Readme for more samples that are compatible with [AzureAccelerators](https://github.com/Azure/azure-dev/).

## Prerequisites
- Local shell with Azure CLI installed or [Azure Cloud Shell](https://ms.portal.azure.com/#cloudshell/)
- Azure Subscription, on which you are able to create resources and assign permissions
  - View your subscription using ```az account show``` 
  -  If you don't have an account, you can [create one for free](https://azure.microsoft.com/free).  

## Getting Started
### Fork the repository

Fork the repository by clicking the 'Fork' button on the top right of the page.
This creates a local copy of the repository for you to work in. 

### Azure Configuration for GitHub  

The newly created GitHub repo uses GitHub Actions to deploy Azure resources and application code automatically. Your subscription is accessed using an Azure Service Principal. This is an identity created for use by applications, hosted services, and automated tools to access Azure resources. The following steps show how to [set up GitHub Actions to deploy Azure applications](https://github.com/Azure/actions-workflow-samples/blob/master/assets/create-secrets-for-GitHub-workflows.md)

Create an [Azure Service Principal](https://docs.microsoft.com/en-us/cli/azure/create-an-azure-service-principal-azure-cli) with **contributor** permissions on the subscription. The subscription-level permission is needed because the deployment includes creation of the resource group itself.
 * Run the following [az cli](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest) command, either locally on your command line or on the Cloud Shell. 
   Replace {subscription-id} with the id of the subscription in GUID format. {service-principal-name} can be any alfanumeric string, e.g. GithubPrincipal
    ```bash  
       az ad sp create-for-rbac --name {service-principal-name} --role contributor --scopes /subscriptions/{subscription-id} --sdk-auth      
      ```
 * The command should output a JSON object similar to this:
 ```
      {
        "clientId": "<GUID>",
        "clientSecret": "<GUID>",
        "subscriptionId": "<GUID>",
        "tenantId": "<GUID>",
        "activeDirectoryEndpointUrl": "<URL>",
        "resourceManagerEndpointUrl": "<URL>",
        "activeDirectoryGraphResourceId": "<URL>",
        "sqlManagementEndpointUrl": "<URL>",
        "galleryEndpointUrl": "<URL>",
        "managementEndpointUrl": "<URL>"
      }
   ```
 * Store the output JSON as the value of a GitHub secret named 'AZURE_CREDENTIALS'
   + Under your repository name, click Settings. 
   + In the "Security" section of the sidebar, select Secrets. 
   + At the top of the page, click New repository secret
   + Provide the secret name as AZURE_CREDENTIALS
   + Add the output JSON as secret value

### GitHub Workflow setup
1. Change the value of DEPLOYMENT_NAME and DEPLOYMENT_REGION in the build-deploy.yaml workflow file under .github/workflows. 
   * The value for DEPLOYMENT_NAME should be globally unique, e.g. yournamedemo1
   * Use only lowercase letters and numbers for DEPLOYMENT_NAME. 
   * DEPLOYMENT_REGION should contain an Azure region name, e.g. westeurope, southcentralus, brazilsouth
2. Run the workflow 
   * If workflows are enabled for this repository it should run automatically. To enable the workflow run automatically, Go to Actions and enable the workflow if needed.
   * Workflow can be manually run 
     + Under your repository name, click Actions .
     + In the left sidebar, click the workflow "Build and Deploy Application".
     + Above the list of workflow runs, select Run workflow .
     + Use the Branch dropdown to select the workflow's main branch, Click Run workflow .
   * The workflow will create an Azure Resource Group using DEPLOYMENT_NAME as a prefix. 

# To-Do List website
Once successfully deployed, the application is accessible through the Front Door endpoint hostname ending in azurefd.net. You can find it by looking on the 'actions' tab on Github, where the latest run will show the URL on the summary page. Alternatively, you can look at the "Front Door and CDN Profiles" resource in your Resource Group through the [Azure Portal](https://portal.azure.com). Optionally, a [custom domain](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain) can be added to Front Door. 

![Screenshot of the todolist webpage](/assets/todolistmanager.png)
