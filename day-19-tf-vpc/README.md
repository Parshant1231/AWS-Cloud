# Terraform: Provider & First Resource
⬡ Everything you built by hand this month — now build it with code. Start Terraform: provider, state, and a VPC.

## STEPS
1. main.tf: configure aws provider, region ap-south-1. terraform init.
2. Write aws_vpc resource with cidr 10.0.0.0/16. terraform plan — read the diff.
3. terraform apply. Check AWS console — VPC created. Check terraform.tfstate.
4. Change CIDR, run plan — Terraform shows destroy+recreate. This is immutable infra.
5. Add aws_subnet resource referencing aws_vpc.main.id. Apply.
