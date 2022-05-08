# Create website using s3 with name example.com

## Given
- You have domain example.com on godaddy


## Steps
- go to s3 make a bucket with name example.com
- in properties make it static website
- in permission unblock public access
- give bucket policy 
- In route 53 create a hosted zone with name example.com
- take name server records, four in this case and update go daddy's DNS service (may require customer service professional)
- in hosted zone create A record for your domain and choose s3 url 

## Concepts
### aws
- every principal * need "s3:GetObject" on all objects of target bucket example.com/*