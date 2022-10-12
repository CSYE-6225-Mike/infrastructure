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

