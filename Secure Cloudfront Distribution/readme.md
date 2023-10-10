# Creating a Cloudfront Distribution with Secure S3 Origin

## Scenario Overview
In a real-life scenario, this lab is highly relevant for securing the distribution of sensitive web assets. By configuring CloudFront with an Amazon S3 origin, the setup ensures robust security measures. Access control through Origin Access Identity (OAI), public access blockers, encryption, global content distribution, and high availability across multiple Availability Zones collectively create a secure content delivery network. This safeguards web assets from unauthorized access and potential threats, aligning with industry best practices and AWS's security standards.

## Lab Environment
My dedicated lab environment was designed to mimic a real-world setup and came with:

- Amazon VPC (with necessary network structure) deployed across multiple availabilty zones
- An auto scaling group of EC2, serving as public web servers
- Elastic Load Balancer

## Step 1: Creating an S3 Bucket and Configuring Public Access
Next, I set up an S3 bucket and made it accessible to the public:

- I created a new S3 bucket.
- To allow public access, I edited the Block public access settings.
- In the Bucket policy section, I copied and pasted a bucket policy into the editor. [The JSON bucket policy can be foudn inthe repository.]

**Note**: In the provided JSON policy, `"your-bucket-name"` is a placeholder representing the name of your Amazon S3 bucket. You should replace `"your-bucket-name"` with the actual name of the S3 bucket to which you want to apply this policy.

## Step 2: Putting Objects in the Bucket
- I created a new folder within the bucket.
- Then I uploaded a test image to the bucket.
- Finally, I tested public access to the uploaded object.

## Step 3: Adding the Bucket as an Additional Origin to CloudFront
In this step, I integrated the S3 bucket as an additional origin for the CloudFront distribution:

- I chose the existing CloudFront distribution.
- I created a new origin for my S3 bucket.
- Configuring the settings for the new origin was a crucial part.
- Additionally, I created a new Origin Access Identity (OAI).
- Lastly, I configured a new behavior for my S3 origin.

## Step 4: Securing the Bucket with CloudFront OAI
To enhance security, I ensured that the S3 bucket only allowed access through CloudFront using the Origin Access Identity (OAI):

- I configured the bucket's policy to permit access only through CloudFront using the OAI.
- Editing the allowed principal in the bucket policy was an essential step.
- Public access blockers were also enabled to bolster security.

## Step 5: Testing Direct Access to an Object in the Bucket Using the Amazon S3 URL
I tested if direct access to an object in the S3 bucket was restricted:

- Attempting to access an object using the Amazon S3 URL was a part of this test.
- I confirmed that direct access was indeed restricted.

## Step 6: Testing Access to the Object in the Bucket Using the CloudFront Distribution
Finally, I verified if accessing an object through the CloudFront distribution worked as expected:

- I accessed an object through the CloudFront distribution.
- Confirmed that the object was retrieved from the CloudFront distribution.

![Architecture Diagram](https://github.com/LeeDrew86/AWS-Projects/blob/785721f2bb0844c8eeb7fe5a3b79f443d2b0837a/Secure%20Cloudfront%20Distribution/Cloudfront%20with%20S3%20Origin%20Diagram.png)

## Conclusion
In conclusion, I successfully completed this lab, configuring Amazon CloudFront with an Amazon S3 origin and securing access to the S3 bucket. This experience closely resembled the real-world scenario of setting up a content delivery network (CDN) for a website and ensuring the security of assets hosted on Amazon S3.
