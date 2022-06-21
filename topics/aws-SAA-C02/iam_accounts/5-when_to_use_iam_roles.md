Common uses for IAM Roles:

1) AWS Services - aws service operate on your behalf and they need access rights to perform certain actions.
2) Emergency situations - roles can be obtained if really needed
3) When adding AWS to existing network


External accounts can't be used in AWS directly but an IAM role can be used to make that happen.


Benefits:
1) No AWS credentials on the app - AWS can managed short lived credentials using sts:AssumeRole
2) Uses existing customer logins, for example, user can use login via facebook functionality and that identity can be granted a role to access aws services
3) Scales really well as mentioned above because IAM users have a limit of 5000 users per account
