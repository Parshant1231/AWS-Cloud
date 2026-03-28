# Terraform Variables & Outputs
⬡ Parameterize your Terraform with variables and expose outputs — the same patterns used in modules.


## STEPS
1. Create variables.tf with vpc_cidr, env, region variables.
2. Reference them in main.tf as var.vpc_cidr.
3. Create outputs.tf — output the VPC ID and subnet IDs.
4. Create terraform.tfvars with values. Apply.
5. This mirrors what you built in your Terraform nested modules project. Every resource should be parameterized.