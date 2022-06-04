# make a lambda with cw logs with testability

## Steps
- make a node.js file with async function with one parameter event and simple console logs
- make a zip of the content, please note, get inside your project dir and compress
- create a new function, choose basic role creation for lambda with trusted entity Lambda
- upload the code 
- test the function

## Concepts
### nodejs
- any async js method exported with the name handler can be lambda function
> module.exports.handler = async (event)

### aws
- permission of role for lambda that is tested to log event need permission on logs service


### js
- async function return promise and can use await inside
