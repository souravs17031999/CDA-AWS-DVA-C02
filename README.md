# CDA-AWS-DVA-C02
AWS Certified Developer - Associate

# Development with AWS Services

# Security

## IAM 
- AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources.
- You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.
- IAM doesn't requires region selection (global)
- IAM, like many other AWS services, is eventually consistent. IAM achieves high availability by replicating data across multiple servers within Amazon's data centers around the world. If a request to change some data is successful, the change is committed and safely stored. However, the change must be replicated across IAM, which can take some time.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d00d9c94-18c8-4919-9cc0-d77e48b3a4e4)  

- When principal makes a request to AWS for authn and authz, AWS gathers the request information into a request context, which is used to evaluate and authorize the request.
- AWS checks each policy that applies to the context of your request. If a single permissions policy includes a denied action, AWS denies the entire request and stops evaluating. This is called an explicit deny. Because requests are denied by default, AWS authorizes your request only if every part of your request is allowed by the applicable permissions policies.
- IAM users are granted long-term credentials to your AWS resources. In contrast, users in AWS IAM Identity Center (successor to AWS Single Sign-On) are granted short-term credentials to your AWS resources.
- User Federation in usecases like:
  - Your users already exist in a corporate directory: Corporate directory, Microsoft Azure AD, external IDP's like Okta etc..
  - Your users already have Internet identities: Internet identity provider like Login with Amazon, Facebook, Google, or any OpenID Connect (OIDC) compatible identity provider
 
**ACCESS CONTROL METHODS/WAYS:**
- Single sign-on access for human users
- Federated access for human users,
- Cross-account access between AWS accounts
- Long-term credentials for designated IAM users in your AWS account

#######################```TASKS REQUIRING ROOT USER CREDENTIALS```#######################   
- Change your account settings. This includes the account name, email address, root user password, and root user access keys. 
- Restore IAM user permissions. If the only IAM administrator accidentally revokes their own permissions, you can sign in as the root user to edit policies and restore those permissions.
- Activate IAM access to the Billing and Cost Management console.
- View certain tax invoices. An IAM user with the aws-portal:ViewBilling permission can view and download VAT invoices from AWS Europe, but not AWS Inc. or Amazon Internet Services Private Limited (AISPL).
- Close your AWS account.
- Register as a seller in the Reserved Instance Marketplace.
- Configure an Amazon S3 bucket to enable MFA (multi-factor authentication).
- Edit or delete an Amazon Simple Queue Service (Amazon SQS) resource policy that denies all principals.
- Edit or delete an Amazon Simple Storage Service (Amazon S3) bucket policy that denies all principals.
- Sign up for AWS GovCloud (US).
- Request AWS GovCloud (US) account root user access keys from AWS Support.


#######################```IAM USER```#######################    

- An IAM user is an identity within your AWS account that has specific permissions for a single person or application
- An IAM group is an identity that specifies a collection of IAM users. You can't sign in as a group. You can use groups to specify permissions for multiple users at a time. 
- Every User can be either alone or put into a group  i.e. policies can be individually assigned to IAM user (single) or to a group.

**While creating IAM User Two options ->** 
- Specify a user in Identity Center - Recommended
We recommend that you use Identity Center to provide console access to a person. With Identity Center, you can centrally manage user access to their AWS accounts and cloud applications.
- I want to create an IAM user
We recommend that you create IAM users only if you need to enable programmatic access through access keys, service-specific credentials for AWS CodeCommit or Amazon Keyspaces, or a backup credential for emergency account access.
- Control maximum permissions using IAM boundary:
  - An entity's permissions boundary allows it to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries.
  - The permissions boundary for an IAM entity (user or role) sets the maximum permissions that the entity can have.
  - If any one of these policy types explicitly denies access for an operation, then the request is denied. 

- Administrative access to IAM user group (group name is admin here)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3bb8415f-823f-4726-88ab-a28640aa1494)

- Now, this user can also have its own alias set after which its own custom URL will be generated for Logon.

#######################```IAM POLICIES```#######################  

**Identity-based and resource-based policies**
- Identity-based policies are permissions policies that you attach to an IAM identity, such as an IAM user, group, or role.
  - AWS Managed policies, Customer managed policies, Inline policies 
