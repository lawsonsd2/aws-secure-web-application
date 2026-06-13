**Phase 4 – AWS Identity and Access Management (IAM)**

**Objective:**

Implement secure user access for the Foody Woody cloud environment by creating an IAM user with limited permissions and enabling multi-factor authentication.
##
**Services Used**
- AWS IAM
##
**User Name:**

food-admin

**Console Access**

Enabled

**Password Management**

- Auto-generated password
- User required to change password at first sign-in
##
**Permissions Assigned**

The following managed policies were attached to the IAM user:

| Policy | Purpose |
|----------|---------|
| AmazonS3FullAccess | Manage the S3 bucket hosting the Foody Woody website |
| CloudFrontFullAccess | Manage the CloudFront distribution |
| AWSWAFFullAccess | Configure and manage AWS WAF protections |
| IAMReadOnlyAccess | View IAM resources without modifying them |
##
**Multi-Factor Authentication**

MFA was enabled using an authenticator application to provide an additional layer of account security.

Benefits:

- Protects against password compromise.
- Requires possession of a trusted device.
- Strengthens account authentication.
##
**Security Principles Applied**
**Least Privilege**

Permissions were limited to only the services required for the project.

**Separation from Root Account**

Administrative tasks are performed using an IAM user instead of the AWS root account.

**Multi-Factor Authentication**

A second authentication factor protects against unauthorized access.
##
**Security Benefits**
- Reduced risk of accidental root account usage.
- Improved account protection.
- Controlled access to AWS services.
- Stronger authentication through MFA.
