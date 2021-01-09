# Design an infrastructure strategy (15-20%)

## Design a storage strategy

- Choose managed storage over unmanaged storage

- Know differences between Premium and Standard storage (disks)

- Different storage access tiers: premium, hot (standard), cool, archive

- [x] __design a storage provisioning strategy__

  - Go through Azure portal, create storage account and see what options are available during the account creation

  - Storage (as most resources in Azure) can be alos provisioned via ARM templates, calling directly RESTful API or using 3rd party tools like Terraform or Pulumi

- [x] __design storage access strategy__

  - [Plularsight - Storage tiers](https://app.pluralsight.com/player?course=microsoft-azure-storage-strategy-design&author=john-savill&name=ac3201c8-3638-4ee1-9880-d04d7c95d041&clip=6&mode=live)

  - [Azure Blob storage: hot, cool, and archive access tiers](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers)

- [x] __identify storage requirements__

  - Capacity
    - US & EU: 2 PB
    - UK & other: 500 TB

  - Thruput: 20k RW/s (read and writes per second)

  - Networking speed (inbound)
    - US: 20 Gbps local storage, 10 Gbps global storage
    - Other: 10 Gbps local storage, 5 Gbps global storage

  - Networking speed (outbound) V1
    - US: 30 Gbps local storage, 20 Gbps global storage
    - Other: 15 Gbps local storage, 10 Gbps global storage

  - Networking speed (outbound) V2
    - all: global and local 50 Gbps

  - Limits
    - 250 storage accounts per subscription per region

- [x] __recommend a storage solution__

  - Storage account
    - Standard: Uses HDD, cheapest, charge by usage, supports cool and hot tiers
    - Premium: SSD, low latency, supports only hot tier

  - Unmanaged disks

  - Managed disks
    - High availabiliy: 99.999%
    - Disk types: Ultra SSD, Premium SSD, Standard SSD, Standard HDD

  - High Durability mechanism
    - Local Redundant Storage or Zone Redundant Storage: 3 copies of a file
    - Globally Redundant Storage: 6 copies of a file

- [x] __recommend storage management tools__

  - Azure portal

  - PowerShell via [Cloud Shell](https://azure.microsoft.com/en-us/features/cloud-shell/) or installed as [Powershell Module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-3.2.0) on Windows or Linux (requires [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-6))

  - Use [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/get-started-with-azure-cli?view=azure-cli-latest) with bash/zsh. Use `az intractive` command to get autocompletion and command line help. Azure CLI can be [installed](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest) on Windows (including WSL) and of course Linux

## Design a compute strategy

[Plularsight - Design a Compute Strategy for Microsoft Azure](https://app.pluralsight.com/library/courses/microsoft-azure-compute-strategy-design/table-of-contents)

- [x] __design a compute provisioning strategy__

  - Automate provisioning and de-provisioning of compute resources by using Infrastructure as Code (Terraform or ARM templates)

  - VMs can also have extensions installed as well as using Azre Blueprints and init scripts to install components at startup

- [x] __design a secure compute strategy__

  - There are several tools available for securing compute resources and managing access to them in Azure such as
    - RBAC to manage access and rights
    - Azure Policies
    - Tagging resources for better organization
    - Azure Blueprints
    - Resources locking

- [x] __determine appropriate compute technologies__

  ![Compute Options Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/images/compute-decision-tree.svg)

  - [Overview of Azure compute options](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-overview#azure-compute-options)

- [x] __design an Azure HPC environment__

  - [High Performance Computing (HPC) on Azure](https://docs.microsoft.com/en-gb/azure/architecture/topics/high-performance-computing)

- [x] __identify compute requirements__
- [x] __recommend management tools for compute__

  - Azure portal

  - PowerShell via [Cloud Shell](https://azure.microsoft.com/en-us/features/cloud-shell/) or installed as [Powershell Module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-3.2.0) on Windows or Linux (requires [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-6))

  - Use [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/get-started-with-azure-cli?view=azure-cli-latest) with bash/zsh. Use `az intractive` command to get autocompletion and command line help. Azure CLI can be [installed](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest) on Windows (including WSL) and of course Linux

## Design a networking strategy

If you have previously passed AZ-300 exam, you should be able to easily pass any networking related questions as most of the AZ-300 conntent is about VNEts and VMs.
Separate repo with learning notes preparing for [AZ-300 exam here](https://github.com/Piotr1215/az-300-prep-kit/tree/master/1-infrastructure#implement-and-manage-virtual-networking)

- [x] __design a network provisioning strategy__

  - Go through Azure portal, create VNET, Virtual GateWay or other virtual network components and see what options are available during the creation

  - Virtual networking components (as most resources in Azure) can be alos provisioned via ARM templates, calling directly RESTful API or using 3rd party tools like Terraform or Pulumi

- [x] __design a network security strategy__

  - Use [Network Security Groups](https://azure.microsoft.com/en-us/blog/network-security-groups/) and create Inbound and Outbound traffic rules to govern traffic from and into your VNET

  - Use [Appication Security Group](https://azure.microsoft.com/en-us/blog/applicationsecuritygroups/) to create and manage network security on an application level

  - Limit access to resources by placing them on VNEt and useing [Virtual Network service endpoints](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-service-endpoints-overview) to allow access only from predefined Azure services

  - Change Azure default routing rules by creating [Route Table](https://docs.microsoft.com/en-us/azure/virtual-network/manage-route-table)

- [x] __determine appropriate network connectivity technologies__

Iterating throught options, details are in the AZ-300 repo.

- Virtual network peering
- VPN (site-to-site, point-to-site)
- Application Gateway
- ExpressRoute

- [x] __identify networking requirements__
- [x] __recommend network management tools__

  - Azure portal
    - Use [Network Watcher](https://docs.microsoft.com/en-us/azure/network-watcher/network-watcher-diagnose-on-premises-connectivity) to visualize VNets and connectivity between them. Network Watcher can also be used to troubleshoot networking issues

  - PowerShell via [Cloud Shell](https://azure.microsoft.com/en-us/features/cloud-shell/) or installed as [Powershell Module](https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-3.2.0) on Windows or Linux (requires [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-6))

  - Use [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/get-started-with-azure-cli?view=azure-cli-latest) with bash/zsh. Use `az intractive` command to get autocompletion and command line help. Azure CLI can be [installed](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest) on Windows (including WSL) and of course Linux

- [x] __recommend network security solutions__

  - Reuse network security groups

  - Follow Principle of least priviledge

  - Use [Application Gateway](https://docs.microsoft.com/en-us/azure/application-gateway/overview) with [WAF](https://docs.microsoft.com/en-us/azure/web-application-firewall/overview)

  - Follow [Zero Trust Network Security Architecture Guidelines](https://doubleoctopus.com/security-wiki/network-architecture/zero-trust/)

  - Take adventage of [Just-in-Time VM Access](https://azure.microsoft.com/en-us/blog/just-in-time-vm-access-is-generally-available/) to open SSH and RDP ports only when needed

## Design a monitoring strategy for infrastructure

- [x] __design for alert notifications__
- [x] __design an alert and metrics strategy__
