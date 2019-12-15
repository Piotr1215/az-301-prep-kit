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
- [x] __choose between relational and non-relational databases__
- [x] __design a data auditing strategy__
- [x] __design a data caching strategy__
- [x] __identify data attributes__
- [x] __recommend database service tier sizing__
- [x] __design a data retention policy__
- [x] __design for data availability__
- [x] __design for data consistency__
- [x] __design for data durability__
- [x] __design a data warehouse strategy__

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
