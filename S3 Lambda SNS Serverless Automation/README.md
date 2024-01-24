# Serverless Automation with AWS Lambda, S3, and SNS

## Introduction

This project aims to implement serverless automation using AWS Lambda, S3, and SNS. The goal is to set up an S3 object put notification with Lambda, and SNS subscribed to email, as an opportunity to improve Python and Boto3 skills.

## Steps

- **Step 1: Creating Lambda Function and IAM Role**
  - Created the Lambda function responsible for handling S3 put notifications.
  - Created an IAM role with S3 read access for Lambda and a custom SNS role allowing Lambda to publish messages.

- **Step 2: Setting up S3 Bucket and Event Notification**
  - Created the S3 bucket where the put notifications will be triggered.
  - Edited the S3 bucket event notification settings to trigger Lambda when a new object is put.

- **Step 3: Creating SNS Topic and Subscription**
  - Created an SNS Topic to act as a notification channel.
  - Subscribed to the SNS Topic using an email address for notifications.

- **Step 4: Developing Lambda Code**
  - Looked up Boto3 documentation on AWS for SNS publish operations.
  - Edited Lambda code to extract necessary information from the S3 event, such as bucket name and object name.
  - Tested Lambda function, addressing any bugs in the code (incorrect ARN suffix, spacing issues).

- **Step 5: Customizing Notification Content**
  - Extracted relevant parameters from the JSON received via email.
  - Used Python dictionaries to structure the code for publishing desired information (e.g., bucket name and object name).
  - Tested the Lambda function with an S3 upload to ensure correct extraction and publication of information.

## Conclusion

This project showcases the implementation of serverless automation using AWS Lambda, S3, and SNS. It highlights the benefits of serverless architecture and demonstrates practical Python and Boto3 usage for AWS cloud automation. The solution is scalable, cost-effective, and easy to maintain.
