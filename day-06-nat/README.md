# How to create nat gateway for private subnet

## Steps
1. Allocate an Elastic IP (VPC → Elastic IPs → Allocate).
2. VPC → NAT Gateways → Create in public-subnet-1a using that EIP.
3. Create route table private-rt: route 0.0.0.0/0 → NAT Gateway. Associate with private subnet.
4. Launch a second EC2 in private subnet (no public IP). SSH via your public EC2 (bastion) and run curl google.com. It works — but nobody can reach this EC2 from internet.
5. ⚠️ Delete NAT GW after testing (costs ~$0.045/hr).

## NOTE:
- Error mainly lies in outbound(not allow ssh rules by bastion) & inbound rules(not add ssh to given instance SG)