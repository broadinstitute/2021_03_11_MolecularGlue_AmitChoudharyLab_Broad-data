# 2021_03_11_MolecularGlue_AmitChoudharyLab_Broad

## Overview

[Brief description of the experiment/dataset (2-3 sentences)]

## Project Information

- **Start Date**: 2021_03_11 (of the first batch)
- **Related data repos**: None
- **Metadata Location**: [Link to external metadata tracking system, if applicable]
- **Analysis Repo**: [Link to associated analysis repositories]

Note: All discussions related to this dataset should happen in the GitHub issues of this repository. 

## Processing Details

- **Pipeline Modifications**: [Any changes from standard pipeline]
- **Other notes**:
  - [Any other notes related to processing]

## Data Access Instructions

### Cloning the Repository

```bash
git clone git@github.com:<org>/<repo>.git
```

### Downloading Data Files

```bash
cd <repo>
dvc pull
```

### AWS configuration

The DVC cache is typically stored in an AWS S3 bucket, so you will need run `aws configure` before running `dvc pull`.

If the DVC location is not publicly accessible, you will need AWS credentials to access it.

If the DVC location is not publicly accessible, to access the files stored via DVC, you will need to created a IAM user with the `AmazonS3ReadOnlyAccess` policy attached:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:Get*",
                "s3:List*",
                "s3-object-lambda:Get*",
                "s3-object-lambda:List*"
            ],
            "Resource": "*"
        }
    ]
}
```

