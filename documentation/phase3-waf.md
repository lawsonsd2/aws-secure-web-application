**Phase 3 – AWS WAF Protection**

**Objective**:

Implement AWS WAF to protect the Foody Woody website from common web attacks and malicious traffic before requests reach the CloudFront distribution and S3 origin.
##
**Solution**:

Enabled AWS WAF protection for the CloudFront distribution using AWS Managed Core Rule Set. CloudFront automatically provisioned and associated a Web ACL to inspect incoming requests before they reached the S3 origin.
##

**Services Used**:

- Amazon S3
- Amazon CloudFront
- AWS WAF
- AWS Shield Standard
##

**Managed Rules Enabled**

**AWS Core Rule Set**

Protects against:

- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)
- HTTP protocol violations
- Common application vulnerabilities
  ##
**Optional Rule Groups**

- Amazon IP Reputation List
- Known Bad Inputs
##
**Resource Association**

The Web ACL was associated with the CloudFront distribution to inspect traffic before requests reached the S3 bucket.
##
**Verification**

The CloudFront website loaded successfully after attaching the Web ACL.

A malicious test request was sent:  
https://<distribution>.cloudfront.net/?q=<script>alert(1)</script>

AWS WAF detected the malicious payload and returned:

403 Forbidden

This confirmed that the AWS Managed Core Rule Set was functioning correctly.
##
**Edge Protection**

Threats are blocked at CloudFront edge locations before reaching the origin.

**DDoS Protection**

AWS Shield Standard provides automatic protection against common DDoS attacks.

**Scalability**

Security policies automatically scale with traffic demand.
