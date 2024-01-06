# Multi-Environment Pipeline Implementation

## Project Overview

This project builds upon prior experience in CI/CD, aiming to simulate a real-world scenario with multiple environments—development and production. 

[Project Diagram](https://github.com/LeeDrew86/AWS-Projects/blob/main/Multi-Environment%20Pipeline/CICD%20Project.drawio.png)

### Development Setup

- Created a new 'dev' branch in the GitHub repository using 'git checkout -b dev'.
- Modified the 'index.html' file on the 'dev' branch for subsequent testing.

### Environment Setup

- Provisioned new EC2 instances, duplicating existing setups to save time by copying over user data, security groups and roles.
- Assigned 'env' tags to distinguish between 'prod' and 'dev' environments.

### CodeDeploy Application and Deployment

- Created the 'Apache' CodeDeploy Application.
- Configured deployments for 'Dev' and 'Prod,' linking them to respective instances.

### Pipeline Creation and Testing

- Set up a 'Development' pipeline, linking it to the 'dev' branch.
- Resolved errors in 'appspec.yml', commenting out lifecycle hook as there were no files in root directory to remove.
- Validated Apache functionality on Dev instance and confirmed prod instance showed different content.

### Production Pipeline and Deployment

- Established the 'Production' pipeline, connected to the main repository branch.
- Simulated a review process by initiating a "compare and pull request."
- In a commercial setting, it is at this point a Senior Engineer would recieve the request and check for errors.
- I Merged 'dev' with 'prod' to simulate successful testing and deployment completion.

## Conclusion

This project demonstrated the deployment of code across multiple environments, mimicking real-world testing and final deployment scenarios. The hands-on experience significantly enhanced my understanding of CI/CD processes—an invaluable skill in cloud engineering.
