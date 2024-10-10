### AWS Organizations
- Global service
- Allows to manage multiple AWS accounts
- The main account is the management account
- Other accounts are member accounts
- Member accounts can only be part of one organization
- Consolidated Billing across all accounts usage (volume discount for EC2, S3...)
- **Shared reserved instances and Savings Plans discounts across accounts**
- API is available to automate AWS account creation

- **Advantages**
  - Multi Account vs One Account MultiVPC
  - Use tagging standards for billing purpose
  - Enable CloudTrail on all accounts, send logs to central S3 account
  - Send CloudWatch Logs to central logging account
  - Establish Cross Account Roles for Admin purposes
- **Security: Service Control Policies (SCP)**
  - IAM polices applied to OU or Accounts to restrict Users and Roles
  - They do not apply to the management account (full admin power)
  - Must have an explicit allow from the root through each OU in the direct path to the target account (does not allow anything by default - like IAM)

### SCP Hierarchy
- Management Account
  - Can do anything (no SCP apply)
- Account A
  - Can do anything
  - EXCEPT S3 (explicit Deny from Sandbox OU)
  - EXCEPT EC2 (explicit Deny)
- Account B & C
  - Can do anything
  - EXCEPT S3 (explicit Deny from Sandbox OU)
- Account D
  - Can access EC2

### Advanced Policies
- IAM Conditions
  - aws:SourceIp : restrict the client IP from which the API calls are being made
  - aws:RequestedRegion : restrict the region the API calls are made to
  - ec2:ResourceTag : restrict based on tags
  - aws:MultiFactorAuthPresent : to force MFA
- IAM for S3
  - s3:ListBucket permission applies to arn:aws:s3:::test
    - bucket level permission
  - s3:GetObject, s3:PutObject,s3:DeleteObject applies to arn:awn:s3:::test/*
    - object level permission
- Resource Policies & aws:PrincipalOrgID
  - aws:PrincipalOrgID can be used in any resource policies to restrict access to accounts that are member of an AWS Organization

### IAM Roles vs Resource Based Policies
- Cross account:
  - ataching a resource-based policy to a resource (example:S3 bucket policy)
  - OR using a role as a proxy

### IAM Roles vs Resource-Based Policies
- **When you assume a role (user, application or service), you give up your original permissions and take the permissions assihned to the role**
- When using a resource-based policy, the principal doesn't have to give up his permissions
- <u>Example</u>: User in account A needs to scan a DynamoDB table in Account A and dump it in an S3 bucket in Account B
- Supported by: Amazon S3 buckets, SNS topics, SQS queues, etc...

### Amazon EventBridge - Security
- When a rule runs, it needs permissions on the target
- Resource-based policy: Lambda, SNS, SQS, S3 buckets, API Gateway....
- IAM role: Kinesis stream, Systems Manager Run Command, ECS task...

### IAM Permission Boundaries
- IAM Permission Boundaries are supported for users and roles (not groups)
- Advanced feature to use a managed policy to set the maximum permissions an IAM entity can get

### AWS IAM Identity Center (successor to AWS Single Sign-On)
- One login (single sign-on) for all your
  - **AWS accounts in AWS Organizations**
  - Business cloud applications (e.g., Salesforce, Box, Microsoft 365, ....)
  - SAML2.0-enabled applications
  - EC2 Windows Instances
- Identity providers
  - Built-in identity store in IAM Identity Center

### AWS IAM Identity Center Fine-grained Permissions and Assignments
- **Multi-Account Permissions**
  - Manage access across AWS accounts in your AWS Organization
  - Permission Sets - a collection of one or more IAM Policies assigned to users and groups to define AWS access
- **Application Assignments**
  - SSO access to many SAML 2.0 business applications (Salesforce, Box, Microsoft 365,...)
  - Provide required URLs, certificates, and metadata
- **Attribute-Based Access Control (ABAC)**
  - Fine-grained permissions based on users' attributes stored in IAM Identity Center Identity Store
  - Example: cost center, title, locale, ...
  - Use case: Define permissions once, then modify AWS access by changing the attributes