# Design a business continuity strategy (15-20%)

## Design a site recovery strategy

![Azure Site Recovery](https://azurecomcdn.azureedge.net/cvt-e39d2318588fa389b7221a303fe6d12be1bd24c86e1600ad32ae68cddc73c67e/images/page/services/site-recovery/asr-architecture.png)

- [Azure Site Recovery](https://azure.microsoft.com/en-gb/services/site-recovery/)

- [x] __design a recovery solution__

  - Plan and be ready to deploy to another region without using the resources until needed
    - Create [Recovery Services Vault](https://docs.microsoft.com/en-us/azure/backup/backup-create-rs-vault)

  - Recovery can be done between Azure regions or on-prem data center and Azure region

- [x] __design a site recovery replication policy__

  - [Configure and manage replication policies for VMware disaster recovery](https://docs.microsoft.com/en-us/azure/site-recovery/vmware-azure-set-up-replication)

- [x] __design for site recovery capacity__

  - [Azure Site Recovery capacity-planning guide for migrations](https://docs.microsoft.com/en-us/azure/cloud-solution-provider/migration/on-premises-to-azure-csp/asr-capacity-planning)

- [x] __design for storage replication__

  - [Lynda Video - https://www.lynda.com/Azure-tutorials/Implement-Azure-Storage-replication/797734/5032317-4.html](https://www.lynda.com/Azure-tutorials/Implement-Azure-Storage-replication/797734/5032317-4.html)

- [x] __design site failover and failback__

  - [Fail over and fail back physical servers replicated to Azure](https://docs.microsoft.com/en-us/azure/site-recovery/physical-to-azure-failover-failback)

- [x] __design the site recovery network__

  - [About networking in Azure VM disaster recovery](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-about-networking)

- [x] __recommend recovery objectives (Azure, on-prem, hybrid, Recovery Time Objective (RTO), Recovery Level Objective (RLO), Recovery Point Objective (RPO))__

  - **RPO** stands for recovery POINT objective, i.e., how much data is one potentially prepared and willing to lose, worse case
  - **RTO** stands for recovery TIME objective, i.e., if/when the ‘bad thing’ happens, how much time does it take to be back up and running again
  - **RLO** stands for Recovery Level Objective (business continuity management) - defines a level to which software should be restored to

- [x] __identify resources that require site recovery__
- [x] __identify supported and unsupported workloads__

  - [Support matrix for Azure VM disaster recovery between Azure regions](https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-support-matrix)
- [x] __recommend a geographical distribution strategy__

  - [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/en-us/azure/best-practices-availability-paired-regions)

    - Azure does not deploy/upgrage to both paired regions simultaniously

## Design for high availability

|% Uptime|Downtime per week|Downtime per month|Downtime per year|
|--- |--- |--- |--- |
|99%|1.68 hours|7.2 hours|3.65 days|
|99.9%|10 minutes|43.2 minutes|8.76 hours|
|99.95%|5 minutes|21.6 minutes|4.38 hours|
|99.99%|1 minute|4.32 minutes|52.56 minutes|
|99.999%|6 seconds|26 seconds|5.26 minutes|

![Load Balancing Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/images/load-balancing-decision-tree.png)

- [x] __design for application redundancy__

  - Follow architectural principle of [making "all things" redundant](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/redundancy)

  - [Architecting Azure applications for resiliency and availability](https://docs.microsoft.com/en-us/azure/architecture/reliability/architect)

- [x] __design for autoscaling__

  - [Plularsight - Autoscaling](https://www.pluralsight.com/courses/microsoft-azure-autoscaling-developing)

  - [Autoscaling best practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/auto-scaling)

  - [Design to scale out](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/scale-out)

- [x] __design for data center and fault domain redundancy__

  - [Lynda Video - design for data center and fault domain redundancy](https://www.lynda.com/Azure-tutorials/Design-data-center-fault-domain-redundancy/2822056/2267274-4.html)
- [x] __design for network redundancy__

  - [Lynda Video - Network Redundancy](https://www.lynda.com/Azure-tutorials/Network-redundancy-high-availability/2822056/2267275-4.html)

  - [Highly Available Cross-Premises and VNet-to-VNet Connectivity](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-highlyavailable)

- [x] __identify resources that require high availability__
- [x] __identify storage types for high availability__
- [x] __design a disaster recovery strategy for individual workloads__

  - [About disaster recovery for on-premises apps](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-workload)

  - [Set up disaster recovery for SQL Server](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-sql)

- [x] __design failover/failback scenarios__

  - [Lynda Video - design failover/failback scenarios](https://www.lynda.com/Azure-tutorials/Design-failback/2822056/2267272-4.html)

- [x] __document recovery requirements__
- [x] __identify resources that require backup__
- [x] __recommend a geographic availability strategy__

## Design a data archiving strategy

- [x] __recommend storage types and methodology for data archiving__

  - [Lynda Video - recommend storage types and methodology for data archiving](https://www.lynda.com/Azure-tutorials/Storage-types-methodology-data-archiving/2822056/2267278-4.html)

  - Only standard blob or file storage supports archive tier

    - Hot access 99.9% availability

    - Cool: Must keep data at least 30 days, 99% availability

    - Archive: High retrieval cost, must keep 180 days at least, data must be rehydrated to be retrieved (might take several hours)

    - Archive tier can be changed after creating the storage account

- [x] __identify business compliance requirements for data archiving__
- [x] __identify requirements for data archiving__
- [x] __identify SLA(s) for data archiving__
