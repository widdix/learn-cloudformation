# Lab 10: Estimate Costs

Use a CloudFormationtemplate to calculate the monthly costs.

## Overview
1. Estimate costs of an CloudFormation template.

## Instructions
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose file `learn-cloudformation/lab10-estimate-costs/demo.yaml`.
1. Click **Next** button.
1. Insert `lab10-$username`as stack name. Replace `$username` with your username (e.g. lab10-awittig).
1. Select two random subnets and the only available VPC as **Parameters**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Under **Estimate cost**, you will find a **Cost** link. CLick this link. A new tab will open
1. Explore the calculated costs.
1. Go back to the CLoudFormation tab and click **Cancel** to stop exit the wizzard.
1. Congratulations! You are done with the lab!
