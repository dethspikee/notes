IAM Policy - set of security statements to AWS. It grants or denies access to aws products

The following process is used to determine priority of the policy if multiple security statements are used:
1) Explicit denies
2) Explicit allows
3) Implicit denies

Any identity starts with no access, if there is no explicit allow access an implicit deny will be served and identity will be blocked out from the service.

Two different types of policies:
1) Inline - json file that can be assigned to each of the accounts individually, can be though as one to one relationship
2) Managed policies are created as their own object. First you create json file with allow/deny statemets and then you can attach that policy to any identities who need access rights. Can be thought as one to many

Inlines can be used under special circumstances or exceptions to allow / deny specific rights of an individual.