- Resource-based policies are permissions policies that you attach to a resource such as an Amazon S3 bucket or an IAM role trust policy.
  - Resource-based policies are inline policies, and there are no managed resource-based policies.
  - The IAM service supports only one type of resource-based policy called a role trust policy, which is attached to an IAM role.
  - Trust policies define which principal entities (accounts, users, roles, and federated users) can assume the role. 

- For ex. in below, identity based policies given to users defines what actions can they perform on specific resources whereas resource based policies defines which principals (users) have access to them.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0386d74c-f8b0-49bb-acba-25eff9c5b4ed)   
- For requests made from one account to another, the requester in Account A must have an identity-based policy that allows them to make a request to the resource in Account B. Also, the resource-based policy in Account B must allow the requester in Account A to access the resource. There must be policies in both accounts that allow the operation, otherwise the request fails.
- In addition, Amazon S3 supports a permission mechanism known as an access control list (ACL) that is independent of IAM policies and permissions. You can use IAM policies in combination with Amazon S3 ACLs.
- ACL(ACCESS CONTROL LIST):
  - enable you to manage access to buckets and objects.
  - When you create a bucket or an object, Amazon S3 creates a default ACL that grants the resource owner full control over the resource.
  - ![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b71a231f-6e5c-42bf-94ea-9b97407af266)  


**AWS MANAGED POLICY VS CUSTOMER MANAGED POLICY**
- Managed policies that are created and managed by AWS (AWS MANAGED POLICIES)
- AWS managed policies make it convenient for you to assign appropriate permissions to users, groups, and roles. It is faster than writing the policies yourself
- Managed policies that you create and manage in your AWS account.
- You cannot change the permissions defined in AWS managed policies. AWS occasionally updates the permissions defined in an AWS managed policy.   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/baa8855f-4321-4b05-accf-cce7167c558e)   

  
- Customer managed policies provide more precise control over your policies than AWS managed policies. You can create, edit, and validate an IAM policy in the visual editor or by creating the JSON policy document directly.   

- IAM Policy inheritance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/99800cc5-9184-4095-8b2a-59fbc71f949a)   

- IAM policy structure and meaning of JSON documents   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0f61aa3e-c15e-4a73-9fb4-1384479a7b99)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d6d1ddbe-8947-4970-8cac-bc28f0bdc7e7)   


- IAM policy can be created using policy visual editor   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/93b8242a-d731-4f5b-93be-fcb97829e8ae)  

- Overall for ex. Below shows User which has policies attached via different mechanisms   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6e7a6b17-7588-47f3-a35d-62036962c697)   

#######################```PASSWORD POLICY IAM```#######################   
- IAM password policy can be managed and user can be required to change their password at certain time or their first logon etc...   
- Password policy can be either chosen as AWS default or it can be new custom policy as defined by admin user.    

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9f082128-6eeb-4f96-9a0f-cce471281413)   


#######################```MFA```#######################   
- Multi factor authentication
- Types of MFA devices
  - Virtual MFA device (google authenticator, Authy)
  - Universal 2nd Factor U2F key ex. YubiKey by Yubico (3rd party)
  - Hardware Key Fob MFA device (Gemalto 3rd party)
  - Hardware Key Fob MFA device for AWS GovCloud (surePassID 3rd party)

- You can register up to 8 MFA devices of any combination with your AWS account root and IAM user.   
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b91a99e8-877b-4efc-9e10-fcf5c34a2485)   

#######################```LOGON WITH ACCESS KEYS```#######################  
- ACCESS KEY ID (USERNAME)
- SECRET ACCESS KEYS (PASSWORD)

- According to purpose of access keys, AWS recommends multiple options like AWS CLI V2, CLOUDSHELL ETC...

#######################```IAM ROLES```#######################  

- A role is an IAM identity that you can create in your account that has specific permissions.
- However, instead of being uniquely associated with one person, a role can be assumed by anyone who needs it. A role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.
- Roles are meant to be depending on various use cases, for ex. Assigned directly to the aws services instead of users.
- Few examples shown below:    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fd2b5ed5-4f5e-4d72-a72d-4e43466e1969)
- When you create a role, you create two policies:
  - A role ```trust policy``` that specifies who can assume the role and a ```permissions policy``` that specifies what can be done with the role.
  - You specify the trusted principal who is allowed to assume the role in the role trust policy.  
