![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/8499d536-3a16-470f-b463-eafe8101d671)# CDA-AWS-DVA-C02
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

**Identity-based and resource-based policies**
- Identity-based policies are permissions policies that you attach to an IAM identity, such as an IAM user, group, or role.
  - AWS Managed policies, Customer managed policies, Inline policies 
- Resource-based policies are permissions policies that you attach to a resource such as an Amazon S3 bucket or an IAM role trust policy.
  - Resource-based policies are inline policies, and there are no managed resource-based policies.
  - The IAM service supports only one type of resource-based policy called a role trust policy, which is attached to an IAM role.
  - Trust policies define which principal entities (accounts, users, roles, and federated users) can assume the role. 


#######################
TASKS REQUIRING ROOT USER CREDENTIALS   
#######################  
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


#######################
IAM USER 
#######################  

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

#######################
IAM POLICIES 
#######################

- IAM Policy inheritance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/99800cc5-9184-4095-8b2a-59fbc71f949a)   

- IAM policy structure and meaning of JSON documents   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0f61aa3e-c15e-4a73-9fb4-1384479a7b99)  
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d6d1ddbe-8947-4970-8cac-bc28f0bdc7e7)   


- IAM policy can be created using policy visual editor   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/93b8242a-d731-4f5b-93be-fcb97829e8ae)  

- Overall for ex. Below shows User which has policies attached via different mechanisms   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/6e7a6b17-7588-47f3-a35d-62036962c697)   

#######################
PASSWORD POLICY IAM 
#######################
- IAM password policy can be managed and user can be required to change their password at certain time or their first logon etc...   
- Password policy can be either chosen as AWS default or it can be new custom policy as defined by admin user.    

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/9f082128-6eeb-4f96-9a0f-cce471281413)   


#######################
MFA
#######################
- Multi factor authentication
- Types of MFA devices
  - Virtual MFA device (google authenticator, Authy)
  - Universal 2nd Factor U2F key ex. YubiKey by Yubico (3rd party)
  - Hardware Key Fob MFA device (Gemalto 3rd party)
  - Hardware Key Fob MFA device for AWS GovCloud (surePassID 3rd party)

- You can register up to 8 MFA devices of any combination with your AWS account root and IAM user.   
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/b91a99e8-877b-4efc-9e10-fcf5c34a2485)   

#######################
LOGON WITH ACCESS KEYS
#######################
- ACCESS KEY ID (USERNAME)
- SECRET ACCESS KEYS (PASSWORD)

- According to purpose of access keys, AWS recommends multiple options like AWS CLI V2, CLOUDSHELL ETC...

#######################
IAM ROLES
#######################

- A role is an IAM identity that you can create in your account that has specific permissions.
- However, instead of being uniquely associated with one person, a role can be assumed by anyone who needs it. A role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.
- Roles are meant to be depending on various use cases, for ex. Assigned directly to the aws services instead of users.
- Few examples shown below:    
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/fd2b5ed5-4f5e-4d72-a72d-4e43466e1969)
- When you create a role, you create two policies:
  - A role trust policy that specifies who can assume the role and a permissions policy that specifies what can be done with the role.
  - You specify the trusted principal who is allowed to assume the role in the role trust policy.  
- For ex. Role creation for EC2 instance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/1234becc-443e-4fa5-a067-837e098ff897)   

#######################
IAM POLICY SIMULATOR
#######################
- One can choose and evaluate the roles and policies attached in real time using this simulator.   
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/11dbc126-c328-4225-bf62-d2d25ff816e2)   

#######################
IAM SECURITY TOOLS 
#######################
- IAM CREDENTIALS REPORT (ACCOUNT LEVEL)
  - report that lists all your account users and the status of their various credentials
 
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/dc27d454-ad21-44b4-981e-b575d4911462)    

- IAM ACCESS ADVISOR (USER LEVEL)
  - shows service permissions granted to a user and when were they last accessed
  - you can use this information to revise the policies, can help in reducing the permissions for least privelege.

![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/d79b24a5-b708-4890-96bf-2fc1596b97ba)     

#######################
IAM BEST PRACTICES
#######################
- DONT'T user ever root user except for AWS account setup
- One physical user = AWS IAM user  
- Assign users to groups and assign permissions to groups
- create a strong password policy
- use and enforce MFA
- create and use Roles for giving permissions to AWS services
- Use Access keys for Programmatic access (CLI/SDK)  
- Audit permission of your account using IAM creds report and access advisor   
- Never share IAM user and access keys

#######################
AWS SHARED RESPONSIBILITY MODEL FOR IAM 
#######################
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

# Deployment

# Troubleshooting and Optimization
