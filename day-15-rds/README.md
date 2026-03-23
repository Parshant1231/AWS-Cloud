# RDS PostgreSQL Setup
⬡ Launch a managed PostgreSQL RDS instance in a private subnet, connect from EC2, create tables.

## STEPS

1. RDS → Create DB. Engine: PostgreSQL 15. Template: Free Tier. Identifier: cloudgrind-db.
2. VPC: cloudgrind-vpc. Subnet group: create new with your private subnets. Attach db-sg.
3. From your public EC2: sudo yum install postgresql15 -y. Connect: psql -h RDS_ENDPOINT -U postgres -d postgres.
4. Create a table: CREATE TABLE tasks (id SERIAL, name TEXT, done BOOLEAN);. Insert a row.
5. Multi-AZ: understand it creates a standby in another AZ for failover.