# NEver User root account

# follow least privilige principle


## Policies Structure

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
