# IAM Roles for EC2
⬡ Assign an IAM role to EC2 so it can access S3 and DynamoDB without any access keys.

## STEPS
1. IAM → Roles → Create role. Trusted entity: EC2. Attach AmazonS3ReadOnlyAccess.
2. EC2 → Select your instance → Actions → Security → Modify IAM role → Attach new role.
3. SSH into instance. Run: aws s3 ls — works without any credentials configured.
4. This is how production apps access AWS services — NEVER hardcode access keys in code.
5. Check IMDS: curl http://169.254.169.254/latest/meta-data/iam/security-credentials/ROLE_NAME — see temp creds.