# Create subdomain in r53 pointing to LB with two ec2 with ASG

## Steps
- keep user-date in s3 bucket for ec2 to copy and run on index.txt file
- have an instance profile role to read from s3
- have vpc and public subnet
- have sec group for ssh on 22 and http IP4
- keep key pair ready 
- create instance using above, chose ami of Amz or REHL and instance t3.micro
- On instance run yum update and install httpd and copy web content /var/www/html
- also check file /etc/init.d/httpd is there
- hit ec2 public ip from browse to make sure index.html file shows
- create ALB in same vpc and in same az where ec2 are running (this is essential)
- choose subnet which is public and choose sec group which allow trafic from internet
- make target group for instance which is running
- give TG in ALB
- hit ALB from browser
- Now create a Lauch configuration for ec2 above so that you can reuse ec2 creation config
- Give it to an ASG, there is option in LC to attach that to ASG
- In ASG you can give ALB as well
- test your ALB using browser
- Now in route 53 create a simple record say web.conducive.in of A type point that to ALB using simple routing
- Hit the url web.conducive.in



Please note if aws or unzip not installed
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
yum install unzip -y
unzip awscliv2.zip
./aws/install
```

For any problem in user-data section, look at following places
```
/var/lib/cloud/instances/<instance-id>/user-data.txt
/var/log/cloud-init*.log
/etc/init.d/httpd
/var/www/html
```