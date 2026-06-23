# AWS VPC - Public and Private Subnet Lab

## Objective

Create a custom AWS VPC with Public and Private Subnets to understand network segmentation and secure cloud architecture.

---

## Architecture

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

---

## Services Used

- Amazon VPC
- Amazon EC2
- Internet Gateway
- Route Tables
- Subnets
- Security Groups

---

## Steps Performed

1. Created a custom VPC (10.0.0.0/16)
2. Created Public Subnet (10.0.1.0/24)
3. Created Private Subnet (10.0.2.0/24)
4. Created and attached Internet Gateway
5. Created Public Route Table
6. Added route 0.0.0.0/0 → Internet Gateway
7. Associated Public Subnet with Public Route Table
8. Launched Public EC2 Instance
9. Verified internet connectivity using ping google.com
10. Launched Private EC2 Instance without Public IP
11. Verified Private EC2 is isolated from the internet

---

## Validation

### Public EC2

- Public IP assigned
- Internet access available
- Successfully pinged external hosts

### Private EC2

- No Public IP assigned
- Not reachable from the internet
- Isolated inside the VPC

---

## Key Learning

This lab demonstrates how AWS networking works using Public and Private Subnets.

- Public resources can access the internet through an Internet Gateway.
- Private resources remain protected from direct internet access.
- Network segmentation improves security.
- This architecture is commonly used in production environments.

---

## Outcome

Successfully implemented a secure AWS VPC architecture with:

- Custom VPC
- Public Subnet
- Private Subnet
- Internet Gateway
- Route Table
- Public EC2
- Private EC2

Validated internet connectivity for Public EC2 and network isolation for Private EC2.