- For ex. Role creation for EC2 instance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1234becc-443e-4fa5-a067-837e098ff897)
- Role chaining:
  - Role chaining is when you use a role to assume a second role through the AWS CLI
  - AWS does not treat using roles to grant permissions to applications that run on EC2 instances as role chaining.

**SCENARIOS FOR ROLES**
- Providing access to an IAM user in another AWS account that you own  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8e074f0b-8f9f-4608-abe9-2444c2861c72)
- Providing access for non AWS workloads
- Providing access to AWS accounts owned by third parties
- Providing access to an AWS service
- Providing access to externally authenticated users (identity federation)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0e8a366e-3b74-4e7d-a880-fd828d6e7b7d)   

**Using IAM Roles**
- AWS Management Console (by switching roles)
- assume-role CLI or AssumeRole API operation
- assume-role-with-saml CLI or AssumeRoleWithSAML API operation
- assume-role-with-web-identity CLI or AssumeRoleWithWebIdentity API operation
- Console URL constructed with AssumeRole, AssumeRoleWithSAML, AssumeRoleWithWebIdentity (broker constructs the URL and calls STS for assuming the roles)

**The confused deputy problem**
- The confused deputy problem is a security issue where an entity that doesn't have permission to perform an action can coerce a more-privileged entity to perform the action.
- Prevention: ```aws:SourceArn``` and ```aws:SourceAccount``` global condition context keys in resource-based policies to limit the permissions that a service has to a specific resource.

#######################```IAM POLICY SIMULATOR```#######################  
- One can choose and evaluate the roles and policies attached in real time using this simulator.   
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/11dbc126-c328-4225-bf62-d2d25ff816e2)   


#######################```ABAC```#######################   
- Attribute-based access control (ABAC) is an authorization strategy that defines permissions based on attributes. In AWS, these attributes are called tags. You can attach tags to IAM resources, including IAM entities (users or roles) and to AWS resources.
- These ABAC policies can be designed to allow operations when the principal's tag matches the resource tag.
- ABAC is helpful in environments that are growing rapidly and helps with situations where policy management becomes cumbersome.
- The disadvantage to using the traditional RBAC model is that when employees add new resources, you must update policies to allow access to those resources.
- RBAC
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6c593575-9a2e-4482-ae0f-34c1fc501c34)    
- ABAC
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5e0c31ef-ddb0-49ad-a38e-d4dbf3e45751)  

#######################```SECURITY TOKEN SERVICE (STS)```#######################   
- You can use the AWS Security Token Service (AWS STS) to create and provide trusted users with temporary security credentials that can control access to your AWS resources.
- Temporary security credentials are not stored with the user but are generated dynamically and provided to the user when requested.
- By default, AWS STS is a global service with a single endpoint at https://sts.amazonaws.com. However, you can also choose to make AWS STS API calls to endpoints in any other supported Region.
- This is used in Identity federation usecases, cross account accesses
- The AWS STS API operations create a new session with temporary security credentials that include an access key pair and a session token. The access key pair consists of an access key ID and a secret key. Users (or an application that the user runs) can use these credentials to access your resources.
- TO Have user call STS, User should be assigned in-line policy with STS assumeRole (depending on usecase there are 3 options)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/868fa142-b2d2-4622-be23-8d488f888c20)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1f78aa93-d980-4860-9bf7-ebada1995d94)   

- Bearer tokens:
  - AWS STS can help in getting bearer tokens which are required for accessing some services programmatically. For ex. AWS CodeArtifact etc..
  - The token's access key ID begins with the ABIA prefix (can help in cloudtrail logs)
  - The bearer token can be used only for calls to the service that generates it and in the Region where it was generated.
