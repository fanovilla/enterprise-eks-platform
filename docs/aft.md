Deploying AFT with github
https://github.com/aws-ia/terraform-aws-control_tower_account_factory/blob/main/examples/github%2Btf_oss/main.tf

login with admin user and load cloudformation stack
from https://github.com/aws-actions/configure-aws-credentials#sample-iam-oidc-cloudformation-template

ClickOps

Inputs

* Stack name - aws10-aft
* GitHubOrg - fanovilla
* OIDCAudience - sts.amazonaws.com (default)
* RepositoryName - aws10-aft

Creates

* role - aws10-aft-Role-il09lnBJpwFj
* idp - token.actions.githubusercontent.com

```json
{
  "Version": "2008-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Federated": "arn:aws:iam::523529320610:oidc-provider/token.actions.githubusercontent.com"
      },
      "Action": "sts:AssumeRoleWithWebIdentity",
      "Condition": {
        "StringEquals": {
          "token.actions.githubusercontent.com:aud": "sts.amazonaws.com"
        },
        "StringLike": {
          "token.actions.githubusercontent.com:sub": "repo:fanovilla/aws10-aft:*"
        }
      }
    }
  ]
}
```

Actions simple workflow


configure AWS creds - https://github.com/aws-actions/configure-aws-credentials#overview

https://github.com/hashicorp/setup-terraform#usage
