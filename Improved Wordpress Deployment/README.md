# Improved Wordpress Deployment

## Project Overview

This project involved setting up a highly available WordPress infrastructure on AWS, in order to improve on my prevous wordpress build, making changes to increase security, availability and optimise performance. 

### Step 1: VPC Setup for High Availability

- Created a new VPC with 3 public and 3 private subnets to ensure high availability.
- Created a NAT gateway in one of the subnets only to optimise costs.

### Step 2: RDS Instance and Security Group Configuration

- Established an RDS instance in the private subnet, along with a security group to secure WordPress data.

### Step 3: Bastion Host for Secure SSH Access

- Created a Bastion Host in the public subnet to securely SSH into the EC2 instance in the private subnet.
- Configured Security Groups for both the Bastion Host and the WordPress instance.
- Aligned Security Group configurations to allow inbound traffic from Bastion SG to the WordPress instance on SSH port 22.

### Step 4: LAMP Stack and WordPress Configuration

- Provisioned a new EC2 instance and installed LAMP stack.
- Installed and configured WordPress, modifying the Database hostname to the RDS instance DNS for database connectivity.
- Utilised AWS documentation for reference during LAMP and WordPress setup.

### Step 5: Application Load Balancer Configuration

- Created an ALB to securely route internet traffic to the WordPress instance in the private subnet.
- Configured a Security Group for the ALB and established a target group listening on HTTP port 80 to direct traffic to the WordPress instance.
- Troubleshooted ALB's target group health issue, resolving it by adjusting the Security Group inbound rule to allow traffic from the ALB SG.

### Testing, Access, and Future Enhancements

- Successfully accessed WordPress on the EC2 instance using the public DNS of the ALB.
- Completed WordPress installation and conducted test posts.
- Plan for future enhancements includes using Route 53 for domain routing to the ALB and implementing ACM for HTTPS.

### Learning and Troubleshooting Experience

- Utilised AWS documentation for setup and troubleshooting.
- Faced challenges with ALB target group health due to misconfigured Security Group, resolved by adjusting the inbound rules to allow traffic from the ALB sG to the EC2 instance.

## Future Enhancements and Security

To further improve this build, I would take the following measures:

- Use Route 53 to create a domain name for user access.
- Create and apply a certificate using ACM to the ALB to enforce HTTPS traffic for enhanced security.
