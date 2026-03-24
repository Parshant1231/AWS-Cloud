# IAM Users, Groups & Policies
⬡ Create an IAM user with limited S3 access, test it, understand the principle of least privilege.

## STEPS
1. IAM → Users → Create user dev-user. Enable console access with a password.
2. Create group s3-read-group. Attach managed policy AmazonS3ReadOnlyAccess. Add user to group.
3. Log in as dev-user. Try listing S3 buckets — works. Try deleting — denied.
4. Create a custom policy (JSON) that allows only s3:GetObject on one specific bucket ARN.
5. Attach custom policy directly to user. Understand: group policy + user policy both apply (union).