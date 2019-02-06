# Lab 3: Using build-in functions

Use input parameters to be able to re-use CloudFormation templates.

## Overview
1. Create a CloudFormation template using build-in functions `Fn::Base64` and `Fn::Sub`.
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open `stub.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Use functions `Fn::Base64` and `Fn::Sub` to combine the following Bash script and inject it into the EC2 instance with the help of `UserData`. $URL needs to be replaced with the template parameter named `URL` (see [Build-in functions](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html)).


Bash script installing httpd-tools and running a small HTTP load test.

```
#!/bin/bash -ex
yum install -y httpd-tools
ab -n 1000 -c 4 $URL
```


## Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert `lab3-$username`as stack name. Replace `$username`with your username (e.g. lab3-awittig).
1. Select a random subnet as parameter for **Subnet**.
1. Insert `t2.micro` as parameter for **InstanceType**.
1. Insert `ami-bff32ccc` (eu-west-1) or `ami-bc5b48d0`(eu-central-1) as parameter for **AMI**.
1. Insert `http://widdix.net/` or a website you own for **URL**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
[Build-in functions](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html)

## Sample solution
This lab includes a sample solution `sample-solution.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