- All the STS calls can be traced by cloudtrail logs for ex. as shown below :  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e8e7e18e-1c0b-49a6-9434-2992c60c5f1d)   
- Calls made from another account to access cross-account services which assumes a role : ```sts:SourceIdentity``` condition key in the role trust policy to require users to specify an identity when they assume a role. For ex. shown below :   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/14be993f-ac99-44ae-b237-9ee065e1fbd9)   
Now, For this same request one entry will be there in the another account (assumed role account log).
- When performing role chaining, tags are passed on from first assumed role as "transitive tags" as shown below:
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/50429340-5926-463b-9e80-607fd2813c05)
- Web Identity provider - includes the tags passed through identity provider as shown below :
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3614606a-409c-4215-b014-8878362a6cc8)  
- Sign-in events are logged as well except the incorrect username whose information is then masked with ```HIDDEN_DUE_TO_SECURITY_REASONS```    
EXAMPLES OF STS API's :
- AssumeRole, AssumeRoleWithSAML, AssumeRoleWithWebIdentity, GetFederationToken, GetSessionToken
- The permissions policy of the role that is being assumed determines the permissions for the temporary security credentials that are returned by AssumeRole, AssumeRoleWithSAML, and AssumeRoleWithWebIdentity
- Optionally, one can pass inline or managed session policies as parameters which filters only the passed permissions returned.

#######################```IAM SECURITY TOOLS```#######################   
- IAM CREDENTIALS REPORT (ACCOUNT LEVEL)
  - report that lists all your account users and the status of their various credentials
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dc27d454-ad21-44b4-981e-b575d4911462)    

- IAM ACCESS ADVISOR (USER LEVEL)
  - shows service permissions granted to a user and when were they last accessed
  - you can use this information to revise the policies, can help in reducing the permissions for least privelege.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d79b24a5-b708-4890-96bf-2fc1596b97ba)     

#######################```IAM BEST PRACTICES```#######################   
- DONT'T user ever root user except for AWS account setup
- One physical user = AWS IAM user  
- Assign users to groups and assign permissions to groups
- create a strong password policy
- use and enforce MFA
- create and use Roles for giving permissions to AWS services
- Use Access keys for Programmatic access (CLI/SDK)  
- Audit permission of your account using IAM creds report and access advisor   
- Never share IAM user and access keys

#######################```AWS SHARED RESPONSIBILITY MODEL FOR IAM```#######################    
- AWS
  - INFRASTRUCTURE OF GLOBAL NETWORK SECURITY
  - CONFIGURATION AND VULN ANALYSIS
  - COMPLIANCE VALIDATION
 
- YOU
  - USERS, GROUPS, ROLES AND POLICIES MANAGEMENT AND MONITORING
  - ENABLE MFA ON ALL ACCOUNTS
  - ROTATE ALL YOUR KEYS OFTEN
  - USE IAM ROOLS TO APPLY APPROPRIATE PERMISSIONS
  - ANALYZE ACCESS PATTERNS AND REVIEW PERMISSIONS

#######################``` Identity providers and federation ```#######################      

- In case users are already managed outside of AWS like in corporate directory or any other identity providers, you can use IAM identity providers instead of creating IAM users in your AWS account. Ex. well-known IdP, such as Login with Amazon, Facebook, or Google.
- IAM supports IdPs that are compatible with OpenID Connect (OIDC) or SAML 2.0 (Security Assertion Markup Language 2.0)   

**OIDC**   
- OpenID Connect is an interoperable authentication protocol based on the OAuth 2.0 framework of specifications (IETF RFC 6749 and 6750). It simplifies the way to verify the identity of users based on the authentication performed by an Authorization Server and to obtain user profile information in an interoperable and REST-like manner.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/a286a5c3-fdd3-40d0-8f9f-78a390feae8a)   

**SAML**  
- Security Assertion Markup Language is an open standard for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider using SOAP over HTTP.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d5d4f3d3-acf4-4a65-a725-157c1590c42f)     
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/583d89be-6d08-4abe-9ad6-fe9580bf8251)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f1309a89-a805-4b6d-bab9-3f919236a144)     
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f639a8f3-3a0c-4d10-b7fe-0936e3776d82)
- A SAML Request, also known as an authentication request, is generated by the Service Provider to "request" an authentication.
- A SAML Response is generated by the Identity Provider. It contains the actual assertion of the authenticated user. In addition, a SAML Response may contain additional information, such as user profile information and group/role information, depending on what the Service Provider can support.
- The Service Provider never directly interacts with the Identity Provider. A browser acts as the agent to carry out all the redirections.

- The preferred way to use web identity federation is to use Amazon Cognito.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6c922032-fbad-4d27-be1f-17698bc16f4a)  
- Using SAML-based federation for API access to AWS
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/2119d497-dee5-4be7-9fc7-2d0e35e6b398)    

