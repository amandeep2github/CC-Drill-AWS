# make a lambda with cw logs with testability

## Steps
- make a node.js program with simple console logs
- create a new function, choose basic role creation for lambda with trusted entity Lambda
- make a zip of the content, please note, get inside your project dir and compress
- upload the code 
- test the function

## Concepts
### nodejs
- any async js method exported with the name handler can be lambda function
> module.exports.handler = async (event)

### aws
- permission of role for lambda that is tested to log event need permission on logs service
> "Action": "logs:CreateLogGroup",
> "Resource": "arn:aws:logs:us-east-1:142456454879:*"
> "logs:CreateLogStream", "logs:PutLogEvents"
> "arn:aws:logs:us-east-1:142456454879:log-group:/aws/lambda/nodeSimple:*"

### js
- async function return promise and can use await inside
