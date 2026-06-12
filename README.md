# aws-secure-web-environment
Secure AWS Web Application Environment demonstrating Amazon S3, Amazon Cloudfront, AWS WAF, AWS IAM, Amazon Cloudwatch and Cloudtrail

## Overview
A fast-growing restaurant, wants to launch its online website to showcase menus, offers, and customer reviews. The business needs the site to be globally accessible, fast, and most importantly secure from cyber threats like SQL injection (SQLi), cross-site scripting (XSS), and DDoS attacks

## Solution
A serverless and secure website hosted on Amazon S3, delivered globally using Amazon CloudFront, and protected by AWS WAF. To ensure best practices, we’ll enforce Origin Access Control (OAC) to restrict direct S3 access, apply least-privilege IAM policies, and use CloudWatch for monitoring and logging.

## Objectives
-Creating and configuring an S3 bucket for website hosting  
-Securing the bucket using Origin Access Control (OAC)  
-Setting up a CloudFront distribution with HTTPS enforced  
-Attaching AWS WAF for web application security  
-Enabling CloudWatch/CloudTrail for monitoring and compliance

## Technologies Utilized
Amazon S3 → Store and serve static website files (HTML, CSS, images)  
Amazon CloudFront → Distribute content globally with low latency and HTTPS  
AWS WAF → Protect against SQLi, XSS, bots, and malicious requests  
AWS IAM → Manage least-privilege permissions for access control  
Amazon CloudWatch & CloudTrail → Monitor logs, track user actions, and detect anomalies

## Architecture
<img width="541" height="298" alt="Architecture" src="https://github.com/user-attachments/assets/4f01d968-12d6-40c0-9381-127ad845e6d2" />

