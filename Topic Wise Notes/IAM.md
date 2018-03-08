# IAM (Identity Access Management)

## Important Points
 1. IAM allows to manage users and their level of access to AWS console. 
 2. It comes under "Security, Identity & Compliance"
 3. IAM does not have any region. It is global.
 4. A root account is the email address which has been used to signup to AWS.
 5. Access key ID and secret access key are used for only interacting with AWS in a programmatic way. They cannot be used to login to management console.
 6. Username and password cannot be used to interact with AWS in a programmatic way. They are used to login to management console.
 7. New users have no access when first created.
 8. Always setup MFA(Multifactor Authentication) on your root accont.
 9. We can create and customize our own password rotation policy.
 10. Root has adminstrator level access
 11. Users and policy documents are applied globally.
 12. "Power User Access" allows access to all AWS services except management of groups and users within IAM.
 13. Roles are global and not region specific.

## What does it do?
- Centralized control of AWS account
- Shared access to AWS account
- Granular Permissions
- Identity Federation 
- Multifactor Authentication
- Provide temporary access for users/devices and service where neccessary
- Integrates with many AWS services
- Allows to setup password rotation policy
- Supports PCI DSS Compliance

## Critical Terms
- Users (End Users)
- Groups (A collection of users under one set of permissions)
- Roles (You create roles and then can assign to AWS resources)
- Policies (A document that defines one/more permissions)