# How to create IGW & Route Table

## Steps
1. Create a internet gateway from the igw by using given vpc.
2. Then, create a route table with the given route.
3. Add a route dest: "0.0.0.0/0".
4. Do subnet association with given route table 

## NOTE
- Subnet Assoc is enabling the route to the given subnet (most likely public-sb)  