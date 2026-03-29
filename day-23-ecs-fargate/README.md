# ECR + ECS Fargate
⬡ Push a Docker image to ECR, run it serverlessly on ECS Fargate — no EC2 to manage.

## STEPS
1. Create simple Node.js app → Dockerfile → build image locally (or use Day 9 nginx).
2. ECR → Create repository cloudgrind-app. Follow push commands to tag & push image.
3. ECS → Create cluster (Fargate). Task definition: use your ECR image, 256 CPU, 512 MB RAM.
4. Create service: 1 desired task, attach to your VPC/subnets/web-sg.
5. Access via public IP in task details. This is how QuantumSafe Messenger and DevDeploy containers run.
