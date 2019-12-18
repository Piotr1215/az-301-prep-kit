# Design a business continuity strategy (15-20%)

## Design a site recovery strategy

![Azure Site Recovery](https://azurecomcdn.azureedge.net/cvt-e39d2318588fa389b7221a303fe6d12be1bd24c86e1600ad32ae68cddc73c67e/images/page/services/site-recovery/asr-architecture.png)

- [Azure Site Recovery](https://azure.microsoft.com/en-gb/services/site-recovery/)

- [x] __design a recovery solution__

  - Plan and be ready to deploy to another region without using the resources until needed
    - Create Recovery Services Vault

  - Recovery can be done between Azure regions or on-prem data center and Azure region

- [x] __design a site recovery replication policy__
- [x] __design for site recovery capacity__
- [x] __design for storage replication__
- [x] __design site failover and failback__
- [x] __design the site recovery network__
- [x] __recommend recovery objectives (Azure, on-prem, hybrid, Recovery Time Objective (RTO), Recovery Level Objective (RLO), Recovery Point Objective (RPO))__
- [x] __identify resources that require site recovery__
- [x] __identify supported and unsupported workloads__
- [x] __recommend a geographical distribution strategy__

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
- [x] __design for autoscaling__
- [x] __design for data center and fault domain redundancy__
- [x] __design for network redundancy__
- [x] __identify resources that require high availability__
- [x] __identify storage types for high availability__
- [x] __design a disaster recovery strategy for individual workloads__
- [x] __design failover/failback scenarios__
- [x] __document recovery requirements__
- [x] __identify resources that require backup__
- [x] __recommend a geographic availability strategy__

## Design a data archiving strategy

- [x] __recommend storage types and methodology for data archiving__
- [x] __identify business compliance requirements for data archiving__
- [x] __identify requirements for data archiving__
- [x] __identify SLA(s) for data archiving__
