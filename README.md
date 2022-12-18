# Terraform Project: Azure Load Balancer with Availability Set

## Project scenario

We are tasked with provisioning an Azure Load Balancer for the HTTP and HTTPS requests with an availability set as the backend pool. We are also tasked to output subnet IDs and the load balancer's frontend IP. Lastly we will keep the tfstate file in a separate storage account remotely.

## Project Objectives

In this project, we will:

+ Step 1: Provision the required lab environment.
+ Step 2: Provision the load balancer.
+ Step 3: Output subnet IDs and load balancer's frontend IP.
+ Step 4: Configure the tfstate file remote storage.

## Directions

### Step 1: Provision the required lab environment

In this step, we will create:

+ a resource group,
+ a virtual network,
+ two subnets are frontend and backend,
+ a storage account,
+ two virtual machines in an availability set.

### Step 2: Provision the load balancer

In this step, we will create the load balancer. In order to create the load balancer, we will need to create:

+ a frontend public IP,
+ a backend pool (our availability set),
+ a health probe for HTTP,
+ a load balancing rule for HTTP,
+ a health probe for HTTPS,
+ a load balancing rule for HTTPS.

### Step 3: Output subnet IDs and load balancer's frontend IP

For this task, we will create an output file with the content subnet IDs and load balancer's frontend IP.

### Step 4: Configure the tfstate file remote storage

For this step, we will use an already created resource group and an existing storage account with a container.


As last statement I share the sources that is used in the project.

## Source from Terraform 


| Name | Type |
|------|------|
| [azurerm_availability_set.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/availability_set) | script resource |
| [azurerm_lb.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/lb) | script resource |
| [azurerm_lb_backend_address_pool.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/lb_backend_address_pool) | script resource |
| [azurerm_lb_probe.port443](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/lb_probe) | script resource |
| [azurerm_lb_probe.port80](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/lb_probe) | script resource |
| [azurerm_lb_rule.port443](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/lb_rule) | script resource |
| [azurerm_lb_rule.port80](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/lb_rule) | script resource |
| [azurerm_network_interface.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/network_interface) | script resource |
| [azurerm_network_interface_backend_address_pool_association.ba_association](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/network_interface_backend_address_pool_association) | script resource |
| [azurerm_public_ip.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/public_ip) | script resource |
| [azurerm_resource_group.terraform_sample](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/resource_group) | script resource |
| [azurerm_storage_account.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/storage_account) | script resource |
| [azurerm_storage_container.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/storage_container) | script resource |
| [azurerm_subnet.my_subnet_backend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/subnet) | script resource |
| [azurerm_subnet.my_subnet_dmz](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/subnet) | script resource |
| [azurerm_subnet.my_subnet_frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/subnet) | script resource |
| [azurerm_virtual_machine.frontend](https://registry.terraform.io/providers/hashicorp/azurerm/3.0.0/docs/resources/virtual_machine) | script re