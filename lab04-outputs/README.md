# Lab 4: Outputs

Use outputs to get access to informations about the resources created by a stack.

## Overview
1. Create a CloudFormation template using outputs.
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open `stub.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add `InstanceId` containing the instance-id of the EC2 instance to the outputs section (see [Outputs section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html) and [Resource Type: EC2 instance](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)).
1. Launching the instance into a public subnet? Otherwise skip this step. Add `PublicIPAddress` containing the public IP address of the EC2 instance to the outputs section: [Outputs section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html) and [Resource Type: EC2 instance](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)).
1. Launching the instance into a private subnet? Otherwise skip this step. Add `PrivateIPAddress` containing the private IP address of the EC2 instance to the outputs section: [Outputs section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html) and [Resource Type: EC2 instance](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)).

## Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert `lab4-$username`as stack name. Replace `$username`with your username (e.g. lab4-awittig).
1. Select a random subnet as parameter for **Subnet**.
1. Insert `t2.micro` as parameter for **InstanceType**.
1. Insert `ami-bff32ccc` (eu-west-1) or `ami-bc5b48d0`(eu-central-1) as parameter for **AMI**.
1. Insert `http://widdix.net/` or a website you own for **URL**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Change to the **Outputs** tab.
1. Find value of `InstanceId` and note it down.
1. Select the **EC2 service** from the main navigation.
1. Search for an EC2 instance with the instance id from the outputs tab.
1. Select the EC2 instance by clicking on the row of the table.
1. Select the action **Get System Log** from the **Actions** menu hidden under **Instance Settings**.
1. You will find the outputs from the load test in the logs.
1. Switch back to the CloudFormation service.
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
* [Outputs section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)
* [Resource Type: EC2 instance](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)

## Sample solution
This lab includes a sample solution `sample-solution.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
