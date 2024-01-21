AWS IAM policy to grant full access to a single s3 bucket


```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Allow",
            "Action": [
                "s3:ListAllMyBuckets"
            ],
            "Resource": "arn:aws:s3:::*"
        },
        {
            "Sid": "Statement2",
            "Effect": "Allow",
            "Action": [
                "s3:*"
            ],
            "Resource": [
                "arn:aws:s3:::YOUR-BUCKET/*",
                "arn:aws:s3:::YOUR-BUCKET"
            ]
        }
    ]
}
```