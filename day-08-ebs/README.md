# EBS Volumes & Snapshots

## Steps
1. EC2 → Volumes → Create 10GB gp3 volume in same AZ as your EC2. Attach to instance as /dev/xvdf.
2. SSH → lsblk to see it → sudo mkfs.ext4 /dev/xvdf → mount to /data.
3. Write a file: echo 'cloudgrind' > /data/test.txt.
4. Create snapshot of this volume. Then create new volume from snapshot. Attach & mount — your file is there.