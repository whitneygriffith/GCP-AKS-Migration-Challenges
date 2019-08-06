# Introduction

Perhaps this is a place where we can talk about our project.

I've added user stories (primitive ones) here.

# Next Steps

It might make sense to find tutorials for these user stories and think of ways where small teams can work together to deliver code for each user story.

If any of us have time we can find tutorials for each of these and simply add them inline so everybody can see everything.

- As a cluster admin, I want to provision the cluster, from script or Terraform so that we can implement Infrastructure as code.
    1. https://docs.microsoft.com/en-us/azure/terraform/terraform-create-k8s-cluster-with-tf-and-aks

- As a developer I would like to deploy Spring Boot Java Containers to K8s so that I can support a microservice app.

- As a developer I need to provision and get connectivituy to Postgres/Redis so that the microservices have persistent storage.

- As a infrastructure engineer I need to figure out how to map AWS-specific technologies to Azure so that we have a platform to host our microservice apps.

- As a cluster admin I want to use Terraform to provision my infrastructure so we can have a single platform for provisioning infrastructure.
    1. https://docs.microsoft.com/en-us/azure/terraform/terraform-create-k8s-cluster-with-tf-and-aks - Same as above

- As a network administrator, I would like to migrate any VPCs to Azure VPNs so the proper routing rules, policies, security, addressing, subnetting works properly.
    1. ARM Template Samples - https://docs.microsoft.com/en-us/azure/virtual-network/template-samples
    1. Routing Tutorial - https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-create-route-table-portal
    1. Azure Network Policy Samples - https://docs.microsoft.com/en-us/azure/virtual-network/policy-samples