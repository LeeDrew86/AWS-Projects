# CI/CD Project: GitHub-based Continuous Integration/Continuous Deployment

## Project Overview

Having gained familiarity with GitHub for uploading projects, this CI/CD project aims to implement a streamlined Continuous Integration/Continuous Deployment (CI/CD) process using AWS CodeDeploy and AWS CodePipeline. It's a continuation of previous practice, wherein several files were created in VSCode for experimentation. These included `index.html`, `second.html`, and `third.html`, serving as learning material for Git commands (`commit` and `push`), staging changes, and utilising `.gitignore` to conceal a confidential text file.

![project diagram](https://github.com/LeeDrew86/AWS-Projects/blob/main/CI-CD%20Project/CICD%20Project.png)
### Practice Repository and Initial Setup

In the "Git-Project" repository, basic files (`index.html`, `second.html`, `third.html`) were created, altering them to understand Git's version control concepts. Additionally, a confidential file was securely concealed using `.gitignore`.

## Creating the Pipeline

### Setting Up EC2 and CodeDeploy

Using AWS IAM, roles were created for CodeDeploy and EC2 to facilitate interaction. An EC2 instance was then launched, employing the IAM role as the instance profile, with the following user data to prepare the instance upon initialisation:

![user data ec2](https://github.com/LeeDrew86/AWS-Projects/blob/main/CI-CD%20Project/user%20data.png))

### CodeDeploy Application and Deployment Group

Following the successful instance setup, AWS CodeDeploy was employed to continue pipeline setup. An application and deployment group were established, integrating the previously generated IAM role.

### CodePipeline Setup

I then created a new pipeline, connecting my AWS account to GitHub and the appropriate repository. Choosing the previously created applciation and deployment groups, the pipeline was created and deployment began.

## Enabling Deployment and Automation

### AppSpec Configuration for CodeDeploy

Encountering a pipeline failure, it was discovered that an `appspec.yml` file was required in the source code's root directory for CodeDeploy functionality. The `appspec.yml` file was generated, directing CodeDeploy to transfer files from the source to the specified destination, i.e., the root folder of the Apache Web Server.

![AppSpec-CodeDeploy](https://github.com/LeeDrew86/AWS-Projects/blob/main/CI-CD%20Project/appspec.png)

### Expanding Automation with AppSpec Lifecycle Hooks

Exploring automation within CI/CD processes, lifecycle hooks were integrated into `appspec.yml`. A script, `empty_dir.sh`, was created to remove files from the root directory prior to uploading files through the pipeline, revealing the potential for customisation and automation.

![Lifecycle-Hooks-CodeDeploy](https://github.com/LeeDrew86/AWS-Projects/blob/main/CI-CD%20Project/bash.png)

## Conclusion and Future Endeavours

This project's completion marks the first phase, focusing on the successful implementation of a pipeline using AWS CodeDeploy. The next phase will explore the creation of a multi-environment pipeline.

### Learning and Troubleshooting

The project involved referencing AWS documentation for both setup and troubleshooting instances of pipeline failures. This practice enhanced understanding and resolved issues encountered during the implementation phase.

### Future Plans

Potential enhancements include refining automation, integrating multiple environments, and exploring further customisation within the CI/CD process.
