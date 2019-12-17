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
- [x] __design an encryption strategy for data at rest__
- [x] __design an encryption strategy for data in transmission__
- [x] __design an encryption strategy for data in use__
- [x] __design a scalability strategy for data__
- [x] __design secure access to data__
- [x] __design a data loss prevention (DLP) policy__

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
