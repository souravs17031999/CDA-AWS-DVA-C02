# CDA-AWS-DVA-C02
AWS Certified Developer - Associate

# Development with AWS Services

# Security

## IAM 
- Every User can be either alone or put into a group  i.e. policies can be individually assigned to IAM user (single) or to a group.
- IAM doesn't requires region selection (global)
- 
#######################
CREATING IAM USER 
#######################

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

- IAM Policy inheritance   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/99800cc5-9184-4095-8b2a-59fbc71f949a)   

- IAM policy structure and meaning of JSON documents   
![image](https://github.com/souravs17031999/CDA-AWS-DVA-C02/assets/33771969/0f61aa3e-c15e-4a73-9fb4-1384479a7b99)

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

- Assigned directly to the aws services instead of users.

# Deployment

# Troubleshooting and Optimization
