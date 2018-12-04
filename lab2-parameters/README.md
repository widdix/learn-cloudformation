# Lab 2: Using parameters

Use input parameters to be able to re-use CloudFormation templates-

## Overview
1. Create a CloudFormation template accepting input parameters and using them to configure an EC2 instance.
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open `stub.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add a parameter called `AMI` of type `String` to the `Parameters` section (see [Parameters section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)).
1. Add a parameter called `InstanceType` of type `String` to the `Parameters` section (see [Parameters section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)).
1. Add a parameter called `Subnet` of type `AWS::EC2::Subnet::Id` to the `Parameters` section (see [Parameters section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)).


## Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert `lab2-$username`as stack name. Replace `$username`with your username (e.g. lab2-awittig).
1. Select a random subnet as parameter for **Subnet**.
1. Insert `t2.micro` as parameter for **InstanceType**.
1. Insert `ami-bff32ccc` (eu-west-1) or `ami-bc5b48d0`(eu-central-1) as parameter for **AMI**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
* [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)
* [Resource Type: EC2 instance](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)

## Sample solution
This lab includes a sample solution `sample-solution.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
