# Lab 11: Output exports

Use export outputs to get publish informations about the resources created by a stack. Use `!ImportValue` to get access to the exported values in other stacks.

## Overview
1. Create a CloudFormation template that exports values
2. Create a CloudFormation template that imports values.
1. Create two CloudFormation stacks based on your templates.

## Instructions

## Create export template
1. Open `stub-export.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add the three missing [exports](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html) to the outputs.

## Create import template
1. Open `stub-import.yaml` with an editor of your choice. The stub file contains a skeleton to start from.
1. [Import](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-importvalue.html) the security group and subnet id.

## Create export stack based on export template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the export template file you created for this lab.
1. Click **Next** button.
1. Insert `lab11export-$username` as stack name. Replace `$username` with your username (e.g. lab11export-awittig).
1. Select a VPC as parameter for **VPC**.
1. Select a subnet as parameter for **Subnet**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.

## Create import stack based on import template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the expot template file you created for this lab.
1. Click **Next** button.
1. Insert `lab11import-$username` as stack name. Replace `$username` with your username (e.g. lab11import-awittig).
1. Set the parameter **ExportStackName** to the name of the export stack `lab11export-$username` (e.g. lab11export-awittig)
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.

## Clean up
1. Select your import stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Select your export stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Sample solution
This lab includes a sample solution `sample-solution-export.yaml` and `sample-solution-import.yaml`. Use it if you are stuck during the creation of your template of if you want to review your results.
