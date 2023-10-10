# Securing Content Delivery with CloudFront and S3

## Overview
In this lab, I successfully configured Amazon CloudFront with an Amazon S3 origin while implementing robust security measures. This hands-on experience demonstrates my ability to secure content delivery networks (CDNs) and aligns with industry best practices and AWS security standards.

## Lab Environment
- Utilised Amazon VPC with a multi-availability zone network structure.
- Set up an auto-scaling group of EC2 instances as public web servers.
- Employed an Elastic Load Balancer for load distribution.


### Step 1: Creating an S3 Bucket and Ensuring Public Access
- Created a new S3 bucket.
- Crafted a bucket policy to enable public access (refer to the provided [JSON bucket policy](https://github.com/your-repository/bucket-policy.json)).

**Note**: In the provided JSON policy, `"your-bucket-name"` is a placeholder representing the name of your Amazon S3 bucket. You should replace `"your-bucket-name"` with the actual name of the S3 bucket to which you want to apply this policy.


### Step 2: Uploading Objects to the Bucket
- Established a new folder within the bucket.
- Uploaded a sample png image for testing.

### Step 3: Integrating the Bucket as an Additional CloudFront Origin
- Integrated the S3 bucket as an additional origin for CloudFront.
- Configured settings for the new origin:
	-Specified S3 bucket name as the origin
	-Named the S3 origin to easily ID within CloudFront distribution settings
- Created a new Origin Access Identity (OAI) for enhanced security, it enforces access thorgh CloudFront URLs.
- Defined a new behaviour for the S3 origin using CachedObjects/*.png.
- This ensured, in this case, that only the test png file would be returned form the CachedObjects folder of the S3 bucket.
- Finalised origin, adding S3 bucket as the origin to CloudFront

### Step 4: Enhancing Security with CloudFront OAI
- Implemented access control, allowing S3 bucket access only through CloudFront using the OAI.
- Enhanced security with public access blockers.

### Step 5: Testing Restricted Direct Access
- Verified that direct access to objects via Amazon S3 URL was restricted.

### Step 6: Testing Access through CloudFront Distribution
- Confirmed seamless object retrieval through the CloudFront distribution.

## Architecture Diagram
![Architecture Diagram](https://github.com/your-repository/architecture-diagram.png)

## Conclusion
Through this lab, I demonstrated my ability to:

- Set up and secure a content delivery network with Amazon CloudFront.
- Effectively control access to Amazon S3 resources.
- Tackle real-world challenges in securing content delivery.
- Ensure high availability across multiple availability zones.

This practical experience closely aligns with the skills and knowledge required for roles involving AWS, CDN setup, and cloud security.
