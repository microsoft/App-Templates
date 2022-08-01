# App Templates

App Templates are packaged app samples designed to reduce the time it takes a developer to deploy their code to Azure. Unlike standalone example code, the goal of App Templates is to provide all the components to deploy an app to Azure with automation via GitHub Actions or other CI/CD services. 

Each sample consists of example code, CI/CD components, and documentation containing all the required steps.

App Templates are designed to be compatible with [Azure Accelerators](https://github.com/Azure/azure-dev/) which are currently in preview. These templates follow the same file structure and are straightforward to convert to Azure Accelerators once all the components of the template (e.g. programming language) are supported. The purpose of App Templates is to deliver the value of accelerated onboarding for developers who are new to Azure, without needing to go through all the Azure Accelerator steps. App Templates which prove valuable are then simple to convert to Azure Accelerators at a later date.

## Pre-requisites
- Azure Subscription and you must be the owner(or know the owner) of the subscription for configuring automatated deployments

## Sample templates

- [Static Web App with Cosmos DB](https://github.com/microsoft/csu-digiapps-p-azure-function-graphql-cosmosdb)
- [.NET app on App Service](https://github.com/Azure-Samples/app-templates-dotnet-azuresql-appservice)
- Java Spring boot on AKS / LZA (coming soon)
- [Node.js - Azure Graph - CosmosDB](https://github.com/microsoft/csu-digiapps-p-azaccel-cosmos-graph-nodejs) (coming soon)
- 


## Contributing

- Identify a sample app you plan to make into an app template
- Follow steps 1-3 listed here: [How to Azure dev enable (aka dev ify) a project](https://github.com/Azure/azure-dev/wiki/How-to-Azure-dev-enable-(aka-dev-ify)-a-project)
- Add .devcontainer, .github and .github/workflow components

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
