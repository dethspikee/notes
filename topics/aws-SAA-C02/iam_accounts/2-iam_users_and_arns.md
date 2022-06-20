IAM users are identities used for anything requiring long-term AWS access e.g. humans or applications.

IAM starts with principal (an entity).

Principals start off as unidentified by AWS, for them to be able to do anything they must authenticate and be authorized.

Principal (person or an application) makes a request to IAM to interact with aws resources. For that to happen they must authenticate against identity in IAM. Authentication in IAM can be done using Username & Password or access keys.

Once principal becomes an authenticated identity then AWS knows which policies apply to that identity.

ARN - uniquely identify resources within any AWS accounts. Example:

arn:aws:s3:::catgifs -> refers to actual bucket
arn:aws:s3:::catgifs/asterisk -> refers to objects in that bucket


IMPORTANT!
* 5000 IAM Users per account
* IAM User can be a member of 10 groups