-------------------------   
- IAM OIDC identity providers are entities in IAM that describe an external identity provider (IdP) service that supports the OpenID Connect (OIDC) standard, such as Google or Salesforce. You use an IAM OIDC identity provider when you want to establish trust between an OIDC-compatible IdP and your AWS account.
- If you are using an OIDC identity provider from either Google, Facebook, or Amazon Cognito, do not create a separate IAM identity provider using this procedure. These OIDC identity providers are already built-in to AWS and are available for your use.    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9bec80a7-c6a4-46b5-84da-711d986aa372)

- Assigning roles to federated identity :
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/86ae1fb5-a4b3-4bab-be80-e234341be7b9)     

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/780e6c3b-70c1-4317-86ea-950b5c1fac33)  

Note: 
- Github OIDC provider: Best practice is to limit the to a specific GitHub organization, repository, or branch using the conditions section defined in the permission policies.

- For trusting the external IDP, you must supply a thumbprint. IAM requires the thumbprint for the top intermediate certificate authority (CA) that signed the certificate used by the external identity provider (IdP).   

- SAML OIDC identity provider configuration requires metadata document to be uploaded. This document includes the issuer's name, expiration information, and keys that can be used to validate the SAML authentication response (assertions) that are received from the IdP.   
- After you have verified a user's identity in your organization, the external identity provider (IdP) sends an authentication response to the AWS SAML endpoint at https://region-code.signin.aws.amazon.com/saml


- Custom IDP broker: You can write and run code to create a URL that lets users who sign in to your organization's network securely access the AWS Management Console. The URL includes a sign-in token that you get from AWS and that authenticates the user to AWS.

#######################``` Tagging IAM resources ```#######################      
- A tag is a custom attribute label that you can assign to an AWS resource. Each tag has two parts: A tag key, An optional field known as a tag value
- Names for AWS tags are case sensitive so ensure that they are used consistently. 

**When to use IAM policies vs S3 policies**
- If question is What can this user do in AWS? -> choose IAM policies 
- If question is Who can access this S3 bucket?? -> choose S3 bucket policies

#######################``` DIRECTORY SERVICES ```#######################      
**LDAP**
- Lightweight Directory Access Protocol (LDAP) is a vendor-neutral software protocol used to lookup information or devices within a network
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d56cb79e-f31f-4ab3-adad-fb3bafbc9563)
- users will go through one of two possible user authentication methods: simple authentication, like SSO with login credentials, or SASL authentication, which binds the LDAP server to a program like Kerberos.


**ACTIVE DIRECTORY, AWS DIRECTORY SERVICES**
- LDAP is the core protocol used in–but not exclusive to–Microsoft’s Active Directory (AD) directory service, a large directory service database that contains information spanning every user account in a network
- ADDS: Active Directory stores information about objects on the network and makes this information easy for administrators and users to find and use.
- ADFS: Active Directory Federation Service (AD FS) enables Federated Identity and Access Management by securely sharing digital identity and entitlements rights across security and enterprise boundaries. AD FS extends the ability to use single sign-on functionality that is available within a single security or enterprise boundary to Internet-facing applications to enable customers, partners, and suppliers a streamlined user experience while accessing the web-based applications of an organization.
- Four options in AWS:
  - AWS MANAGED AD: AWS Directory Service for Microsoft Active Directory is powered by an actual Microsoft Windows Server Active Directory (AD), managed by AWS in the AWS Cloud.
  - AD Connector: AD Connector is a proxy service that provides an easy way to connect compatible AWS applications. When you add users to AWS applications such as Amazon QuickSight, AD Connector reads your existing Active Directory to create lists of users and groups to select from
  - Simple AD is a Microsoft Active Directory–compatible directory from AWS Directory Service that is powered by Samba 4.
  - Amazon Cognito is a user directory that adds sign-up and sign-in to your mobile app or web application using Amazon Cognito User Pools.

#######################``` IAM IDENTITY CENTER ```#######################    

- IAM Identity Center provides one place where you can create or connect workforce users and centrally manage their access across all their AWS accounts and applications.
- With application assignments, you can grant your workforce users in IAM Identity Center single sign-on access to SAML 2.0 applications, such as Salesforce and Microsoft 365
- With multi-account permissions you can plan for and centrally implement IAM permissions across multiple AWS accounts at one time without needing to configure each of your accounts manually.

