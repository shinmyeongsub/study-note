### IAM : Users & Groups
- IAM = Identity and Access Management, <strong>Global</strong> service
- <strong>Root account</strong> created by default, shouldn't be used or shared
- <strong>Users</strong> are people within your organization, and can be grouped
- <strong>Groups</strong> only contain users, not other groups
- Users don't have to belong to a group, and user can belong to multiple groups

### IAM : Permissions
- <strong>Users or Groups</strong> can be assigned JSON documents called policies
- These policies define the <strong>permissions</strong> of the users
- In AWS you apply the <strong>least privilege principle</strong> : don't give more permissions than a user needs

### IAM Policies Structure
- Consists of
  - <strong>Version</strong> : policy language version, always include "2012-10-17"
  - <strong>Id</strong> : an identifier for the policy (optional)
  - <strong>Statement</strong> : one or more individual statements (required)
- Statements consists of
  - <strong>Sid</strong> : an identifier for the statement (optional)
  - <strong>Effect</strong> : whether the statement allows or denies access (Allow, Deny)
  - <strong>Principal</strong> : account/user/role to which this policy applied to
  - <strong>Action</strong> : list of actions this policy allows or denies
  - <strong>Resource</strong> : list of resources to which the actions applied to
  - <strong>Condition</strong> : conditions for when this policy is in effect (optional)

### IAM - Password Policy
- Strong passwords = higher security for your account
- In AWS, you can setup a password policy:
  - Set a minimum password length
  - Require specific character types:
    - including uppercase letters
    - lowercase letters
    - numbers
    - non-alphanumeric characters
  - Allow all IAM users to change their own passwords
  - Require users to change their password after some time (password expiration)
  - Prevent password re use

### Multi Factor Authentication - MFA
- Users have access to your account and can possibly change configurations or delete resources in your AWS account
- <strong> You want to protect your Root Accounts and IAM users</strong>
- MFA = password you know + security device you own
  - Password + MFA => Successful login
- Main benefit of MFA : if a password is stolen r hacked the account is not compromised

### MFA devices options in AWS
- Virtual MFA device
  - Google Authenticator (phone only), Authy (phone only)
    - Support for multiple tokens on a single device
- Universal 2nd Factor (U2F) Security Key
  - YubiKey by Yubico (3rd party)
    - Support for multiple root and IAM users using a single security key

### MFA devices options in AWS
- Hardware Key Fob MFA Device
  - provided by Gemalto
- Hardware Key Fob MFA Device for AWS GovCloud (US)
  - provided by SurePassID (3rd party)

### How can users access AWS?
- To access AWS, you have three options:
  - AWS Management Console (protected by password + MFA)
  - AWS Command Line Interface (CLI) : protected by access keys
  - AWS Software Developer kit (SDK) - for code: protected by access keys
- Access Keys are generated through the AWS Console
- Users manage their own access keys
- <U><strong>Access Keys are secret, just like a password. Don't share them</strong></U>
- Access Key ID ~= username
- Secret Access Key ~= password

### What's the AWS CLI?
- A tool that enables you to interact with AWS services using commands in your command-line shell
- Direct access to the public APIs of AWS services
- You can develop scripts to manage your resources
- It's open-source https://github.com/aws/aws-cli
- Alternative to using AWS Management Console

### Whats' the AWS SDK?
- AWS Software Development Kit (AWS SDK)
- Language-specific APIs (set of libraries)
- Enables you to access and manage AWS services programmatically
- Embedded within your application
- Supports
  - SDKs (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
  - Mobile SDKs (Android, iOS, ...)
  - IoT Device SDKs (Embedded C, Arduino, ...)
  - Example:AWS CLI is built on AWS SDK for Python

### IAM Roles for Services
- Some AWS service will need to perform actions on your behalf
- To do so, we will assign permissions to AWS services with IAM Roles
- Common roles :
  - EC2 Instance Roles
  - Lambda Function Roles
  - Roles for ColudFormation

### IAM Security Tools
- IAM Credentials Report (account-level)
  - a report that lists all your account's users and the status of their various credentials
- IAM Access Advisor (user-level)
  - Access advisor shows the service permissions granted to a user and when those services were last accessed.
  - You can use this information to revise your policies.

### IAM Guidelines & Best Practices
- Don't use the root account except for AWS account setup
- One physical user = One AWS user
- <strong> Assign users to groups</strong> and assign permissions to groups
- Create a strong password policy
- Use and enforce the use of <strong> Multi Factor Authentication (MFA)</strong>
- Create and use <strong>Roles</strong> for giving permissions to AWS services
- Use Access Key for Programmatic Access (CLI / SDK)
- Audit permissions of your account using IAM Credentials Report & IAM Access Advisor
- <strong> Never share IAM users & Access Keys </strong>

### IAM Section - Summary
- <strong>Users : </strong> mapped to a physical user, has a password for AWS Console
- <strong>Groups :</strong> Contains users only
- <strong>Policies :</strong> JSON document that outlines permissions for users or groups
- <strong>Roles :</strong> for EC2 instance or AWS services
- <strong>Security :</strong> MFA + Password Policy
- <strong>AWS CLI :</strong> manage your AWS services using the command-line
- <strong>AWS SDK :</strong> manage your AWS services using a programming language
- <strong>Access Keys :</strong> access AWS using the CLI or SDK
- <strong>Audit :</strong> IAM Credential Reports & IAM Access Advisor