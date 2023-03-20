# Express_App_Demo_AWS
This is the basic source code repository for deploying a hello-world express application on EC2 using AWS CodePipeline.

1. Launch EC2 and install codedeploy agent on it
sudo yum -y update
sudo yum -y install ruby
sudo yum -y install wget
cd /home/ec2-user
wget https://aws-codedeploy-us-east-1.s3.amazonaws.com/latest/install
sudo chmod +x ./install
sudo ./install auto
2. Open ports 22 and 3000
3. Add the IAM role with the policies 'AWSCodeDeployFullAccess' and 'AmazonS3FullAccess' to the EC2 instance
3. Create CodeBuild project
4. Create IAM role for CodeDeploy with the policy 'AWSCodeDeployRole'
5. Create the CodeDeploy application and deployment group.
6. Create the CodePipeline with source as GitHub, CodeBuild as the build tool and CodeDeploy for deploying to the EC2 instance