* STEPS TO START USING IDENTITY CENTER:
  - Enable identity center (also should be using AWS organizations otherwise it will create one in the process)
  - Choose your identity source:
    - Identity Center directory default
    - Active Directory
    - External identity provider
  - After you enable IAM Identity Center, you must choose your identity source. The identity source that you choose determines where IAM Identity Center searches for users and groups that need single sign-on access.
  - Create an administrative permission set: Permission sets are stored in IAM Identity Center and define the level of access that users and groups have to an AWS account.
  - To set up AWS account access for an administrative user in IAM Identity Center, you must assign the user to the AdministratorAccess permission set.
  - Similarly, for different other uses, least privelege sets can be created and accordingly assigned when new users/groups are synced from other directories.
 
- When working in IAM Identity Center, users must be uniquely identifiable. IAM Identity Center implements a user name that is the primary identifier for your users. For most of SAML based integration, it's the user's email address. IAM Identity Center allows you to specify something other than an email address for user sign-in.
- Identity Center enabled applications can work with users and groups for which IAM Identity Center is aware. Provisioning is the process of making user and group information available for use by IAM Identity Center and Identity Center enabled applications.
- There are two types of authentication sessions maintained by IAM Identity Center: one to represent the users’ sign in to IAM Identity Center, and another to represent the users’ access to IAM Identity Center enabled applications, such as Amazon SageMaker Studio or Amazon Managed Grafana. Sessions are cached for 1 hr refreshable, so if user is disabled/deleted, then upto 1 hr, it can still perform or login or create another sessions.
- A permission set is a template that you create and maintain that defines a collection of one or more IAM policies. One can use predefined permission sets or custom permission sets.
- Although IAM Identity Center determines access from the Region in which you enable the service, AWS accounts are global. This means that after users sign in to IAM Identity Center, they can operate in any Region when they access AWS accounts through IAM Identity Center
- IAM service-linked roles: A service-linked role is a unique type of IAM role that is linked directly to IAM Identity Center. It is predefined by IAM Identity Center and includes all the permissions that the service requires to call other AWS services on your behalf

#######################``` AMAZON COGNITO ```#######################    

- Amazon Cognito is an identity platform for web and mobile apps. It’s a user directory, an authentication server, and an authorization service for OAuth 2.0 access tokens and AWS credentials.
- With Amazon Cognito, you can authenticate and authorize users from the built-in user directory, from your enterprise directory, and from consumer identity providers like Google and Facebook.

**User pools**  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5456ba5e-d0ff-4c94-8d40-21d0ff939325)  
- User pools are a user directory with both self-service and administrator-driven user creation, management, and authentication.
- Your organization's SAML 2.0 and OIDC IdPs bring workforce identities into Cognito and your app. The public OAuth 2.0 identity stores Amazon, Google, Apple and Facebook bring customer identities.
- From a user pool, you can issue authenticated JSON web tokens (JWTs) directly to an app, a web server, or an API.

OIDC IdP |	Issue ID tokens to authenticate users
Authorization server	| Issue access tokens to authorize user access to APIs
SAML 2.0 SP	| Transform SAML assertions into ID and access tokens
OIDC SP	| Transform OIDC tokens into ID and access tokens
OAuth 2.0 SP	| Transform ID tokens from Apple, Facebook, Amazon, or Google to your own ID and access tokens
Authentication frontend service	| Sign up, manage, and authenticate users with the hosted UI
API support for your own UI	| Create, manage and authenticate users through API requests in supported AWS SDKs¹
MFA	| Use SMS messages, TOTPs, or your user's device as an additional authentication factor¹
Security monitoring & response	| Secure against malicious activity and insecure passwords¹
Customize authentication flows	| Build your own authentication mechanism, or add custom steps to existing flows¹
Groups	| Create logical groupings of users, and a hierarchy of IAM role claims when you pass tokens to identity pools
Customize ID tokens	| Customize your ID tokens with new, modified, and suppressed claims
Customize user | attributes	Assign values to user attributes and add your own custom attributes

