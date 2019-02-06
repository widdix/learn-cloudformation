# Lab 8: cfn-init

Making use of cfn-init to provision EC2 instances.

## Overview
1. Create a CloudFormation template using cfn-init.
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open `stub.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Install `httpd` with the help of cfn-init by adding metadata to `EC2Instance` (see [Resource Type: CloudFormation Init](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html)).
1. Create a file `/var/www/html/index.html` with `<html><body>Hello World!</body></html>` as content by adding metadata to `EC2Instance` (see [Resource Type: CloudFormation Init](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html)).
1. Start `httpd` with the help of cfn-init by adding metadata to `EC2Instance` (see [Resource Type: CloudFormation Init](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html)).


## Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert `lab8-$username`as stack name. Replace `$username`with your username (e.g. lab8-awittig).
1. Select a random subnet and the only available VPC as **Parameters**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Switch to the **Outputs** tab.
1. Search for **WebsiteURL** and click on the URL.
1. A website showing `Hello World!` should appear.
1. Select your stack by clicking on row of the table again.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the first lab!

## Documentation
* [Resource Type: CloudFormation Init](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html)

## Sample solution
This lab includes a sample solution `sample-solution.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
