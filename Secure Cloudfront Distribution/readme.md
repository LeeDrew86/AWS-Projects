# Securing Content Delivery with CloudFront and S3

## Introduction
In this lab, I successfully configured Amazon CloudFront with an Amazon S3 origin while implementing robust security measures. This hands-on experience demonstrates my ability to secure content delivery networks (CDNs) and aligns with industry best practices and AWS security standards.

## Lab Environment
For this project, I utilized an Amazon VPC with a multi-availability zone network structure and set up an auto-scaling group of EC2 instances as public web servers. Employing an Elastic Load Balancer allowed for efficient load distribution.

### Step 1: Creating an S3 Bucket and Ensuring Public Access
- To begin, I created a new S3 bucket.
- I crafted a bucket policy to enable public access (refer to the provided [JSON bucket policy](https://github.com/your-repository/bucket-policy.json)).

**Note**: In the provided JSON policy, `"your-bucket-name"` is a placeholder representing the name of your Amazon S3 bucket. Please replace `"your-bucket-name"` with the actual name of the S3 bucket to which you want to apply this policy.

### Step 2: Uploading Objects to the Bucket
- Within the newly created bucket, I established a new folder.
- I then uploaded a sample PNG image for testing.

### Step 3: Integrating the Bucket as an Additional CloudFront Origin
- My next step involved integrating the S3 bucket as an additional origin for CloudFront.
- I configured settings for the new origin, specifying the S3 bucket name as the origin and giving it a recognizable name within CloudFront distribution settings.
- Creating a new Origin Access Identity (OAI) for enhanced security, I enforced access through CloudFront URLs.
- Defining a new behavior for the S3 origin using CachedObjects/*.png ensured that only the test PNG file was retrieved from the CachedObjects folder of the S3 bucket.
- I finalized origin settings by adding the S3 bucket as the origin to CloudFront.

### Step 4: Enhancing Security with CloudFront OAI
- To enhance security, I implemented access control, allowing S3 bucket access only through CloudFront using the OAI.
- I also put in place measures to block public access, further strengthening my security posture.

### Step 5: Testing Restricted Direct Access
- A crucial step involved verifying that direct access to objects via Amazon S3 URL was successfully restricted.

### Step 6: Testing Access through CloudFront Distribution
- In the final step, I confirmed object retrieval through the CloudFront distribution.

## Architecture Diagram
![Architecture Diagram](https://github.com/LeeDrew86/AWS-Projects/blob/21be5405da47af28e3627a4a639e3fb1f37205c6/Secure%20Cloudfront%20Distribution/Cloudfront%20with%20S3%20Origin%20Diagram.png)

## Conclusion
Through this project, I've demonstrated my ability to:

- Set up and secure a content delivery network with Amazon CloudFront.
- Effectively control access to Amazon S3 resources.
- Address real-world challenges in securing content delivery.
- Ensure high availability across multiple availability zones.

This practical experience closely aligns with the skills and knowledge required for roles involving AWS, CDN setup, and cloud security.
