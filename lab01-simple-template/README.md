# Lab 1: Simple template

Create a S3 bucket with the help of CloudFormation.

## Overview
1. Create a CloudFormation template that will create a S3 bucket named learn-cloudformation-$username. Replace $username with your username (e.g. awittig).
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open `stub.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add an `AWSTemplateFormatVersion` definition to your template (see [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)).
1. Add a `Description` to your template (see [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)).
1. Add a `Resources` section to your template (see [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)).
1. Add a **S3 bucket** to the `Resources` section of your template (see [Resource Type: S3 bucket](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)).
1. Add `BucketName` as the only property to the `Properties` section of the S3 bucket. Be careful: bucket name has to be globally unique. Try `learn-cloudformation-$username` replace `$username` with your username.

## Create a stack based on the template (Management Console)
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert `lab1-$username` as stack name. Replace `$username`with your username (e.g. lab1-awittig).
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Create a stack based on the template (CLI)


## Documentation
* [Template anatomy](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)
* [Resource Type: S3 bucket](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)

## Sample solution
This lab includes a sample solution `sample-solution.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
