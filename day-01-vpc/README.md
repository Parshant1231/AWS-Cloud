# How to create a VPC in AWS

## Steps
1. Add a name of the given vpc like  "cloudgrind-vpc"
2. Add cidr block like "10.0.0.0./16" (it gives you 65k IP's) 
3. Add a tags at the end 
4. Last note the VPC id to use in anywhere (mainly used in TF) (vpc-0dc632201519d1ea4)

# What DNS Resolution means? (Domain Name System)
- process of converting a human-readable domain name into a machine -readable IP address so that computer can locate servers on internet.
- DNS Resolution = Domain Name --> IP Address
+ Example: When you type google.com in browser, computer find the IP of Google's server (like 142.250.183.206).