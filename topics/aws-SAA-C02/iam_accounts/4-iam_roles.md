IAM Role is another type of identity that exists in AWS.

While IAM users are best suited for one-to-one connections with users (one IAM user identity per one user), IAM role is generally best suited to be used by unknown number or multiple principals (e.g. multiple users can use single role).

IAM Users are meant to be long lived whilst IAM roles are meant to be short lived.

IAM Roles have two types of policies which can be attached:
1) Trust policy
2) Permissions policy

Trust policy controls which identities can assume that role. If an identity is trusted the IAM role will generate temporary security credentials which will only work for short amount of time before they expire. After they expire identity must reassume the role at which point new short term security credentials are generated.

Roles just like IAM users can be referenced within resource policies.

When you assume a role, temporary credentials are generated by AWS service called STS (secure token service), this is an operation that's used to assume the role and get the credentials: sts:AssumeRole