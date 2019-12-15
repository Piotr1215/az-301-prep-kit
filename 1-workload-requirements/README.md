# Determine workload requirements (10-15%)

## Gather information and requirements

- [x] __identify compliance requirements__

  - [What do the law, authorities, and regulators require?](https://docs.microsoft.com/en-us/azure/architecture/framework/security/law-authority)

  - [Microsoft compliance offerings](https://docs.microsoft.com/en-gb/microsoft-365/compliance/offering-home)

  - [Azure Storage compliance offerings](https://docs.microsoft.com/en-us/azure/storage/common/storage-compliance-offerings)

  - [Audit reports for various Azure services](https://servicetrust.microsoft.com/)

  - [Regulatory compliance dashboard in Azure Security Center](https://azure.microsoft.com/en-us/blog/regulatory-compliance-dashboard-in-azure-security-center-now-available/)

  - [Apply Azure policies to enforce compliance](https://azure.microsoft.com/en-us/services/azure-policy/)

  - [Audit and enforce policy compliance](https://docs.microsoft.com/en-us/azure/architecture/framework/security/governance#audit-and-enforce-policy-compliance)

- [x] __identify identity and access management infrastructure__

  - [Identity and access management](https://docs.microsoft.com/en-us/azure/architecture/framework/security/identity)

  - [Self Paced Lab - Identity management](https://docs.microsoft.com/en-gb/learn/modules/design-for-security-in-azure/3-identity-management)

- [x] __identify service-oriented architectures__

  - [Plularsight - Service Oriented Architectures](https://app.pluralsight.com/course-player?course=microsoft-azure-enterprise-architecture-information-gathering&author=chris-behrens&name=87dac155-b66f-4af5-b489-63b8eacb94f3&clip=0&mode=live)

- [x] __identify accessibility requirements__

  - [Plularsight - Accessibility Requirements](https://app.pluralsight.com/course-player?clipId=40fe86cf-f9c1-4ace-87e7-863f1bc54d4b)

- [x] __identify availability requirements__

  - [Availability patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/category/availability)

  - [Plularsigh - Availability Requirements](https://app.pluralsight.com/course-player?clipId=cdd824ec-8533-4701-802b-5e0375de83ac)

  - [Architecture for Availability](https://docs.microsoft.com/en-us/azure/architecture/guide/pillars#availability)

  - [Make all things redundant](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/redundancy)

|% Uptime|Downtime per week|Downtime per month|Downtime per year|
|--- |--- |--- |--- |
|99%|1.68 hours|7.2 hours|3.65 days|
|99.9%|10 minutes|43.2 minutes|8.76 hours|
|99.95%|5 minutes|21.6 minutes|4.38 hours|
|99.99%|1 minute|4.32 minutes|52.56 minutes|
|99.999%|6 seconds|26 seconds|5.26 minutes|

![Load Balancing Decision Tree](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/images/load-balancing-decision-tree.png)

- [x] __identify capacity planning and scalability requirements__

  - [Plularsight - Capacity Planning and Scalability Requirements](https://app.pluralsight.com/course-player?clipId=5a12417b-35db-450e-8b6b-5f797df22679)

- [x] __identify deploy-ability requirements__

  - [Pluralsight - Deployability Requirements](https://app.pluralsight.com/course-player?clipId=c028929c-bbe2-46ed-8f04-8b2a5574c2af)

- [x] __identify configurability__

  - [Configure an App Service app in the Azure portal](https://docs.microsoft.com/en-us/azure/app-service/configure-common)

  - [What is Azure App Configuration?](https://docs.microsoft.com/en-us/azure/azure-app-configuration/overview)

- [x] __identify governance requirements__

  - [Plularsight - Governance Requirements](https://app.pluralsight.com/course-player?clipId=a12acd37-4df1-4f2a-a66c-f598ded13841)

- [x] __identify maintainability requirements__

  - [Plularsight - Maintainability Requirements](https://app.pluralsight.com/course-player?clipId=400d6f60-2141-423c-b37a-605814b4c1f8)

- [x] __identify security requirements__

  - [Plularsight - Security Requirements](https://app.pluralsight.com/course-player?clipId=5a12417b-35db-450e-8b6b-5f797df22679)

- [x] __identify sizing requirements__
- [x] __recommend changes during project execution__
- [x] __evaluate products and services to align with solution__
- [x] __create testing scenarios__

## Optimize consumption strategy

- [x] __optimize app service costs__
- [x] __optimize compute costs__
- [x] __optimize identity costs__
- [x] __optimize network costs__
- [x] __optimize storage costs__

## Design an auditing and monitoring strategy

- [x] __define logical groupings (tags) for resources to be monitored__
- [x] __determine levels and storage locations for logs__
- [x] __plan for integration with monitoring tools__
- [x] __recommend appropriate monitoring tool(s) for a solution__
- [x] __specify mechanism for event routing and escalation__
- [x] __design auditing for compliance requirements__
- [x] __design auditing policies and traceability requirements__