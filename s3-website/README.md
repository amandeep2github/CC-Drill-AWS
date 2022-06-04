# Create website using s3 with name example.com

## Given
- You have domain example.com on godaddy


## Steps
- go to s3 make a bucket with name example.com
- in properties make it static website
- in permission unblock public access
- give bucket policy 
<<<<<<< HEAD
```
"Sid": "PublicReadGetObject",
"Effect": "Allow",
"Principal": "*",
"Action": "s3:GetObject",
"Resource":"arn:aws::example.com/*"
```
- In route 53 create a hosted zone with name example.com
- take name server records, four in this case and update go daddy's DNS service (may require customer service professional)
- create 'A' record pointing to s3-website.<region>.amazonaws.com (please note bucker name will come from hosted zone)
=======
- In route 53 create a hosted zone with name example.com
- take name server records, four in this case and update go daddy's DNS service (may require customer service professional)
- in hosted zone create A record for your domain and choose s3 url 

## Concepts
### aws
- every principal * need "s3:GetObject" on all objects of target bucket example.com/*
>>>>>>> 837fb8c699e4e4c572ec2f6708e171f2b4b58681
