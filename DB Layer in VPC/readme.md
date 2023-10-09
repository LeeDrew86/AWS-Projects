# Creating a Database Layer within a VPC

## <span style="color:blue">**Scenario Overview**</span>

Imagine I'm part of a dynamic development team tasked with creating a web-based application

Our goal is to design an architecture that delivers outstanding performance but also ensures reliability and scalability


Lab Environment

To simulate and address the complexities of the real-life scenario, I accessed a dedicated lab environment. This environment includes essential resources like Amazon VPC, network structures, security groups, EC2 instances, and associated profiles. Leveraging these resources, I'm ready to prototype, test, and refine the architecture that will drive the project's success.

## <span style="color:blue">**Lab Environment**</span>

- Amazon Virtual Private Cloud (Amazon VPC)
- Necessary network structure
- Three security groups for traffic control
- Two EC2 instances in a private subnet
- Associated EC2 instance profile for AWS Systems Manager Session Manager

### <span style="color:blue">**Architecture Diagram**</span>

![Architecture diagram](https://github.com/LeeDrew86/AWS-Projects/blob/8134ae2d1585e92aa327a48c2a8b1264ddd55fd4/DB%20Layer%20in%20VPC/DB%20Layer%20in%20VPC-DIAGRAM.png)


## <span style="color:blue">**Step 1: Creating an Amazon RDS Database**</span>

- Create an Aurora DB cluster compatible with MySQL.
- Configure engine options.
- Choose Dev/Test templates.
- Configure DB cluster identifier, master username, and password.
- Specify DB instance class and availability settings.
- Set up virtual private cloud (VPC), DB subnet group, and security groups.
- Skip Enhanced monitoring.
- Complete additional configuration.
- Create the database.

## <span style="color:blue">**Step 2: Creating and Configuring an Application Load Balancer**</span>

### <span style="color:blue">**Task 2.1: Creating a Target Group**</span>

- Create a target group.
- Configure target type, target group name, and VPC.
- Register EC2 instances with the target group.

### <span style="color:blue">**Task 2.2: Creating an Application Load Balancer**</span>

- Create an Application Load Balancer.
- Configure load balancer name and network mapping.
- Set security groups and listeners.
- Save the configuration.

## <span style="color:blue">**Step 3: Reviewing the Amazon RDS DB Instance Metadata**</span>

- Navigate to the Amazon RDS console.
- Check the status of the Aurora DB cluster.
- Review connectivity and security details.
- Copy the writer instance endpoint.

## <span style="color:blue">**Step 4: Testing Application Connectivity to the Database**</span>

- Access the Application Load Balancer URL.
- Configure settings to connect to the database.
- Verify application connectivity and functionality.

## <span style="color:blue">**Optional Task: Creating an Amazon RDS Read Replica**</span>

- Create a cross-Region read replica from the source DB instance.
- Configure multi-AZ deployment and network settings.
- Initiate the creation of the read replica.

## <span style="color:blue">**Conclusion**</span>

In this lab, I've successfully:

- Created an Amazon RDS DB instance.
- Set up an Application Load Balancer.
- Configured target groups.
- Registered targets.
- Tested load balancing and application connectivity.
- Reviewed Amazon RDS DB instance metadata.

Please note that while this lab serves as a prototype, it may not meet all AWS Cloud best practices. High availability and redundancy considerations are addressed in the next lab.

[Link to architecture diagram]
