# Lab 5: Dependencies between resources

CloudFormation detects dependencies between resources and creates, updates, or deletes the resources in the correct order.

## Overview
1. Create a CloudFormation template defining dependencies between resources.
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open `stub.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add a reference to `SecurityGroup` to the list of `SecurityGroupIds` of the EC2 instance (see [Reference function](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)).
1. Add a reference to the parameter `KeyName` to the `KeyName`of the EC2 instance (see [Reference function](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)).

## Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert `lab5-$username`as stack name. Replace `$username`with your username (e.g. lab5-awittig).
1. Select a random subnet as parameter for **Subnet**.
1. Select a random key as parameter for **Key Pair**.
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
1. Search for the Security Group attached to the EC2 instance and check if it allows incoming traffic to port 22.
1. Switch back to the CloudFormation service.
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
* [Reference function](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)

## Sample solution
This lab includes a sample solution `sample-solution.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
