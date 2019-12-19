# Design for identity and security (20-25%)

## Design identity management

- [x] __choose an identity management approach__

  - [Identity and access management](https://docs.microsoft.com/en-us/azure/architecture/framework/security/identity)

  - [Azure Identity Management and access control security best practices](https://docs.microsoft.com/en-us/azure/security/fundamentals/identity-management-best-practices)

  - [Deep Dive: The Four Pillars of Identity - Identity Management in the Age of Hybrid IT](https://social.technet.microsoft.com/wiki/contents/articles/15530.the-four-pillars-of-identity-identity-management-in-the-age-of-hybrid-it.aspx)

    - ![Four Pillars](https://social.technet.microsoft.com/wiki/cfs-filesystemfile.ashx/__key/communityserver-wikis-components-files/00-00-00-00-05/4721.fourpillarsofidentity.png)

- [x] __design an identity delegation strategy__

  - [Service-to-service calls that use delegated user identity in the On-Behalf-Of flow](https://docs.microsoft.com/en-us/azure/active-directory/develop/v1-oauth2-on-behalf-of-flow)

  - [UNDERSTANDING AZURE AD’S ON-BEHALF-OF FLOW (AKA OBO FLOW)](https://blogs.aaddevsup.xyz/2019/08/understanding-azure-ads-on-behalf-of-flow-aka-obo-flow/)

- [x] __design an identity repository__

  - TODO: All Link

- [x] __design self-service identity management__

  - requires premium Azure Active Directory account

  - Azure Active Directory -> Password Reset

  - [Quickstart: Configure Azure Active Directory self-service password reset](https://docs.microsoft.com/en-us/azure/active-directory/authentication/quickstart-sspr)

- [x] __design user and persona provisioning__

  - [Automatic user provisioning to AD](https://youtu.be/_ZjARPpI6NI)

- [x] __define personas__

  - TODO: All Link

- [x] __define roles__

  - [Built-in roles for Azure resources](https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)

  - [Custom roles for Azure resources](https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles)

- [x] __recommend appropriate access control strategy__

## Design authentication

- [x] __choose an authentication approach__

  - [What are authentication methods?](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-authentication-methods)

|Authentication Method|Usage|
|--- |--- |
|Password|MFA and SSPR|
|Security questions|SSPR Only|
|Email address|SSPR Only|
|Microsoft Authenticator app|MFA and SSPR|
|OATH Hardware token|Public preview for MFA and SSPR|
|SMS|MFA and SSPR|
|Voice call|MFA and SSPR|
|App passwords|MFA only in certain cases|


- [x] __design a single-sign on approach__

  - [Single sign-on to applications in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-single-sign-on)

  - [Azure Active Directory Seamless Single Sign-On](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sso)

- [x] __design for IPSec authentication__

  - IPSec = Internet Protocol Security

- [x] __design for logon authentication__

- [x] __design for multi-factor authentication__

  - [How it works: Azure Multi-Factor Authentication](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks)

  - [Configure Azure Multi-Factor Authentication settings](https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-mfasettings)

- [x] __design for network access authentication__

  - [SECURE YOUR NETWORK ACCESS WITH AZURE MULTI-FACTOR AUTHENTICATION](https://www.swc.com/blog/cloud/azure-multi-factor-authentication-network-security)

- [x] __design for remote authentication__

## Design authorization

- [x] __choose an authorization approach__

  - Use [RBAC](https://docs.microsoft.com/en-us/azure/role-based-access-control/), define user groups and assigns [users to user groups](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/methods-for-assigning-users-and-groups) to manage access to resources

  - Take adventage of built in Azure roles
    - ReadOnly
    - Contributor
    - Owner

- [x] __define access permissions and privileges__

  - Access persmissions can be defined for users directly or via user groups or also to applications

- [x] __design secure delegated access__

  - [Delegate administration in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/roles-concept-delegation)

- [x] __recommend when and how to use API Keys__

  - Use API Keys to carry claims and ohter authorozation info between APIs, for this leverage [Azure API Management](https://docs.microsoft.com/en-us/azure/api-management/)

## Design for risk prevention for identity

- [x] __design a risk assessment strategy__

  - [Azure Active Directory risk detections](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-risk-events)

  - Take adventage of [Users flagged for risk report](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-user-at-risk) and [Risky sign-ins report](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-risky-sign-ins) to be aware and asses risk to identity integrity

- [x] __evaluate agreements involving services or products from vendors and contractors__

- [x] __update solution design to address and mitigate changes to existing security policies, standards, guidelines and procedures__

## Design a monitoring strategy for identity and security

- [x] __design for alert notifications__

  - Use predefined, but configurable [Azure AD Privileged Identity Management](https://docs.microsoft.com/en-gb/azure/active-directory/privileged-identity-management/pim-email-notifications) alerting notifications to check fules of accessing important resources

- [x] __design an alert and metrics strategy__

  - Secure access into applications using identity by synchronize your on prem AD with [Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect)

  - Use [Azure AD Connect Health](https://docs.microsoft.com/en-gb/azure/active-directory/hybrid/whatis-hybrid-identity) to monitor identity synchronization between Azure AD and on-premises identity

  - Enable integration with [Azure Log Analytics](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/howto-integrate-activity-logs-with-log-analytics) to monitor identity related logs in detail

- [x] __recommend authentication monitors__

  - Use [Azure Identity Protection](https://docs.microsoft.com/en-gb/azure/active-directory/identity-protection/overview-identity-protection) to detect and remediate identity based risks

  - Configure and get [notifications](https://docs.microsoft.com/en-gb/azure/active-directory/identity-protection/howto-identity-protection-configure-notifications) from Azure Identity Protection