**Identity pools**  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9baf3149-1f11-45e6-b056-f8e01abeb8ee)   
- Set up an Amazon Cognito identity pool when you want to authorize authenticated or anonymous users to access your AWS resources.
- Identity pools use both role-based (RBAC) and attribute-based access control (ABAC) to manage your users’ authorization to access your AWS resources.
- An identity pool can accept authenticated claims directly from both workforce and consumer identity providers.
- The token that your identity pool creates for the identity can retrieve temporary session credentials from AWS Security Token Service (AWS STS).

Amazon Cognito user pool SP	| Exchange an ID token from your user pool for web identity credentials from AWS STS
SAML 2.0 SP	| Exchange SAML assertions for web identity credentials from AWS STS
OIDC SP	| Exchange OIDC tokens for web identity credentials from AWS STS
OAuth 2.0 SP	| Exchange OAuth tokens from Amazon, Facebook, Google, Apple, and Twitter for web identity credentials from AWS STS
Custom SP	| With AWS credentials, exchange claims in any format for web identity credentials from AWS STS
Unauthenticated access	| Issue limited-access web identity credentials from AWS STS without authentication
Role-based access control	| Choose an IAM role for your authenticated user based on their claims, and configure your roles to only be assumed in the context of your identity pool
Attribute-based access control	| Convert claims into principal tags for your AWS STS temporary session, and use IAM policies to filter resource access based on principal tags

- An Amazon Cognito user pool can also fulfill a dual role as a service provider (SP) to your IdPs, and an IdP to your app.
- When to choose what ?

**Usecases**
- Authenticate with a user pool   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f8657b51-ec3e-41b3-b844-a91181f45c67)   
- Access your server-side resources with a user pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ebc22418-984a-4a8c-a503-feeca4a4d4bc)
- Access resources with API Gateway and Lambda with a user pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6766c44a-b632-4410-9dfb-00bd0752f79c)
- Access AWS services with a user pool and an identity pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/7fd3590f-f86c-4555-ad79-0775c7693cee)
- Authenticate with a third party and access AWS services with an identity pool
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/eefe922e-e753-4e5a-a078-045dc7dca4aa)   
- Access AWS AppSync resources with Amazon Cognito
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9b3ba223-8652-46fb-88f5-b16136a0060b)   


**Configuring User pools in Cognito** 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ab0b2cfb-8bbd-4b31-9893-899ccd56c05c)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fb5f69d4-344b-40e8-9c21-e9ae4a922d3e)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/90c96aa1-879d-4626-80d4-2e8ae5b99296)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/c85878a3-185f-4345-a612-027cc4c9fdd6)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bc89fba9-60d1-46eb-a5f2-f22659b61e15)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/f62e3f7e-8286-4023-82ff-6b530b95172e)

**Configuring Identity pools in Cognito** 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/09ada152-e41a-4168-b613-2059c10ac17c)   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9ad67ec5-3aae-468c-b6d9-8f1d994831b0)    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/e948aa05-8ae4-4611-aa64-4545330df7bc)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/08e536da-388b-4b1f-b91b-2101f6fed754)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d29ae56a-8eb5-4600-92dc-fc58dac218d5)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/bd248f73-76e9-4e31-b5cb-35fd6dec4c8c)  


**Lambda Triggers** 
- You can create a Lambda function and then activate that function during user pool operations such as user sign-up, confirmation, and sign-in (authentication) with a Lambda trigger. You can add authentication challenges, migrate users, and customize verification messages.
- When you have a Lambda trigger assigned to your user pool, Amazon Cognito interrupts its default flow to request information from your function. Amazon Cognito generates a JSON event and passes it to your function. The event contains information about your user's request to create a user account, sign in, reset a password, or update an attribute. Your function then has an opportunity to take action, or to send the event back unmodified.
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/81f90980-982d-4095-a19b-63a1dd888a7d)   
- Except for Custom Sender Lambda triggers, Amazon Cognito invokes Lambda functions synchronously. When Amazon Cognito calls your Lambda function, it must respond within 5 seconds. If it doesn't and if the call can be retried, Amazon Cognito retries the call. After three unsuccessful attempts, the function times out. You can't change this five-second timeout value.

