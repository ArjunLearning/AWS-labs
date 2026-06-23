VPC Public and Private Subnet Lab
Objective

Create a custom AWS VPC with Public and Private Subnets to understand network segmentation and secure cloud architecture.

Architecture
Internet
    |
Internet Gateway
    |
Public Route Table
    |
Public Subnet (10.0.1.0/24)
    |
Public EC2
    |
-------------------------
    |
Private Subnet (10.0.2.0/24)
    |
Private EC2
Services Used
Amazon VPC
Amazon EC2
Internet Gateway
Route Tables
Subnets
Security Groups
Steps Performed
Created custom VPC (10.0.0.0/16)
Created Public Subnet (10.0.1.0/24)
Created Private Subnet (10.0.2.0/24)
Created and attached Internet Gateway
Created Public Route Table
Added route:
0.0.0.0/0 -> Internet Gateway
Associated Public Subnet with Public Route Table
Launched Public EC2 Instance
Verified internet connectivity using:
ping google.com
curl ifconfig.me
Launched Private EC2 Instance without Public IP
Verified Private EC2 is not accessible from the internet
Validation
Public EC2
Public IP assigned
Internet access available
Successfully pinged external hosts
Private EC2
No Public IP assigned
Not reachable from the internet
Remains isolated inside the VPC
Key Learning

This lab demonstrates how AWS VPC networking works using Public and Private Subnets.

Public resources can access the internet through an Internet Gateway.
Private resources remain protected from direct internet access.
Network segmentation improves security and follows real-world production architecture.
Outcome

Successfully implemented a secure AWS VPC architecture with Public and Private Subnets, Internet Gateway, Route Tables, and EC2 instances while validating internet access and network isolation.
