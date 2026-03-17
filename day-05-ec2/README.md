# How to create EC2 instance

## Steps
1. EC2 → Launch Instance. AMI: Ubuntu Linux 2023. Type: t3.micro.
2. Network: cloudgrind-vpc, Subnet: public-subnet-1a. Create new key pair, download it.
3. Attach web-sg. Launch

## Note: 
- maximum cases your IP changes and you cant do ssh so update the SG from security group section.