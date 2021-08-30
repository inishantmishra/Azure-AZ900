# Active Directory

### Roles in AD

- Access can be given at resource level
- Access can be given at resource group level
- Access can be given at subscription level

### Basic InBuilt roles

- Contributor-
  Allow full acess to manage all resources but does not allow you to assign roles in Azure RBAC or share image gallaries.
- Owner-
  - Grants full access to manage all resources, including the ability to assign roles in RBAC.
- Reader-
  - View all resources but does not allow you to make any changes
- User Access Administrator-

  - Lets you manage user access to Azure Resources.

- Access Control(IAM) is used to assign roles.

- We can create Azure AD groups as a set of users.

> MFA- By using Per user MFA

> To have Conditional Access MFA you need to have Azure AD Premium P2 license. You can try for free trial also.

### Azure Key Vault

- It stores Secret Keys, Encryption keys, Password secrets, Certificates
- Secret Identifier is the url by which we can access the value of secret key.
- You can also easily provision, manage, and deploy public and private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates
- All of the secrets and keys are safeguarded by Azure, using industry-standard algorithms, key lengths, and hardware security modules (HSMs).
- You can also monitor all the key vault activity by enabling logging. The logs can be sent to an Azure storage account, to an event hub or to Azure Monitor logs.

### Azure Policies

- We can use policy to apply some rule on subscription.
- To do that go to Policy Menu and find all default policies under Policy Definitions.

- For conditional access policies, premium ad lincense is required.

### Management Groups

- It is a concept of grouping the set of (subscription-> resource groups-> resources) under one group. Ex- Department name like HR, Logistics Management groups
- Default Root group will be Tenant Root group. Under this all Management groups will be created.
- A management group can contain multiple subscriptions.
- Advantage of Management groups are:
  - Billing as per different departments
  - Roles will be inherited to all resources, resource groups, subscription if given at Mnagament group level. Hence, role access can be given as per department.

### Resource Locks

- Locking resourcse help us to ensure dont accidently delete or modify resources
- 2 types of locks:
  - CanntoDelete
  - ReadOnly
- Locks can be ceated at Subscription, ResourceGroup, Resources level

### Azure Security Center

- Concept is to get security overview of all resources under your subscription
- We can see all security recommendations and check whether we are following or are we havign any unhealthy recommendation.
- This is an infrastructure security management system.

- You can use this tool to improve the security of your Azure based resources and on-premise resources as well.

- Azure Security Center has in-built support for services such as Azure virtual machines , Function Apps, Azure SQL Server databases.

- You can also allow Azure Security Center to give recommendations on what to do for on-premise Windows and Linux servers.

- On these servers, you need to ensure you install the Microsoft Monitoring agent.

- This service also helps detect and prevent threats at an Infrastructure layer

### Azure Sentinel

- Cloud Service to provide
  a solution for Security Information Event Management and Security Orchestration Automated Response
- You can collect data across all users, devices, apps.
- It helps to detect undected threats

- Azure Security Centre Vs Azure Sentinel

### Azure Blueprints

- This is a service that allows you to define a repeatable set of Azure resources.

- The definition of the Azure resources can adhere to an organization’s standards, patterns and requirements.

ˇUsing blueprints , you can orchestrate the deployment of resources such as role assignments, policy assignments, Azure resource manager templates and resource groups.

- Some differences between Azure blueprints and resource manager templates

- You can use blueprints to upgrade several subscriptions at once .

- The relationship between the blueprint definition and the blueprint assignment is reserved.

### Azure DDoS protection

- This service helps protect against Distributed denial of service attacks.

- This is probably the biggest security concern for companies when they expose their applications to the Internet.

- You have 2 plans for Azure DDoS protection.

  - Basic – This is automatically enabled. This continuously monitors traffic in real time and looks at mitigation of common network-level attacks.

  - Standard – This is a paid plan. But you get many benefits

    – Here you can get real time attack metrics and diagnostic logs via Azure Monitor

    – You can get help from DDoS Experts during a live attack
