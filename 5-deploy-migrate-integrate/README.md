# Design for deployment, migration, and integration (10-15%)

## Design deployments

[Plularsight - Designing Deployments in Microsoft Azure](https://app.pluralsight.com/player?course=microsoft-azure-deployments-designing&author=greg-shields&name=6cfd39d2-986b-4c5e-bb64-3abc65ae6135&clip=0)

- [x] __design a compute deployment strategy__

  - CI/CD pipelines with AzureDevOps
  - GitHub Actions
  - Chef/Puppet

- [x] __design a container deployment strategy__

  - [Azure container registry](https://azure.microsoft.com/en-us/services/container-registry/)

- [x] __design a data platform deployment strategy__

  - Deploy SQL schema using DACPAC files

- [x] __design a messaging solution deployment strategy__

  - Deploy Kafka/RabbitMQ as bundles from Marketplace

- [x] __design a storage deployment strategy__

  - Use AzCopy or Azure Pipeline copy task to copy files to storage

  - Copy files over SSH into VMs (can be also task in Azure Pipeline)

- [x] __design a web app and service deployment strategy__

  - Automated deployment step in Azure Pipeline

  - Manually deploy using Kudu (zipped binaries)

  - GitHub Actions

## Design migrations

- [Plularsight - Designing Migrations in Microsoft Azure](https://app.pluralsight.com/player?course=microsoft-azure-migrations-designing&author=greg-shields&name=f8c92b4d-e41e-4f07-a90b-d472e8efcea1&clip=0)

- Visit [Azure migration center](https://azure.microsoft.com/en-ca/migration/) for more details about migrations

- You can also use [Azure Site Recovery](https://docs.microsoft.com/en-us/azure/site-recovery/site-recovery-overview) to support migration plans

- [x] __recommend a migration strategy__

  - Migrating workloads with and without downtime

  - Lift&Shift vs rearchitect to migrate

- [x] __design data import/export strategies during migration__

  - Use [Azure Import/Export service](https://docs.microsoft.com/en-us/azure/storage/common/storage-import-export-service)

- [x] __determine the appropriate application migration method__

  - Rehost (lift&shift), refactor (small changes), rearchitect (larger changes), rebuild from scratch

- [x] __determine the appropriate data transfer method__

  - AzCopy

  - Database Migration Service (not only for SQL Server)

  - Data Box (phisical data mediium transfer)

  - Azure Import/Export service

- [x] __determine the appropriate network connectivity method__

  - VPN connections or ExpressRoute

- [x] __determine migration scope, including redundant, related, trivial, and outdated data__
- [x] __determine application and data compatibility__

## Design an API integration strategy

- [x] __design an API gateway strategy__

  - API Management

- [x] __determine policies for internal and external consumption of APIs__

  - Different types of policies to manage usage of exposed APIs

- [x] __recommend a hosting structure for API management__

  - How to combine APIs into products and expose them to developers through API portals