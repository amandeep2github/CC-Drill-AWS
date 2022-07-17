# Using SSO with MSAD as identity provider (this depends on idfed-msad)

- open SSO console and enable
- give identity provider as msad (default its SSO) itself
- (sso can work with many identity providers msad, ad connector, apps supporting saml 2.0)
- it should show organiation heirarchy
- enable permissions for say role Data Scientist for another aws account say cs gmail
- In accounts, add user that was created in AD and assign that role to the user
- now take the sso url form directory service console and put in workspace browser
- it will list all apps supporting SSO and console should be an option, click and connect


