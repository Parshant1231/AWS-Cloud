# Application Load Balancer
⬡ Put an ALB in front of your ASG. Traffic should be distributed across instances and health-checked.

## STEPS
1. EC2 → Load Balancers → Create Application LB. Internet-facing, public subnets.
2. Create Target Group: type Instance, protocol HTTP port 80. Health check path /.
3. Register your running EC2s as targets.
4. Listener rule: forward port 80 to your target group.
5. Hit the ALB DNS name in browser. Terminate one EC2 — ALB stops sending traffic to it automatically.
