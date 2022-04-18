# Create subdomain in r53 pointing to LB with two ec2 with ASG

## Steps
- keep user-date in s3 bucket for ec2 to copy and run on index.txt file
- have an instance profile role to read from s3
- have vpc and public subnet
- have sec group for ssh on 22 and All traffic
- keep key pair ready 
- create instance using above 
- On instance run yum update and install httpd and copy web content /var/www/html
- also check file /etc/init.d/httpd is there
- hit ec2 public ip from browse to make sure index.html file shows
- create ALB in same vpc and in same az where ec2 are running (this is essential)
- choose subnet which is public and choose sec group which allow trafic from internet
- make target group for instance which is running
- give TG in ALB
- hit ALB from browser