# Setup management account and invite/add other accounts

- in root account create organization
- invite other account which need to be managed
- invitation will be sent to that account
- upon acceptance that account becomes part of organization
- from admin user of root account setup cross account access to managee account
- in managee account create role say OrganizationAccountAccessRole and give AdministratorAccess
- add trusted policy to trust manager account to assume this role
- in manager account for admin user add policy to let it assumeRole OrganizationAccountAccessRole in managee account
- manager account need this additional policy inspite of AdministratorAccess because the role as a resource is in separate account
- now try switching to this account
- please note using console you can't switch if there is external id
- also if you create account instead of invite account above role and policy steps are executed by aws
- please note the SCP (service control policy) doesn't apply on users in management account



[Refer link](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_access.html#orgs_manage_accounts_create-cross-account-role)