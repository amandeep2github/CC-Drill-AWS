# connecting two vpc using transit gw

## steps
- have two ec2 in diff vpc with cidr say 172.31.0.0/16 and 192.0.0.0/24
- in their respective security group allow ssh from other's cidr
- create a transit gw
- create transit gw attachment in each vpc
- in the route table attached to subnet create route for other's cidr with target as tgw attachment
- after that login to public ec2 and ssh to other vpc's ec2