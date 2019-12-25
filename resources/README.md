# Frequent questions - need to memorize

This section contains random important topics for easier access.

## Mindmaps

During learning I used mindmaps to help memorizing visual content. Mindmaps use XMind software and are shared here_

- [Networking Overview](https://www.xmind.net/m/UkvfGf/)

<iframe src='https://www.xmind.net/embed/UkvfGf/' width='750' height='540' frameborder='0' scrolling='no' allowfullscreen="true"></iframe>

## Differences between Availability Set and Availability Zone

|||
|--- |--- |
|**Availability Set**|**Availability Zone**|
|Protect from Hardware failures within data centers|Protect from entire data center failure|
|SLA 99.95 %|SLA 99.99%|

### Availability Set

- No additional cost
- Same data center
- At least 2 VMs in set

![Availability Set](https://cdn.shortpixel.ai/client/q_glossy,ret_img,w_690/https://cloudopszone.com/wp-content/uploads/2018/08/AvailabilitySet.png)

### Availability Zone

- 3 per region (not all regions supported)
- Separate power source, network and cooling

![Availability Zone](https://cdn.shortpixel.ai/client/q_glossy,ret_img,w_690/https://cloudopszone.com/wp-content/uploads/2018/08/AvailabilityZone.png)

## Characteristics of different redundancy options

![Redundancy Options](https://github.com/Piotr1215/azure-architect-exams-resources/blob/master/RedundancyOptionsDiagram.png?raw=true)

### Redundancy Options Scenarios

|Scenario|LRS|ZRS|GRS/RA-GRS|GZRS/RA-GZRS (preview)|
|--- |--- |--- |--- |--- |
|Node unavailability within a data center|Yes|Yes|Yes|Yes|
|An entire data center (zonal or non-zonal) becomes unavailable|No|Yes|Yes|Yes|
|A region-wide outage|No|No|Yes|Yes|
|Read access to your data (in a remote, geo-replicated region) in the event of region-wide unavailability|No|No|Yes (with RA-GRS)|Yes (with RA-GZRS)|
|Designed to provide __ durability of objects over a given year|at least 99.999999999% (11 9's)|at least 99.9999999999% (12 9's)|at least 99.99999999999999% (16 9's)|at least 99.99999999999999% (16 9's)|
|Supported storage account types|GPv2, GPv1, Blob|GPv2|GPv2, GPv1, Blob|GPv2|
|Availability SLA for read requests|At least 99.9% (99% for cool access tier)|At least 99.9% (99% for cool access tier)|At least 99.9% (99% for cool access tier) for GRSAt least 99.99% (99.9% for cool access tier) for RA-GRS|At least 99.9% (99% for cool access tier) for GZRSAt least 99.99% (99.9% for cool access tier) for RA-GZRS|
|Availability SLA for write requests|At least 99.9% (99% for cool access tier)|At least 99.9% (99% for cool access tier)|At least 99.9% (99% for cool access tier)|At least 99.9% (99% for cool access tier)|

### Redundancy Options Simple

|||
|--- |--- |
|locally redundant storage|Designed to provide at least 99.999999999% (11 9’s) durability of objects over a given year by keeping multiple copies of your data in one data centre.|
|zone redundant storage|Designed to provide at least 99.9999999999% (12 9’s) durability of objects over a given year by keeping multiple copies of your data across multiple data centres or across regions.|
|geographically redundant storage|Designed to provide at least 99.99999999999999% (16 9’s) durability of objects over a given year by keeping multiple copies of the data in one region, and asynchronously replicating to a second region.|
|read-access geographically redundant storage|Designed for to provide at least 99.99999999999999% (16 9’s) durability of objects over a given year and 99.99% read availability by allowing read access from the second region used for GRS.|

## How to choose compute option

![Compute Options Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/images/compute-decision-tree.svg)

## Differences between load balancers

|Service|Global/regional|Recommended traffic|
|--- |--- |--- |
|Azure Front Door|Global|HTTP(S)|
|Traffic Manager|Global|non-HTTP(S)|
|Application Gateway|Regional|HTTP(S)|
|Azure Load Balancer|Regional|non-HTTP(S)|

![Load Balancers Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/images/load-balancing-decision-tree.png)

## Understand SKUs for App Service Plans

![App Service Plans SKUs](https://github.com/Piotr1215/azure-architect-exams-resources/blob/master/App-Plan-SKU.png?raw=true)
