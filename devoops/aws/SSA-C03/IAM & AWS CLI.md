### IAM : Users & Groups
- IAM = Identity and Access Management, <Strong>Global</Strong> service
- <Strong>Root account</Strong> created by default, shouldn't be used or shared
- <Strong>Users</Strong> are people within your organization, and can be grouped
- <Strong>Groups</Strong> only contain users, not other groups
- Users don't have to belong to a group, and user can belong to multiple groups

### IAM : Permissions
- <Strong>Users or Groups</Strong> can be assigned JSON documents called policies
- These policies define the <Strong>permissions</Strong> of the users
- In AWS you apply the <Strong>least privilege principle</Strong> : don't give more permissions than a user needs

### IAM Policies Structure
- Consists of
  - <Strong>Version</Strong> : policy language version, always include "2012-10-17"
  - <Strong>Id</Strong> : an identifier for the policy (optional)
  - <Strong>Statement</Strong> : one or more individual statements (required)
- Statements consists of
  - <Strong>Sid</Strong> : an identifier for the statement (optional)
  - <Strong>Effect</Strong> : whether the statement allows or denies access (Allow, Deny)
  - <Strong>Principal</Strong> : account/user/role to which this policy applied to
  - <Strong>Action</Strong> : list of actions this policy allows or denies
  - <Strong>Resource</Strong> : list of resources to which the actions applied to
  - <Strong>Condition</Strong> : conditions for when this policy is in effect (optional)

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
- <Strong> You want to protect your Root Accounts and IAM users</Strong>
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