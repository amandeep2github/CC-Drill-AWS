# make two ec2 ping each other in same account

## Steps
- one ec2 is in public subnet and allows ssh on 22 from outside
- create a peering connection from requester vpc 172.31.0.0/16 to accepter vpc 192.0.0.0/24, accept it
- in request vpc create a security group allowing ssh outbound to 192.0.0.0/24
- attach this sec group to instance in requester vpc
- in requester vpc, add a route to 192.0.0.0 with target as vpc peering and choose newly created peering connection
- in accepter vpc, create a security group allowing ssh inbound from 172.31.0.0/16
- in accepter vpc, add a route to 172.31.0.0/16 with target as vpc peering and choose newly created peering connection


## Concepts
- communication happens over private ips
- no network device so no single point of failure

## appendix

| Destination  | Target |
| :-----------:  | :------: |
| 172.31.0.0/16|pcx-08b97a7a9f972d20b|