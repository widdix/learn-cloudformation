# Lab 9: Rolling update of EC2 instances

Create a CloudFormation stack and use Rolling Updates to update the application version deployed to your EC2 instances.

## Overview
1. Create a CloudFormation stack based on an existing template.

## Instructions
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose file `learn-cloudformation/lab9-rolling-update/demo.yaml`.
1. Click **Next** button.
1. Insert `lab9-$username`as stack name. Replace `$username`with your username (e.g. lab9-awittig).
1. Select two random subnets and the only available VPC as **Parameters**.
1. Insert `1` as **VersionParameter**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Switch to the **Outputs** tab.
1. Search for **ELB* and click on the URL.
1. A website showing `Version 1` should appear.
1. Select your stack by clicking on row of the table again.
1. Select **Update Stack** from the **Actions** menu.
1. Select **Use current template** and click **Next**.
1. Insert `2` as **VersionParameter**.
1. Click **Next**.
1. Click **Next**.
1. Click **Update**.
1. Wait until your stack reaches status **UPDATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Switch to the **Outputs** tab.
1. Search for **ELB** and click on the URL.
1. A website showing `Version 2` should appear.
1. Select your stack by clicking on row of the table again.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!
