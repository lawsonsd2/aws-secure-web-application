**Objective:**

Deploy Amazon CloudFront in front of the Foody Woody S3 website to improve performance and enforce secure HTTPS connections.

**Services Used:**
- Amazon S3
- Amazon CloudFront
- Origin Access Control (OAC)

**Configuration**

CloudFront Distribution:
- Origin: foody-woody-website
- Origin Type: Amazon S3
- Cache Policy: CachingOptimized
  
Security Settings:
- Redirect HTTP to HTTPS
- Allowed Methods: GET, HEAD
- OAC enabled
  
Root Object:
- index.html

**Testing**

Verified:

- CloudFront distribution deployed successfully.
- Website accessible through CloudFront domain.
- HTTPS lock icon present.
- S3 bucket remains private.
  
**Benefits**
- Faster content delivery.
- Improved scalability.
- Reduced S3 requests.
- Enhanced security through OAC.
