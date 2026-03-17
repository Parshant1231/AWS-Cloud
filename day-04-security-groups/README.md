# How to create SG's rules 

## Steps 
1. Select name for given SG
2. Then, pick a descript & vpc for given SG
3. Add inbound & outbound rules.

# NOTE: It is like a firewall on instance level

## How SG's is different from the NACL's
- SG is statefull means If Inbound is alowed , resp traffic automatically allowedsame for outbound.
- 👉 In NACLs (stateless):
    Every request needs: Inbound rule, Outbound rule
    Otherwise traffic breaks 💥