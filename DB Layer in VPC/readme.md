# Creating a Database Layer within a VPC

## **Scenario Overview**

In a practical, hands-on lab environment, I've taken on the task of designing a robust and scalable architecture for a web-based application, with a key focus on implementing a secure and efficient database layer within an Amazon Virtual Private Cloud (VPC).

The goal was to create an architecture that delivers outstanding performance, reliability, and scalability, with a specific emphasis on the secure management of data through the implementation of a VPC-based database layer.

## **Lab Environment**

Working in a lab environment, I had access to essential resources:

- Amazon Virtual Private Cloud (Amazon VPC)
- Network structure
- Security groups
- Two EC2 instances in a private subnet
- AWS Systems Manager Session Manager profile

## **Step 1: Creating an Amazon RDS Database**

- I created an Aurora DB cluster compatible with MySQL.
- Engine options and templates were configured.
- I specified DB cluster details, master credentials, and instance settings.
- Setting up VPC, subnet groups, and security was my responsibility.
- Enhanced monitoring was skipped.
- I completed additional configurations and created the database.

## **Step 2: Creating and Configuring an Application Load Balancer**

### **Task 2.1: Creating a Target Group**

- I established a target group for EC2 instance management.
- Configuration included target type, name, and VPC settings.
- Registration of EC2 instances was done by me.

### **Task 2.2: Creating an Application Load Balancer**

- I designed the Application Load Balancer to manage incoming traffic.
- Configuration involved naming, network mapping, security groups, and listeners.
- Saving the configuration was my final step.

## **Step 3: Reviewing the Amazon RDS DB Instance Metadata**

- In the Amazon RDS console, I monitored the Aurora DB cluster.
- I reviewed connectivity and security.
- I copied the writer instance endpoint.

## **Step 4: Testing Application Connectivity to the Database**

- I tested the application's connectivity by accessing the Application Load Balancer URL.
- Configuration for a secure database connection was my task.
- I verified application functionality.

### **Step 5: Creating an Amazon RDS Read Replica**

- I created a cross-Region Read Replica from the source DB instance.
- Then I configured network settings.
- Finally, I initiated the creation of the Read Replica.

This step is aimed at enhancing read operation scalability by creating a Read Replica of the source database.


### **Architecture Diagram**

![Architecture diagram](https://github.com/LeeDrew86/AWS-Projects/blob/8134ae2d1585e92aa327a48c2a8b1264ddd55fd4/DB%20Layer%20in%20VPC/DB%20Layer%20in%20VPC-DIAGRAM.png)

## **Conclusion**

In this project, I:

- Created an Amazon RDS DB instance for the web application's data layer.
- Developed an Application Load Balancer for efficient traffic distribution.
- Configured target groups and registered EC2 instances for load balancing.
- Monitored Amazon RDS DB instance metadata.
- Conducted tests to ensure application connectivity and functionality.

This project demonstrates my ability to design a robust infrastructure for web applications, focusing on performance, reliability, and scalability. While it serves as a prototype, it showcases my skills relevant to cloud architecture and database management roles.
