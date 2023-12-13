# Deploying WordPress on Amazon EC2 with LAMP Stack

## **Project Overview**

This project involved deploying a WordPress instance on an Amazon EC2 instance while setting up and optimising a LAMP (Linux, Apache, MySQL, PHP) stack. The primary goal was to establish a robust and dynamic web hosting environment for a WordPress-based website.

## **Step 1: Provisioning an Amazon EC2 Instance**

- I provisioned an Amazon EC2 instance, selecting appropriate specifications and setting up security groups for a secure environment.

## **Step 2: Installing LAMP Stack**

- Utilized AWS documentation to guide the installation of the LAMP stack components: Linux, Apache, MySQL, and PHP.

## **Step 3: WordPress Installation**

- Installed and configured the WordPress package from scratch on the EC2 instance.

## **Testing and Optimisation**

- Performed tests to ensure proper connectivity and responsiveness of the WordPress instance.
- Optimised the LAMP stack components for optimal performance and reliability.

### **Learning and Troubleshooting Experience**

- Employed AWS documentation extensively for guidance during the setup process.
- Faced challenges with MariaDB installation on Windows PowerShell in terms of compatability but successfully resolved it using AWS CloudShell.
- Utilised various troubleshooting techniques and resources, including online searches and diagnostic tools like `systemctl status`, to resolve encountered issues.

## **Future Enhancements**

In further iterations of this project, I plan to enhance security, availability, and scalability by implementing the following:

- **Network Segmentation:** Place the EC2 instance in a private subnet behind an Application Load Balancer (ALB) in a public subnet.
- **RDS Integration:** Utilise Amazon RDS with the WordPress instance to secure data.
- **Secure Access:** Implement a bastion host to allow secure access to the EC2 instance via SSH.
- **ALB for Secure Routing:** Use the ALB DNS as a secure route to access the EC2 instance, ensuring secure and efficient traffic routing.

These enhancements aim to improve the infrastructure by aligning with industry best practices for a robust web hosting environment.
