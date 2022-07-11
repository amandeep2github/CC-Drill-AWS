# how ec2 in pvt subnet can access s3

## Steps
- create ec2 in public subnet with ssh enabled in sg from outside
- create ec2 in private subnet with ssh enabled in sg from sg of above
- in vpc section create endpoint and in type search s3 and choose com.amazonaws.<region>.s3 of type gateway
- attach the endpoint to route table of private subnet, it will also create a route in route table of sn
- in the route table, copy the destination value 
- in sg of private ec2, create outbound rule for https with destination above copied value