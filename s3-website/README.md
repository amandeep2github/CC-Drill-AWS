# Create website using s3 with name example.com

## Given
- You have domain example.com on godaddy


## Steps
- go to s3 make a bucket with name example.com
- in properties make it static website
- in permission unblock public access
- give bucket policy 
```
"Sid": "PublicReadGetObject",
"Effect": "Allow",
"Principal": "*",
"Action": "s3:GetObject",
"Resource":"arn:aws::example.com/*"
```
- In route 53 create a hosted with name example.com
- take name server records, four in this case and update go daddy's DNS service (may require customer service professional)
- in hosted zone create A record for your domain and choose s3 url 