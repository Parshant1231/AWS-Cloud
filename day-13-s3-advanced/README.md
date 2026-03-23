# S3 Lifecycle & Cross-Region Replication
⬡ Automate S3 cost management with lifecycle rules and replicate data to another region for durability.
## STEPS
1. On your Day 9 bucket: Management → Lifecycle Rules → Create rule.
2. Transition objects to S3-IA after 30 days, Glacier after 90 days, delete after 365 days.
3. Enable versioning (required for replication). Create a destination bucket in ap-southeast-1.
4. S3 → Management → Replication → Add rule: replicate all objects to destination bucket.
5. Upload a file. Check destination bucket — it appears there within minutes.