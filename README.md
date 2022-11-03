# infrastructure

1. Set up AWS cli and add profile for two account
2. Setup the profile
3. Show profiles: aws configure list-profiles
    - Linux or macOS: export AWS_PROFILE=user1
    - Windows: setx AWS_PROFILE user1
4. How to run cloudformation
    - Step 1: aws cloudformation describe-stacks
    - Step 2: aws cloudformation create-stack --stack-name testVPC --template-body file://csye6225-infra.yaml
    - Step 3: aws cloudformation delete-stack --stack-name testVPC
5. For Assignment 4: Change the ami ID to the ami ID built by dev account and share it with demo account. After this, do the step 4 and launch the EC2 instance. Open the public ip and run the web application.

6. For Assignment 5: aws cloudformation create-stack --stack-name testVPC3 --template-body file://csye6225-infra.yaml --profile=mikedemo --region=us-east-1

7. For Assignment 6: aws cloudformation create-stack --stack-name testEC2 --template-body file://csye6225-infra.yaml --capabilities CAPABILITY_NAMED_IAM --profile=mikedemo --region=us-east-1
