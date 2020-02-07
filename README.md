# cssrepo

CSS Exercise
Using Cloud formation to create a Codecommit repo, CodeBuild, CloudWatch event, and store the event log as a JSON file in a newly generated S3 bucket.



Prerequisites:

Technology: AWS AMAZON - Services - S3 - Create Bucket (give it public accessibility)

Please create an S3 Bucket for primary storage, and copy the following files into it - codebuild.zip, lambda.zip, and repo.zip.


Creating Stack:

Technology: AWS AMAZON - Services - CloudFormation - Create Stack

Stack Parameters:

Stack name: Give your stack a name

CloudWatchEventBucketName: Give your S3 storage a name

CodeBucketName: Insert the name of the initially created S3 Bucket, where the zip files are stored.

Make sure to acknowledge AWS::IAM::Role at the end of the process.


-----------------------------------------------------------------------------

After CloudFormation stack has been created

Please clone the repo. The build will fail at first, considering the content of repo.zip will be pushed to the master branch (check build history for build status).

To Fix Error
Checkout a Branch and fix the error by opening buildspec.yml in your repo folder and remove the last line (# 18 "- pip install -e .")

A log file should be generated and stored in the primary S3 Bucket.

