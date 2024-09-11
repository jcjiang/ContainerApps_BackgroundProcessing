# Building a Background Processing Application with Azure Container Apps

## Introduction

You can use Azure Container Apps to deploy applications without requiring the exposure of public endpoints. The application can scale out and in by using scaling rules based on the Azure Storage queue length. When there are no messages on the queue, the container app scales in to zero.

This repository contains reference code for [this tutorial](https://learn.microsoft.com/en-us/azure/container-apps/background-processing?tabs=azure-powershell). 

Specifically, you will learn how to:

- Create a Container Apps environment to deploy your container apps
- Create an Azure Storage Queue to send messages to the container app
- Authenticate using Managed Identity
- Deploy your background processing application as a container app
- Verify that the queue messages are processed by the container app

## Repository Overview

The majority of this tutorial is in the form of CLI commands, which can be found in the original documentation. 

This repository contains a file named `queue.json`, which contains the configuration code for deploying this project to Azure with support for managed identity.

## Conclusion

You have successfully built and deployed a background processing application using Azure Container Apps. You can now scale your application and manage background tasks efficiently.

## Common Errors

- If your subscription cannot be found when creating a new storage account using the command `$StorageAcct = New-AzStorageAccount @StorageAcctArgs`, the `Microsoft.Storage` resource provider might not have been registered for your subscription. To do so, follow the instructions [here](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/resource-providers-and-types).

## Resources

- [Azure Container Apps Documentation](https://docs.microsoft.com/en-us/azure/container-apps/)
- [Docker Documentation](https://docs.docker.com/)
- [Azure Storage Queues Documentation](https://docs.microsoft.com/en-us/azure/storage/queues/)

## Feedback

If you have any feedback or questions, please reach out via [GitHub Issues](https://github.com/your-repo/issues).
