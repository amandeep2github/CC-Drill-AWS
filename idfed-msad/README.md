# creating identity in msad to access workspace

- create role say Ec2DomainJoin for service ec2 with permissions AmazonSSMManagedInstanceCore and AmazonSSMDirectoryServiceAccess
- create role PowerAD with administrative access
- create sec group allowing rdp from outside or your ip
- create MSAD and wait till it comes up
- go to active directory and enable URL and enable console and check if PowerAD role showing up
- create window server ec2 with role Ec2DomainJoin and give msad domain 
- login to win ec2 with domain msad-domain\admin and pwd and check whoami
- open server manager and enable features for Remote Administrative ? Role Administrative Tools
- Open Administrative Tools > (Site and services) (domain and trusts) (users and computers)
- (users and computers) > add user to domain msad-domain
- add the same user to active directly console, PowerAD role
- go to workspaces and register active directory
- create a workspace and assign the user created in active directory to it
- download link to tool to connect to workspace, give registration code and sign in using ad user
- from directory console copy console url and type in workspace and using same ad user login



## action required to create msad
- ds:CreateMicrosoftAD, it can be denied in scp