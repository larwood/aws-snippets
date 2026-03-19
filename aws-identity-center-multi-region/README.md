# AWS Identity Center Multi Region Replication Enablement Deep Dive

KMS key policy for the Amazon Web Services video on YouTube

https://www.youtube.com/watch?v=vFg9aQx34AE

## Find and replace variables in KMS policy with your details using an AWS CLI session that is authenticated to the Organization Management account.

```
<MANAGEMENT-ACCOUNT> = $(aws organizations describe-organization --query "Organization.MasterAccountId" --output text)
<ORG-ID> = $(aws organizations describe-organization --query "Organization.Id" --output text)
<SSO-INSTANCE-ARN> = $(aws sso-admin list-instances --query "Instances[0].InstanceArn" --output text)
<IDENTITYSTORE-ID> = $(aws sso-admin list-instances --query "Instances[0].IdentityStoreId" --output text)
```
