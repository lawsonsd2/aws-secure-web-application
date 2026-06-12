## Phase 1 – Amazon S3 Secure Website Storage    

Objective:  

Create a secure Amazon S3 bucket to store static website files for the Restaurant web application.  

## Services Used  
-Amazon S3  
##

**Actions Performed**

**1. Created an S3 Bucket**

A dedicated bucket was created to store website assets.

**2. Uploaded Website Files**

The following files were uploaded:

 - index.html  
 - styles.css  
 - images  
 
**3. Enabled Versioning**

Bucket versioning was enabled to provide protection against accidental deletion and allow recovery of previous object versions.

**4. Maintained Block Public Access Settings**

All public access settings remained enabled to ensure the bucket cannot be accessed directly from the Internet.
##

**Security Considerations**  

**Private Storage**

The S3 bucket remains private.

Direct public access was intentionally disabled because website content will eventually be delivered through Amazon CloudFront using Origin Access Control (OAC).

**Versioning**

Versioning improves resilience by allowing recovery from accidental overwrites or deletions.

**Principle of Least Exposure**

Restricting public access reduces the attack surface and prevents unauthorized access to website assets.
##
**Skills Demonstrated**

Amazon S3
- Secure bucket configuration
- Versioning
- Static website hosting concepts
- Object storage management
##

**Lessons Learned**

During this phase, I did the following:

- Create and configure an Amazon S3 bucket.
- Upload and manage a static website asset.
- Enable versioning for object recovery.
- Apply secure storage practices by preventing public access.
- Prepare an S3 bucket for integration with Amazon CloudFront and Origin Access Control.
