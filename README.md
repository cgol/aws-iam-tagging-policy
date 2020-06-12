# aws-iam-tagging-policy
Cloudformation Template that creates an IAM Managed Policy that can be attached to a FinOps user role or group.
It allows the holder use the Resource Manager Tag Editor to add or modify a Cost Allocation Tag on any AWS resource.

The user, role or group should also be granted the arn:aws:iam::aws:policy/ReadOnlyAccess and probably the arn:aws:iam::aws:policy/job-function/Billing policies to allow console access.

The `CostAllocationTagKey` is a wildcard parameter that specifies the name of the Cost Allocation tag. It will generally be something like 'CostCenter'.

The Policy Actions are obtained from the AWS IAM Documentation [https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_actions-resources-contextkeys.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_actions-resources-contextkeys.html)

For most services the API is serviceName:TagResource but there are exceptions and variations, and not all AWS services allow tagging.
