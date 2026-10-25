# AWS IAM Access Control

A selected set of IAM policy examples and implementation notes.

## Repository structure

```text
aws-iam-access-control/
├── README.md
├── documentation/
│   └── implementation-steps.md
└── policies/
    ├── ec2-admin-policy.json
    ├── ec2-support-policy.json
    └── s3-support-policy.json
```

## Attribution

The selected policy examples and implementation guide in this repository are derived from [VanshPatyal/aws-iam-access-control-project](https://github.com/VanshPatyal/aws-iam-access-control-project) and are included with permission. This repository contains only selected files, not the complete original project.

## Important policy warning

The included policy JSON files are copied as provided, but their actual permissions do not match some filenames and descriptions: `ec2-support-policy.json` allows `ec2:*`; `ec2-admin-policy.json` allows S3 list/get actions; and `s3-support-policy.json` allows EC2 describe actions. Do not attach these policies as-is. Review and test every action and resource in a safe AWS environment first.
