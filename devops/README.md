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

![step1](/devops/images/lab_codedeploy_step_1.png)

* Choose Sample deployment
* Click Next

![step2](/devops/images/lab_codedeploy_step_2.png)

* Choose In-place deployment
* Click Next

![step3](/devops/images/lab_codedeploy_step_3.png)

* Choose Amazon Linux
* Choose a Key Pair name (if you haven't created one, check the link below) 
  * https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/ec2-key-pairs.html#having-ec2-create-your-key-pair
* Customize Tag Value (ex: change from CodeDeployDemo to CodeDeployDemo-username1)
* Click Launch instances and wait the completion (this may take a few minutes)
* Click Next

![step4](/devops/images/lab_codedeploy_step_4.png)

* Customize your Application Name (ex: DemoApplication-username1)
* Click Next

![step5](/devops/images/lab_codedeploy_step_5.png)

* Check the revision that will be deployed
* Click Next

![step6](/devops/images/lab_codedeploy_step_6.png)

* Customized the Deployment Group Name (ex: DemoFleet-username1)
* Click Next

![step7](/devops/images/lab_codedeploy_step_7.png)

* A service role will be created to manage your deployments
* Click Next

![step8](/devops/images/lab_codedeploy_step_8.png)
* Choose the One at a time deployment configuration
* Click Next

![step9](/devops/images/lab_codedeploy_step_9.png)

* Review all the configurations
* Click Deploy

### Deploy a new version

* Access CodeDeploy Console
  * https://console.aws.amazon.com/codedeploy/home
* Choose the Application you have created on the previous session
![step2_1](/devops/images/lab_codedeploy_2_step_1.png)
* Choose the Deployment group you have created on the previous session
* Choose the Actions -> Deploy new revision
![step2_2](/devops/images/lab_codedeploy_2_step_2.png)
* Choose the Revision Location to point to a new version
  * s3://aws-codedeploy-us-east-1/samples/latest/SampleApp2_Linux.zip
* Click Deploy at the bottom of the page
