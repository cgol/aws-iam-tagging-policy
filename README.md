# aws-iam-tagging-policy
Cloudformation Template that creates an IAM Managed Policy that can be attached to a FinOps user role or group.
It allows the holder use the Resource Manager Tag Editor to add or modify a Cost Allocation Tag on any AWS resource.

The user, role or group should also be granted the arn:aws:iam::aws:policy/ReadOnlyAccess and probably the arn:aws:iam::aws:policy/job-function/Billing policies to allow console access.
