# Introduction

Welcome to the DevOps labs!

## Prerequisites

A user account that can login into the AWS console The following permissions:

* Launch and delete a CloudFormation template
* Create and delete IAM policies and roles (needed for CloudFormation)
* Create a Virtual Private Cloud (VPC)
* Create Security Groups, Route Tables, Elastic IP (EIP) and association of an Internet Gateway (IGW)
* Create of a T2 Elastic Compute Cloud (EC2) instance
* Create an SSH key created for the region where the CloudFormation template will be launched

## CloudFormation

Open the guide below:

* https://docs.aws.amazon.com/pt_br/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html

It will guide you through the following steps: create, monitor and delete a CloudFormation Stack.

If you are sharing the same account, append your name on the identifiers. For example, stack name and key name.

## Elastic Beanstalk

Organize the distribution of the regions among the participants.

Download the guide on:
* https://s3.amazonaws.com/dreis-id/devops/elastic_beanstalk_hol.docx

## CodeDeploy

* Access CodeDeploy Console
 * https://console.aws.amazon.com/codedeploy/home
* Choose Sample deployment
* Click Next
* Choose In-place deployment
* Click Next
* Choose Amazon Linux
* Choose a Key Pair name (if you haven't created one, check  
 * https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair)
* Customize Tag Value (ex: change from CodeDeployDemo to CodeDeployDemo-username1)
* Click launch instances and wait the completion (this may take a few minutes)
* Click Next
![step5](https://github.com/reisjr/aws-id/blob/master/devops/images/lab_codedeploy_2_step_1.png)
* Change the Deployment Group Name
* Click Next
* Click Next
* Choose the One at a time deployment configuration
* Click Next
* Review all the configurations
* Click Deploy

### Deploy a new version

* Access CodeDeploy Console
 * https://console.aws.amazon.com/codedeploy/home
* Choose the Application you have created on the previous session
* Choose the Deployment group you have created on the previous session
* Choose the Actions -> Deploy new revision
* Choose the Revision Location: s3://aws-codedeploy-us-east-1/samples/latest/SampleApp2_Linux.zip
* Click Deploy on the bottom of the page
