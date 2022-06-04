# Create simplest cloudformation that will create an instance and then use mapping and parameter

## Steps
- create a .yml or json cloudformation file with Resources top element
- just define three properties of logical Instance which are az, size, image
- provide image id from mapping
- provide size from parameter

## Concepts
- an ec2 will be created in default vpc and will be assigned default security group, default volume
- parameter can be used with Ref like as any logical resources
- AWS related resources can be referrenced by AWS::Region
- top level cloudformation elements like Resources, Mappings are object maps not list so they are {} not []