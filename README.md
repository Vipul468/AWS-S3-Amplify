{
	"Version": "2008-10-17",
	"Statement": [
		{
			"Sid": "AllowAmplifyToListPrefix_d5ejfhobg2dfe_staging_",
			"Effect": "Allow",
			"Principal": {
				"Service": "amplify.amazonaws.com"
			},
			"Action": "s3:ListBucket",
			"Resource": "arn:aws:s3:::amplify-lab-09-06-26",
			"Condition": {
				"StringEquals": {
					"aws:SourceArn": "arn%3Aaws%3Aamplify%3Aus-east-2%3A497938349654%3Aapps%2Fd5ejfhobg2dfe%2Fbranches%2Fstaging",
					"s3:prefix": "",
					"aws:SourceAccount": "497938349654"
				}
			}
		},
		{
			"Sid": "AllowAmplifyToReadPrefix_d5ejfhobg2dfe_staging_",
			"Effect": "Allow",
			"Principal": {
				"Service": "amplify.amazonaws.com"
			},
			"Action": "s3:GetObject",
			"Resource": "arn:aws:s3:::amplify-lab-09-06-26/*",
			"Condition": {
				"StringEquals": {
					"aws:SourceArn": "arn%3Aaws%3Aamplify%3Aus-east-2%3A497938349654%3Aapps%2Fd5ejfhobg2dfe%2Fbranches%2Fstaging",
					"aws:SourceAccount": "497938349654"
				}
			}
		},
		{
			"Effect": "Deny",
			"Principal": "*",
			"Action": "s3:*",
			"Resource": "arn:aws:s3:::amplify-lab-09-06-26/*",
			"Condition": {
				"Bool": {
					"aws:SecureTransport": "false"
				}
			}
		},
		{
			"Sid": "AllowAmplifyToListPrefix_d1zqpnz6jkw64o_staging_",
			"Effect": "Allow",
			"Principal": {
				"Service": "amplify.amazonaws.com"
			},
			"Action": "s3:ListBucket",
			"Resource": "arn:aws:s3:::amplify-lab-09-06-26",
			"Condition": {
				"StringEquals": {
					"aws:SourceArn": "arn%3Aaws%3Aamplify%3Aus-east-2%3A497938349654%3Aapps%2Fd1zqpnz6jkw64o%2Fbranches%2Fstaging",
					"s3:prefix": "",
					"aws:SourceAccount": "497938349654"
				}
			}
		},
		{
			"Sid": "AllowAmplifyToReadPrefix_d1zqpnz6jkw64o_staging_",
			"Effect": "Allow",
			"Principal": {
				"Service": "amplify.amazonaws.com"
			},
			"Action": "s3:GetObject",
			"Resource": "arn:aws:s3:::amplify-lab-09-06-26/*",
			"Condition": {
				"StringEquals": {
					"aws:SourceArn": "arn%3Aaws%3Aamplify%3Aus-east-2%3A497938349654%3Aapps%2Fd1zqpnz6jkw64o%2Fbranches%2Fstaging",
					"aws:SourceAccount": "497938349654"
				}
			}
		}
	]
}
