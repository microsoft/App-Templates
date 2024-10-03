# App Templates

App Templates are packaged app samples designed to reduce the time it takes a developer to deploy their code to Azure. Unlike standalone example code, the goal of App Templates is to provide all the components to deploy an app to Azure with automation via GitHub Actions or other CI/CD services. 

Each sample consists of example code, CI/CD components, and documentation containing all the required steps.

App Templates are designed to be compatible with the [Azure Developer CLI(azd)](https://github.com/Azure/azure-dev/). These templates follow the same file structure and are straightforward to convert to `azd` compatible templates once all the components of the template (e.g. programming language) are supported. 

App Templates are open to any technology some may not be on the azd roadmap and can be deployed using the READ ME guidance. The purpose of App Templates is to deliver and prove the value of accelerated onboarding for developers who are new to Azure. Developing examples for `azd` is one of our aims that fit into the broader goal of accelerated developer onboarding.

If you are looking for enterprise scale guidance on design pillars like Reliability, Performance, Networking, leverage design areas recommendation and reference implementation on [Landing Zone Accelerators](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/app-platform/ready)

## Pre-requisites
- Azure Subscription and you must be the owner(or know the owner) of the subscription for configuring automated deployments

## Sample templates

|Template | Usecase | Azure Services|
|----|----|----|
|[AI Retrieval Augmented Generation (RAG) pattern with Azure Open AI using your own data for C#](https://github.com/Azure-Samples/azure-search-openai-demo-csharp)|This sample demonstrates a few approaches for creating ChatGPT-like experiences over your own data using the Retrieval Augmented Generation pattern. It uses Azure OpenAI Service to access a GPT model (gpt-35-turbo), and Azure AI Search for data indexing and retrieval.| Azure Open AI, .NET, Azure App Serivce, Azure AI Search |
|[AI Retrieval Augmented Generation pattern with Azure Open AI using your own data for Java](https://github.com/Azure-Samples/azure-search-openai-demo-java)| This app template is the Java version of the above RAG pattern AI sample. It uses Azure OpenAI Service to access a GPT model, and Azure Azure AI Search for data indexing and retrieval. The result is a chat-with-your-data implementation. | Azure Open AI, Java, Azure App Serivce, Azure AI Search |
|[AI Retrieval Augmented Generation pattern with Azure Open AI using your own data for Python](https://github.com/Azure-Samples/azure-search-openai-demo)| This app template is the Python version of the above RAG pattern AI sample. It uses Azure OpenAI Service to access a GPT model, and Azure Azure AI Search for data indexing and retrieval. The result is a chat-with-your-data implementation. | Azure Open AI, Python, Azure App Serivce, Azure AI Search |
|[AI Retrieval Augmented Generation pattern with Azure Open AI using your own data for JavaScript](https://github.com/Azure-Samples/azure-search-openai-javascript)| This app template is the JavaScript version of the above RAG pattern AI sample. It uses Azure OpenAI Service to access a GPT model, and Azure Azure AI Search for data indexing and retrieval. The result is a chat-with-your-data implementation. | Azure Open AI, JavaScript, Azure App Serivce, Azure AI Search |
|[.NET app on App Service](https://github.com/Azure-Samples/app-templates-dotnet-azuresql-appservice)| Sample application that demonstrates how to deploy ASP.NET Core web app to App Service.| App Service, Azure SQL, Load Testing, App Insights, Key Vault|
|[Integration Services - APIM + ServiceBus + Functions + Cosmos](https://github.com/Azure-Samples/app-templates-integration-services)| Sample integration app template that walks through setting up API Management policy for sending data to Azure Service Bus. The API Management uses Managed Identity to access the Service Bus REST APIs. A Function is triggered when a message is queued in Service Bus, and it will write message data to Cosmos DB. The Function App uses Managed Identity to get access to Service Bus | APIM, Service Bus, Functions, Cosmos|
|[WordPress on Azure Container Apps](https://github.com/Azure-Samples/apptemplate-wordpress-on-ACA)| In this application template, you'll learn how to and will be able to easily, quickly create and deploy your first scalable and secure WordPress site to Azure, leveraging Azure Container Apps with Azure Database for MariaDb. |Azure Container Apps, APIM, App Service, Functions|
|[Java SpringApp with Azure OpenAI](https://github.com/Azure-Samples/app-templates-java-openai-springapps)| AI Shopping Cart Sample Application with Azure OpenAI and Azure Spring Apps | Azure OpenAI, Spring Apps, App Insights|
|[Microservices integration - APIM + Container Apps + AppService + Functions](https://github.com/Azure-Samples/app-templates-microservices-integration)| This sample leverages the Reddog codebase and the Reddog Container Apps bicep modules. It was created to help users deploy a comprehensive, microservice-based sample application to Azure Container Apps, Azure App Service, Azure Functions, and Azure API Management. |Azure Container Apps, APIM, App Service, Functions,Azure Service Bus and Azure Cache for Redis|
|[JBoss EAP on Appservice](https://github.com/Azure-Samples/app-templates-JBossEAP-on-AppService)| This sample Pet Store application is built with Maven and deployed to an Azure App Service secured by Azure Firewall | Azure User Defined Routing (UDR), Azure Application Inisghts, Azure Log Analytics, Azure Application Gateway, Azure Fire Wall, Azure Bastion, Azure App Service, Azure PostgreSQL DB|
|[Jakarta EE IBM Open Liberty on AKS](https://github.com/Azure-Samples/app-templates-Liberty-on-aks)| This is a sample app template of the Domain-Driven Design Jakarta EE application. The application is built with Maven and deployed to Open Liberty running in Azure Kubernetes Service (AKS). The app template uses the official Azure offer for running Liberty on AKS. The application is exposed by Azure Load Balancer service via Public IP address. | Azure Container Registry, Azure Kubernetes Service, Azure PostgreSQL DB|
|[Jakarta EE Oracle WebLogic Server (WLS) on AKS](https://github.com/Azure-Samples/app-templates-WLS-on-aks)| This is a sample app template of the Domain-Driven Design Jakarta EE application. The application is built with Maven and deployed to Oracle WebLogic Server running in Azure Kubernetes Service (AKS). The app template uses the official Azure offer for running WLS on AKS. For a quickstart on this offer, see https://aka.ms/wls-aks-quickstart. The application is exposed by Azure Application Gateway  | Azure Infra (VNet), Azure Storage Account, Azure Container Registry, Azure Kubernetes Service, Azure Application Gateway, Azure PostgreSQL DB|
|[Java Spring boot on AKS](https://github.com/Azure-Samples/app-templates-springboot-app-on-AKS)| In this sample app template, the PetClinic application (a Spring Boot based app) is containerized and deployed to a AKS cluster secured by Azure Firewall  | Azure PostgreSQL DB, Azure Container Registry (ACR), Azure Kubernetes Service (AKS), Azure Infra (Vnet/Subnet), Azure Fire Wall, Azure Bastion|
|[Java microservices based spring boot on AKS](https://github.com/Azure-Samples/app-templates-springboot-microservices-on-AKS)| In this sample app template of the PetClinic Microservices application (a Spring Boot based app). Each of the application microservices are containerized and deployed to an Azure Kubernetes Service (AKS) cluster secured by Azure Firewall | Azure User Defined Routing (UDR), Azure Application Inisghts, Azure Log Analytics, Azure Application Gateway, Azure Fire Wall, Azure Bastion, Azure Container Registry (ACR), Azure Kubernetes Service (AKS) Cluster, Azure PostgreSQL DB|
|[Spring Boot PetClinic Microservices Application on Azure Red Hat Openshift (ARO)](https://github.com/Azure-Samples/app-templates-springboot-microservices-on-ARO)| In this sample app template, the PetClinic application (a Spring Boot based app) is containerized and deployed to an Azure RedHat Openshift (ARO) cluster secured by Azure Firewall | Azure RedHat Openshift (ARO), Azure Container Registry (ACR), MySql DB|
|[Spring Boot on Azure Spring Apps](https://github.com/Azure-Samples/apptemplates-microservices-spring-app-on-AzureSpringApps)| This example shows you how to deploy an existing Java Spring Boot/Cloud application to Azure Spring Apps. When you're finished, you can continue to manage the application with Azure services via the Azure CLI, Bicep templates or switch to using the Azure Portal.  | Azure Spring Apps, APIM, Azure Cache for Redis, App Insights, Key Vault|
|[Static Web App with Cosmos DB](https://github.com/Azure-Samples/app-templates-staticwebapp-cosmosdb)| A sample VueJS Single Page Application on a Static Web App, which queries CosmosDB data through a GraphQL endpoint hosted on an Azure Function  |Azure Cosmos DB, Azure Functions, Azure Front Door |

## Contributing

- Identify a sample app you plan to make into an app template
- Follow the steps listed here to make the template azd compatible: [Make your project compatible with Azure Developer CLI](https://learn.microsoft.com/azure/developer/azure-developer-cli/make-azd-compatible?pivots=azd-create)
- Add .devcontainer, .github and .github/workflow components

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Data Collection
The software may collect information about you and your use of the software and send it to Microsoft. Microsoft may use this information to provide services and improve our products and services. You may turn off the telemetry as described in the repository. There are also some features in the software that may enable you and Microsoft to collect data from users of your applications. If you use these features, you must comply with applicable law, including providing appropriate notices to users of your applications together with a copy of Microsoft's privacy statement. Our privacy statement is located at https://go.microsoft.com/fwlink/?LinkId=521839. You can learn more about data collection and use in the help documentation and our privacy statement. Your use of the software operates as your consent to these practices.

## Telemetry Configuration
Telemetry collection is on by default.

To opt-out, set the variable enableTelemetry to false in Bicep/ARM file and disable_terraform_partner_id to false on Terraform files.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
