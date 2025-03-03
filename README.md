# module-1-vnet-1-public-subnet-2-private-subnets/azurerm

## Description
Terraform module for Vnet deployment on Microsoft Azure

## Deployment
This module creates a topology with a single virtual network having a single public facing subnet and two private subnets.

## Usage
```tf
module "vnet" {
    source = "git::https://github.com/armdupre/terraform-azurerm-module-1-vnet-1-public-subnet-2-private-subnets.git"
    PublicSecurityRuleSourceIpPrefixes = [ "1.1.1.1/32" ]
    ResourceGroupName = azurerm_resource_group.ResourceGroup.name
}

resource "azurerm_resource_group" "ResourceGroup" {
    location = "East US"
    name = "azure-1-vnet-1-public-subnet-2-private-subnets"
}
```
