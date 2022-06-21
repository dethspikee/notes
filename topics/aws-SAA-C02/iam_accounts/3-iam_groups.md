IAM groups are containers for IAM users, they exist to make organising large sets of IAM users easier.

You cannot login to IAM groups, and IAM groups have no credentials on its own.

There is no such thing as "All users" group.

No nesting - can't have groups within groups.

A policy on a resource can reference IAM users and IAM roles by using ARN. Groups are not a true identity, they cannot be referenced as a principal in a policy. AWS resource can grant access to IAM users but not to IAM group(s).

