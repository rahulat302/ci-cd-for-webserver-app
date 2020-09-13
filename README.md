README file

Instructions:

Create CodeBuild service role and policy.
https://docs.aws.amazon.com/codebuild/latest/userguide/setting-up.html#setting-up-service-role


EC2 User Data Script to install the CodeDeploy Agent.

#!/bin/bash
sudo yum update -y
sudo yum install -y ruby wget
wget https://aws-codedeploy-eu-west-1.s3.eu-west-1.amazonaws.com/latest/install
chmod +x ./install
sudo ./install auto
sudo service codedeploy-agent status



