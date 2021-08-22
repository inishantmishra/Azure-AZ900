# Active Directory

### Roles in AD

- Access can be given at resource level
- Access can be given at resource group level
- Access can be given at subscription level

### Basic InBuilt roles

- Contributor
- Owner
- Reader
- User Access Administrator

> MFA- By using Per user MFA

> To have Conditional Access MFA you need to have Azure AD Premium P2 license. You can try for free trial also.

### Azure Key Vault

- It stores Secret Keys, Encryption keys, Password secrets, Certificates
- Secret Identifier is the url by which we can access the value of secret key.

### Azure Policies

- We can use policy to apply some rule on subscription.
- To do that go to Policy Menu and find all default policies under Policy Definitions.

### Management Groups

- It is a concept of grouping the set of (subscription-> resource groups-> resources) under one group. Ex- Department name like HR, Logistics Management groups
- Default Root group will be Tenant Root group. Under this all Management groups will be created.
- Advantage of Management groups are:
  - Billing as per different departments
  - Roles will be inherited to all resources, resource groups, subscription if given at Mnagament group level. hence, role access can be given as per department.

### Resource Locks

- Locking resourcse help us to ensure dont accidently delete or modify resources
- 2 types of locks:
  - CanntoDelete
  - ReadOnly
- Locks can be ceated at Subscription, ResourceGroup, Resources level

### Azure Security Center

- Concept is to get security overview of all resources under your subscription
- We can see all security recommendations and check whether we are following or are we havign any unhealthy recommendation.

### Azure Sentinel

- Cloud Service to provide
  a solution for Security Information Event Management and Security Orchestration Automated Response
- You can collect data across all users, devinces, apps.
