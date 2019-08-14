# Kubernetes on Azure Notes

Links:

- [Azure Kubernetes Service \(AKS\)](https://docs.microsoft.com/en-us/azure/aks/)
- [AKS workshop](https://aksworkshop.io/)


# Part I

## Challenge 1 

Deploy a 3 node AKS cluster running Kubernetes version 1.14.5. Select the WestUS 2 region.

## Challenge 2 

Set up Helm and Tiller inside the cluster. [Helm on AKS](https://docs.microsoft.com/en-us/azure/aks/kubernetes-helm)

## Challenge 3

Deploy nginx chart using helm and go to the external IP.


Delete resource group.

# Part II

## Challenge 1

- Deploy a /16 Virtual Network inside a resource group in WestUS 2.
- Create a /24 subnet within the VNet
- Deploy a 3 node AKS cluster running Kubernetes version 1.13.8 within the subnet created above.

[Azure CNI for AKS](https://docs.microsoft.com/en-us/azure/aks/configure-azure-cni)

## Challenge 2

- Create an [Azure Container Registry](https://docs.microsoft.com/en-us/azure/container-registry/container-registry-get-started-azure-cli) with the "Standard" sku in the same resource group as your AKS cluster. 
- Authenticate your AKS cluster in order to pull images from your ACR.
- Push your images to ACR.
- Deploy Application using Helm and images from ACR. 

## Challenge 3

- Implement AAD cluster and other security best practices