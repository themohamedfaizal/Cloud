# IAM ( Indentity Access Management)

    It is a free service that is used for user and group creation.

- login with the email ID and password that was used during the account creation stage.
- This account is called as the root account and it has access to all the services.
- Its recommended to not use it further or share it with anyone.

## IAM Hands on:

- IAM is a Global service
- Creating user and group
- Giving them permissions to access various AWS services.

# Permissions and Policies in IAM

- When you create an user in AWS, the user will not have any permissions.
- Only when we assign policies to them, they would be able to access the AWS services.
- Try creating an User and giving them permissions.


## Understanding the Policies Structure

Consists of
- Version: policy language version, always include “2012-10-17”
- Id: an identifier for the policy (optional)
- Statement: one or more individual statements (required)
Statements consists of
    - Sid: an identifier for the statement (optional)
    - Effect: whether the statement allows or denies access (Allow, Deny)
    - Principal: account/user/role to which this policy applied to
    - Action: list of actions this policy allows or denies
    - Resource: list of resources to which the actions applied to
    - Condition: conditions for when this policy is in effect (optional)

```
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "1",
    "Effect": "Allow",
    "Principal": {"AWS": ["arn:aws:iam::ACCOUNT-ID-WITHOUT-HYPHENS:root"]},
    "Action": "s3:*",
    "Resource": [
      "arn:aws:s3:::mybucket",
      "arn:aws:s3:::mybucket/*"
    ]
  }]
}
```

## policies hands on

- open two tabs and login with diff accounts to show permissions.
- show default policies in aws ( IAM read only)
- remove users from gorup and show permission denied.
- create a inline IAM read only policy.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor1",
            "Effect": "Allow",
            "Action": "s3:*",
            "Resource": "arn:aws:s3:::testawsbucketfaizal"
        }
    ]
}
```

# Gorup Inheritance.



# Interview questions

- Never User root account
- follow least privilige principle

