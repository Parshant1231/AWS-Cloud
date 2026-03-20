# VPC PEERING

## Steps
1. Create a second VPC: cloudgrind-vpc-2, CIDR 10.1.0.0/16 with one subnet 10.1.1.0/24.
2. VPC → Peering Connections → Create. Requester: VPC1, Accepter: VPC2. Accept the request.
3. Add route in VPC1's RT: 10.1.0.0/16 → peering connection. Do same in VPC2's RT: 10.0.0.0/16 → peering.
4. Launch EC2 in each VPC. Ping from VPC1 EC2 to VPC2 EC2's private IP.
5. Note: peering is NOT transitive. If A↔B and B↔C, A cannot reach C.

## IMP
- We can use vpc peering in 3 ways 
  1. Access from laptop -> bastion -> ping
  2. Using SSM  by using endpoints (without internet)
  3. By using one public subnet(IGW) and diretly ping to that.