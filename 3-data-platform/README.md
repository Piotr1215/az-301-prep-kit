# Design a data platform solution (15-20%)

|Storage account type|Supported services|Supported performance tiers|Supported access tiers|Replication options|Deployment model1|Encryption2|
|--- |--- |--- |--- |--- |--- |--- |
|General-purpose V2|Blob, File, Queue, Table, Disk, and Data Lake Gen26|Standard, Premium5|Hot, Cool, Archive3|LRS, GRS, RA-GRS, ZRS, GZRS (preview), RA-GZRS (preview)4|Resource Manager|Encrypted|
|General-purpose V1|Blob, File, Queue, Table, and Disk|Standard, Premium5|N/A|LRS, GRS, RA-GRS|Resource Manager, Classic|Encrypted|
|BlockBlobStorage|Blob (block blobs and append blobs only)|Premium|N/A|LRS, ZRS4|Resource Manager|Encrypted|
|FileStorage|File only|Premium|N/A|LRS, ZRS4|Resource Manager|Encrypted|
|BlobStorage|Blob (block blobs and append blobs only)|Standard|Hot, Cool, Archive3|LRS, GRS, RA-GRS|Resource Manager|Encrypted|

## Design a data management strategy

- [x] __choose between managed and unmanaged data store__

  - Unmanaged Data Stores (choose when need high performance tuning or hight degree of control over hosting environment and offering)
    - Table Storage
    - Blob Storage
    - SQL Server in VM
    - Orable DB in VM

  - Managed Data Stores (highly available, auto-scaling, threat detection, auto tuning)
    - VM Data Disk
    - Azure SQL Database
    - Cosmos DB
    - Azure Database for MySQL, PostgreSQL, MariaDB
    - Managed SQL Server
    - Redis Cache

