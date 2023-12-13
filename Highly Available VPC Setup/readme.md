# Highly Available VPC Setup

In this project, I designed and implemented a highly available and fault-tolerant infrastructure within an Amazon Virtual Private Cloud (VPC) using AWS services. The goal was to showcase my practical experience in cloud engineering, emphasising key AWS components and high availability design.

## Project Overview

I set out to create an infrastructure that could withstand component failures while ensuring rapid recovery. This involved leveraging AWS services such as Elastic Load Balancing, Auto Scaling groups, and Amazon Relational Database Service (RDS) to build a robust and resilient system.

### Task 1: VPC Setup

- Created an Amazon VPC with public and private subnets across two Availability Zones.
- Deployed an internet gateway for connectivity.
- Implemented NAT gateways for private subnets, enabling outbound internet access while maintaining security.
- Configured security groups and network ACLs to control inbound and outbound traffic.

### Task 2: Launch Template Creation

- Developed an EC2 instance launch template that included the necessary parameters for launching Amazon Machine Images (AMIs) and instance types.
- Selected Amazon Linux 2 as the OS and utilized the t3.micro instance type.
- Integrated user data to automate instance configurations.

### Task 3: Auto Scaling Group Setup

- Created an Auto Scaling group to deploy EC2 instances across private subnets.
- Leveraged the power of Load Balancing to route incoming application traffic.
- Configured the group for high availability across multiple Availability Zones, ensuring system resiliency.
- Enabled CloudWatch metrics collection for monitoring.

### Task 4: Database High Availability

- Implemented a highly available Amazon Aurora database cluster.
- Configured Aurora to run across multiple Availability Zones for failover capabilities.
- Ensured the database's ability to withstand primary instance failures and promoted a read replica when needed.

### Task 5: NAT Gateway Redundancy

- Made NAT gateways highly available by launching a second NAT gateway in a different Availability Zone.
- Created and configured a new route table to direct traffic through the new NAT gateway.
- Ensured continuous outbound internet access, even in the event of a failure.

### Task 6: Testing High Availability

- Simulated failures at various levels, including EC2 instances and the primary database instance.
- Demonstrated the system's ability to recover and maintain high availability.
- Monitored the health and performance of the infrastructure using Amazon CloudWatch.

## Architecture Diagram

![Architecture Diagram](https://github.com/LeeDrew86/AWS-Projects/blob/65839cda8bfb26553c4fa2a04e7f2afbf924b104/Highly%20Available%20VPC%20Setup/Highly%20Available%20VPC%20Diagram.png)


## Conclusion

Through this project, I've demonstrated my ability to:

- Create a resilient VPC with highly available network components.
- Set up and manage Auto Scaling groups for application servers.
- Design and implement high availability for Amazon Aurora databases.
- Ensure fault tolerance and redundancy in the network with dual NAT gateways.
- Verify the robustness of the infrastructure through simulated failures and monitoring.

This hands-on experience closely aligns with the skills and knowledge required for cloud engineering positions that demand expertise in AWS, VPC design, and high availability architecture.
