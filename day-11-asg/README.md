# Auto Scaling Group
⬡ Create an ASG using your launch template. Set min/max/desired. Trigger a scale-out event.

## STEPS
1. EC2 → Auto Scaling Groups → Create. Use your launch template from Day 10.
2. VPC: cloudgrind-vpc. Subnets: public-subnet-1a. Min:1, Max:3, Desired:1.
3. Add a scaling policy: Target Tracking on CPUUtilization at 50%.
4. SSH into the running instance. Stress CPU: sudo yum install stress -y && stress --cpu 4 --timeout 120.
5. Watch ASG launch a second instance automatically. After 10 mins, it scales back in.
