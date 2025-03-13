# CT08SVF-Cloud-Computing-TASK4

**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: ARYA RANI

**INTERN ID**: CT08SVF

**DOMAIN**: CLOUD COMPUTING

**DURATION**: 4 WEEKS

**MENTOR**: NEELA SANTOSH 

This repository contains all files and documentation related to the completion of the 4th task of the cloud computing internship at CODTECH IT SOLUTIONS PVT. LTD., submitted by ARYA RANI (Intern ID: CT08SVF).

**DESCRIPTION OF 4th TASK**

Step 1: Create an IAM Policy and User
Goal: Restrict access to specific resources using IAM.
  1.	Navigate to IAM Console:
      o	Go to AWS Management Console > Services > IAM.
      o	Screenshot 1: Capture the IAM dashboard.
      Heading: IAM Dashboard Overview.
  2.	Create a Custom IAM Policy:
      o	In IAM, go to Policies > Create Policy > Switch to JSON tab.
      o	Paste this policy (replace YOUR_BUCKET_NAME with your bucket name):
json
Copy
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:GetObject", "s3:PutObject"],
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
    o	Name the policy (e.g., S3-ReadWrite-Access).
    o	Screenshot 2: Capture the JSON policy editor.
    Heading: Custom IAM Policy JSON Configuration.
  3.	Create an IAM User:
    o	Go to Users > Add user.
    o	Enter a username (e.g., SecureS3User).
    o	Select Programmatic access and AWS Management Console access.
    o	Attach the policy S3-ReadWrite-Access created earlier.
    o	Screenshot 3: Capture the user summary page with the attached policy.
    Heading: IAM User Creation with Custom Policy.

Step 2: Create a Secure S3 Bucket
Goal: Configure an S3 bucket with encryption, versioning, and blocking public access.
  1.	Create an S3 Bucket:
    o	Go to S3 Console > Create bucket.
    o	Enter a unique bucket name and ensure the region is unchanged.
    o	Screenshot 4: Capture the bucket creation page (region visible).
    Heading: S3 Bucket Creation in Default Region.
  2.	Block Public Access:
    o	Under Block Public Access settings, check Block all public access.
    o	Screenshot 5: Capture the public access blocking settings.
    Heading: S3 Bucket Public Access Block Configuration.
  3.	Enable Versioning:
    o	Go to the bucket’s Properties tab > Bucket Versioning > Enable.
    o	Screenshot 6: Capture the versioning settings.
    Heading: S3 Bucket Versioning Enabled.
  4.	Enable Server-Side Encryption:
    o	Go to the bucket’s Properties tab > Default encryption.
    o	Select AWS Key Management Service (SSE-KMS).
    o	Choose AWS managed key (aws/s3) or create a new KMS key (see Step 3).
    o	Screenshot 7: Capture the encryption settings.
    Heading: S3 Bucket Default Encryption Configuration.

Step 3: Configure AWS KMS Encryption
Goal: Create a KMS key for S3 encryption.
  1.	Create a KMS Key:
    o	Go to AWS KMS Console > Customer managed keys > Create key.
    o	Set Key type as Symmetric and Usage as Encrypt and decrypt.
    o	Add a key alias (e.g., S3-Encryption-Key).
    o	Assign the IAM user as a key user in the key policy.
    o	Screenshot 8: Capture the KMS key policy configuration.
    Heading: KMS Key Policy with IAM User Permissions.
  2.	Apply KMS Key to S3 Bucket:
    o	Return to the S3 bucket’s Default encryption settings.
    o	Select the KMS key you created (e.g., S3-Encryption-Key).
    o	Screenshot 9: Capture the S3 bucket’s KMS key selection.
    Heading: S3 Bucket KMS Encryption Key Assignment.

Step 4: Test and Validate
Goal: Verify security policies and encryption.
  1.	Upload a Test File:
    o	Use the IAM user credentials to log in to the AWS Console.
    o	Upload a file to the S3 bucket.
    o	Screenshot 10: Capture the successful upload.
    Heading: File Upload to S3 Using Restricted IAM User.
    2.	Check Encryption Status:
    o	Select the uploaded file in S3 > Properties > Server-Side Encryption.
    o	Confirm encryption is enabled with the KMS key.
    o	Screenshot 11: Capture the file’s encryption details.
    Heading: S3 Object Encryption Status with KMS.

**Output:**









Intern ID: CT08SVF Cloud Computing Task4
