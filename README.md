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
  - 

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

**AWS MANAGED POLICY VS CUSTOMER MANAGED POLICY**
- Managed policies that are created and managed by AWS (AWS MANAGED POLICIES)   
- Managed policies that you create and manage in your AWS account. Customer managed policies provide more precise control over your policies than AWS managed policies. You can create, edit, and validate an IAM policy in the visual editor or by creating the JSON policy document directly.   

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

## Identity providers and federation 
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


# Deployment

# Troubleshooting and Optimization
