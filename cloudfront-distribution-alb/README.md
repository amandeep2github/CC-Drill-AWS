# create a distribution on lab

## steps
- given you have alb 
- in cloudfront create distribution 
- first option comes of aws origin where you will see your s3, alb listed
- choose OAI (object access identities) if bucket is not public
- choose header if want to control access through cloudfront only
- you can leave price class, waf, cname, ssl default