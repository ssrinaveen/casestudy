AWS Lambda Function -> S3 - CSV to Dynamo DB 

By using this repository we can deploy a lambda function in AWS using terraform. It will create a couple of resources in aws like Dynamo DB and S3 Bucket. Whenever a new csv file is uploaded in to a S3 bucket automatically lambda function will trigger and copies data from csv file in to dynamo db.

Requirements:

1. AWS Account
2. Terrform CLI
3. AWS CLI

First download this repository into local machine and install terraform and aws cli tools in your machine. Once it is done please create environment varibles using export in local machine.

Example:

$ export AWS_ACCESS_KEY_ID="YOUR_ACCESS_KEY"
$ export AWS_SECRET_ACCESS_KEY="YOUR_SECRETY_ACCESS_KEY"
$ export AWS_DEFAULT_REGION="us-east-1"

Now move to code repo and make required changes as per your wish in terraform.tfvars file under terraform folder. we are storing our terrform backend file(tfstate) in aws s3 bucket.

Lambda script present under python_lambda_script folder. By default using us-east-1 location for our resources. we can make required changes in script file.

Sample input file present under inputcsv folder and which contains input csv data.