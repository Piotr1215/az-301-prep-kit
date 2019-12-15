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

  - [Overview of the security pillar](https://docs.microsoft.com/en-gb/azure/architecture/framework/security/overview)

  - [Lab - Design for security in Azure](https://docs.microsoft.com/en-us/learn/modules/design-for-security-in-azure/)

- [x] __identify sizing requirements__

  - [Use Azure Monitor to check resources utilization and decide on sizing](https://docs.microsoft.com/en-us/azure/architecture/best-practices/monitoring)

  - [Lab - Predict costs and optimize spending for Azure](https://docs.microsoft.com/en-us/learn/modules/predict-costs-and-optimize-spending/)

  - [Use Azure Advisor to get costs recommendations](https://docs.microsoft.com/en-gb/azure/advisor/?WT.mc_id=AzPortal_Advisor_CmdBar_DocLink)

  - [Use autoscaling to avoid overprovisioning](https://docs.microsoft.com/en-us/azure/architecture/best-practices/auto-scaling)

- [x] __recommend changes during project execution__

  - understand different software design modes: waterfall, agile, devops

  - intustry standards: TOGAF, ITIL

  - [Use Azure DevOps to manage projects and create CI/CD pipelines](https://azure.microsoft.com/en-us/services/devops/?nav=min)

- [x] __evaluate products and services to align with solution__

  - [Azure Marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/)

- [x] __create testing scenarios__

  - [Azure DevOps Create test plans and test suites](https://docs.microsoft.com/en-us/azure/devops/test/create-a-test-plan?view=azure-devops)

  - [Setup playground environment for developers using DevTest Labs](https://azure.microsoft.com/en-us/services/devtest-lab/)

## Optimize consumption strategy

- [Azure billing and cost management documentation](https://docs.microsoft.com/en-us/azure/billing/)

- Create and manage [Azure budgets](https://docs.microsoft.com/en-us/azure/cost-management/tutorial-acm-create-budgets?toc=/azure/billing/TOC.json) to help avoid costs creep up

- Use [Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) to estimate costs

- Reduce service costs using [Azure Advisor](https://docs.microsoft.com/en-us/azure/advisor/advisor-cost-recommendations), you can even [act on the advisor recommendations](https://docs.microsoft.com/en-us/azure/cost-management/tutorial-acm-opt-recommendations?toc=/azure/billing/TOC.json) from the portal

- [Optimizing Azure Costs: Compute, Network, Storage, Identity, and App Services - Azure Training](https://www.youtube.com/watch?v=paOh4RMpd7I)

- [Azure Cost Management technical overview](https://www.youtube.com/watch?v=b26fSQyGFlU)

- Use Azure Policy/Initiative to enforce [adding billing code tags to resources](https://docs.microsoft.com/en-us/azure/governance/policy/samples/billing-tags-policy-initiative) to easier identify resources cost centers

- [x] __optimize app service costs__

  - [Choose appropriate app service plan pricing](https://azure.microsoft.com/en-us/pricing/details/app-service/windows/)

- [x] __optimize compute costs__

  - [Use Azure Reservations to optimize VM costs](https://docs.microsoft.com/en-us/azure/billing/billing-save-compute-costs-reservations)

  - [Preview: Azure Spot VMs for virtual machine scale sets](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/use-spot) - this feature is in preview so it will not be on the exam.

- [x] __optimize identity costs__

  - [Azure active directory editions](https://azure.microsoft.com/en-us/pricing/details/active-directory/) (Free, Basic, Premium P1, Premium P2)

- [x] __optimize network costs__

  - Pay for outbound data, starting from 5GB/month

  - Incomming data traffic is free

- [x] __optimize storage costs__

  - Deleta VHDs if not needed, after deleting VM

  - Storage is billed per GB/month

  - Use [elastic pools](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-elastic-pool) for SQL Databases

  - Use different [storage tiers](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers) (hot, cool, archive) for storage accounts

## Design an auditing and monitoring strategy

- [x] __define logical groupings (tags) for resources to be monitored__
- [x] __determine levels and storage locations for logs__
- [x] __plan for integration with monitoring tools__
- [x] __recommend appropriate monitoring tool(s) for a solution__
- [x] __specify mechanism for event routing and escalation__
- [x] __design auditing for compliance requirements__
- [x] __design auditing policies and traceability requirements__