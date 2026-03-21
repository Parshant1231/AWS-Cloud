# AMI & Launch Template
⬡ Create a custom AMI from your configured EC2, then use a Launch Template to reproducibly launch identical instances.

## STEPS
1. On your running EC2: install nginx → sudo yum install nginx -y && sudo systemctl start nginx.
2. EC2 → Actions → Image and Templates → Create Image. Name it cloudgrind-nginx-ami.
3. After AMI is ready: EC2 → Launch Templates → Create with your new AMI, instance type t2.micro, web-sg.
4. Launch from template. The new instance will have nginx pre-installed — no setup needed.
5. This is the foundation of Auto Scaling.


## NOTE
- Ensure that you pick the right sg which resides in the same vpc as the network of given template.