**Cognito Hosted UI**  
- Cognito has a hosted authentication UI that you can add to your app to handle sign-up and sign-in workflows
- Using the hosted UI, you have a foundation for integration with social logins, OIDC or SAML
- Can customize with a custom logo and custom CSS
- The hosted UI sign-in webpage uses the following URL format. Note the response_type. In this case, response_type=code for the authorization code grant.
- When you navigate to the /oauth2/authorize endpoint with your custom parameters, Amazon Cognito either redirects you to the /oauth2/login endpoint or, if you have an identity_provider or idp_identifier parameter, silently redirects you to your IdP sign-in page.  
```https://<your_domain>/oauth2/authorize?response_type=code&client_id=<your_app_client_id>&redirect_uri=<your_call```  

- You can view the hosted UI sign-in webpage with the following URL for the implicit code grant where response_type=token. After a successful sign-in, Amazon Cognito returns user pool tokens to your web browser's address bar.    
```https://<your_domain>/login?response_type=token&client_id=<your_app_client_id>&redirect_uri=<your_callback_url>```   

- You can find the JSON web token (JWT) identity token after the #idtoken= parameter in the response.   
Here's a sample response from an implicit grant request. Your identity token string will be much longer.     
```https://www.example.com/#id_token=123456789tokens123456789&expires_in=3600&token_type=Bearer```  

- The Amazon Cognito hosted UI doesn't support custom cross-origin resource sharing (CORS) origin policies. A CORS policy in the hosted UI would prevent users from passing authentication parameters in their requests. Instead, implement a CORS policy in the web frontend of your app.

**Tokens** 
- After your app user successfully signs in, Amazon Cognito creates a session and returns an ID, access, and refresh token for the authenticated user.
- The ID token is a JSON Web Token (JWT) that contains claims about the identity of the authenticated user, such as name, email, and phone_number
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/5817e678-72ed-467f-9c36-40b4ba9f70e8)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/87228a79-ca34-4a62-a810-3c21e884cef5)  

- The signature of the ID token is calculated based on the header and payload of the JWT token. Before you accept the claims in any ID token that your app receives, verify the signature of the token.
- The user pool access token contains claims about the authenticated user, a list of the user's groups, and a list of scopes. The purpose of the access token is to authorize API operations.
- You can use the refresh token to retrieve new ID and access tokens. By default, the refresh token expires 30 days after your application user signs into your user pool. When you create an application for your user pool, you can set the application's refresh token expiration to any value between 60 minutes and 10 years.
- With refresh tokens, you can persist users' sessions in your app for a long time. Over time, your users might want to deauthorize some devices where they have signed in, continually refreshing their session. To sign your user out from a single device, revoke their refresh token.
- ```GlobalSignOut``` accepts a user's valid–unaltered, unexpired, not-revoked–access token. Because this API is token-authorized, one user can't use it to initiate sign-out for another user.
- You can, however, generate an ```AdminUserGlobalSignOut``` API request that you authorize with your AWS credentials to sign out any user from all of their devices.
- Before you can revoke a token for an existing user pool client, you must enable token revocation.
- For verification of JWT tokens: Verifying the Token signature (from JWK url, public, private key pair) and Verifying the token claims: exp, aud, client_id, iss etc...
- You can cache the access tokens so that your app only requests a new access token if a cached token is expired. Otherwise, your caching endpoint returns a token from the cache. This prevents an additional call to an Amazon Cognito API endpoint.
- caching proxy with API Gateway: The cache key is a combination of the OAuth scopes that you request in the scope URL parameter and the Authorization header in the request. The Authorization header contains your app client ID and client secret.   

* ALB Flow with Cognito
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/65795aa9-a593-48f1-bff4-a25f17bf5e4c)  

* ALB Flow with any OIDC ID provider 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/3dcd424d-bd8b-4279-8bed-67717107c0d5)   

* Cognito Identity pool with Social providers (user pool)
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/ff78356a-aa88-42d7-8355-bbd8b799899c)  

* Authentication + Authorization 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/563fda90-37f0-4f2b-bfe4-9163c84f387e)   

**Cognito Sync/AppSync**
- Amazon Cognito Sync is an AWS service and client library that makes it possible to sync application-related user data across devices. Amazon Cognito Sync can synchronize user profile data across mobile devices and the web without using your own backend.

# Deployment

# Troubleshooting and Optimization