- [x] __choose between relational and non-relational databases__

  - [Criteria for choosing a data store](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-comparison)

  - [Lab - classify your data](https://docs.microsoft.com/en-gb/learn/modules/choose-storage-approach-in-azure/2-classify-data)

  - Choose relational database for strong consistency and integrity

  - Choose non-relational database for scalability and flexibility

- [x] __design a data auditing strategy__

  - Take advendate of [SQL audit log](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-auditing)

  - Use [Azure Monitor Logs](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-platform-logs) to connect to SQL Databases and other data sources

  - With [Azure Monitor workbooks](https://docs.microsoft.com/en-us/azure/azure-monitor/app/usage-workbooks) you can create interactive reports including data auditing

- [x] __design a data caching strategy__

  - [Architect Caching strategy](https://docs.microsoft.com/en-us/azure/architecture/best-practices/caching)

  - [Plularsight - Data Caching](https://app.pluralsight.com/course-player?clipId=7c9c1b83-daa5-4070-824a-374b9397a8bd)

- [x] __identify data attributes__

  - [Plularsight - understanding data attributes](https://app.pluralsight.com/course-player?clipId=2f803566-67fd-421d-8298-61dee5002e0b)

- [x] __recommend database service tier sizing__

  - Understand [DTU-based pricing model - DTU](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-service-tiers-dtu)

  - Understand [Reuqest Units pricing model - RU/s](https://docs.microsoft.com/en-us/azure/cosmos-db/request-units)

- [x] __design a data retention policy__

  - Regular retention up to 35 days

  - Long Term Retention policy up to 10 years

  - [Automated geo-redundant SQL Database backups](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-automated-backups?tabs=single-database)

- [x] __design for data availability__

  - [Plularsight - Data Availability](https://app.pluralsight.com/course-player?clipId=3ca203aa-3254-4dbf-aef2-8247537f83f4)

- [x] __design for data consistency__

  - ![Cosmos DB Consistency Levels](https://docs.microsoft.com/en-us/azure/cosmos-db/media/consistency-levels/five-consistency-levels.png)

  - [How to choose right consistency level for Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/consistency-levels-choosing)

- [x] __design for data durability__

  - [Understand what is RPO and RTO](https://blogs.msdn.microsoft.com/cloud_solution_architect/2018/05/02/understanding-rpo-and-rto-considerations-of-azure-solutions/)

    - **RPO** stands for recovery POINT objective, i.e., how much data is one potentially prepared and willing to lose, worse case
    - **RTO** stands for recovery TIME objective, i.e., if/when the ‘bad thing’ happens, how much time does it take to be back up and running again

- [x] __design a data warehouse strategy__

  - Use when need to do reports and analytics

  - Read only data

  - Use [Azure Analysis Services](https://docs.microsoft.com/en-us/azure/analysis-services/) to combine data from different sources and perform ad hoc analysis

  - [Big Data Architecture](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-data)

## Design a data protection strategy

- [x] __recommend geographic data storage__

||LRS|ZRS|GRS|RA-GRS|
|--- |--- |--- |--- |--- |
|Overview|Replicates data in a single datacenter|Stores copies of data across multiple datacenters|Stores copies in a local datacenter, like LRS, but then stores three more copies in a datacenter in another region|Same as GRS, but offers read access in the secondary datacenter in the other region|
|Data copies|3|3|6|6|
|Use case|Ensures that your data is highly available but, for compliance reasons, must be kept local|A higher durability option for block storage, where data can stay in only one region|Where you need to ensure that your data and systems are always available despite datacenter or region outages|Where your applications (especially those with many read requests) can read data from other regions, but also to ensure that read operations are always available even if the primary region is down|

- [x] __design an encryption strategy for data at rest__

  - [Azure Storage encryption for data at rest](https://docs.microsoft.com/en-us/azure/storage/common/storage-service-encryption)

  - [Azure Data Encryption-at-Rest](https://docs.microsoft.com/en-us/azure/security/fundamentals/encryption-atrest)

  - [TDE - Transparent data encryption for SQL Database and Data Warehouse](https://docs.microsoft.com/en-us/azure/sql-database/transparent-data-encryption-azure-sql?tabs=azure-portal)

- [x] __design an encryption strategy for data in transmission__

  - Force SSL connections to data storage

  - Use VPN (site-to-site or point-to-site) if connecting from outside Azure network

  - [Plularsight - data encryption in transit](https://app.pluralsight.com/course-player?clipId=6b86cafd-8965-4da6-86d5-ef90ad5cb531)

  - [Dynamic data masking for Azure SQL Database and Data Warehouse](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dynamic-data-masking-get-started)

- [x] __design an encryption strategy for data in use__

  - [Plularsight - data encryption in use](https://app.pluralsight.com/course-player?clipId=2c5186ec-3a3a-4bbb-9cf2-72a8a65561e4)

- [x] __design a scalability strategy for data__

  - [Plularsight - data scalability](https://app.pluralsight.com/course-player?clipId=67f63322-31a8-4575-bf1f-1b3f3d966030)

  - [Scaling out with Azure SQL Database](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-elastic-scale-introduction)

- [x] __design secure access to data__

  - Secure access to data on network level using [Virtual Network service endpoints](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-service-endpoints-overview)

  - Whitelist or blacklist IP ranges using [Azure SQL Database and Azure SQL Data Warehouse IP firewall rules](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-firewall-configure)

  - Use [Azure Active Directory](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-aad-authentication-configure?tabs=azure-powershell) to access SQL database

  - [Plularsight - secure data access](https://app.pluralsight.com/course-player?clipId=70fa078c-87dc-4880-b4a6-625617d1e902)

- [x] __design a data loss prevention (DLP) policy__

  - [Plularsight - data loss prevention](https://app.pluralsight.com/course-player?clipId=cfd5c812-961d-4d43-bd29-28603f494132)

## Design and document data flows

- [x] __identify data flow requirements__
- [x] __create a data flow diagram__
- [x] __design a data flow to meet business requirements__
- [x] __design data flow solutions__
- [x] __design a data import and export strategy__

## Design a monitoring strategy for the data platform

- [x] __design for alert notifications__
- [x] __design an alert and metrics strategy__
- [x] __monitor Azure Data Factory pipelines__
