# Lab 6: Mappings

Mappings are mapping a key to a set of values. Typical use case: defining a mapping between a region and an AMI.

## Overview
1. Create a CloudFormation template defining a mapping for AMIs based on the region.
1. Create a CloudFormation stack based on your template.

## Instructions

## Create a template
1. Open ``stub.yaml`` with an editor of your choice. The stub file contains a skeleton to start from.
1. Add a mappings section to your template (see [Mappings section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/mappings-section-structure.html)).
1. Add a mapping named ``RegionAMIMap``. The mapping should contain a region id as key, ``AmazonLinux`` as name and the AMI id as value per region (see [Mappings section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/mappings-section-structure.html))).
1. Use the mapping ``RegionAMIMap`` to define the AMI for the EC2 instance (see [Mappings section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/mappings-section-structure.html)) and [Resource Type: EC2 instance](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html).

### AMIs per region
```
ap-northeast-1 => ami-cbf90ecb
ap-southeast-1 => ami-68d8e93a
ap-southeast-2 => ami-fd9cecc7
eu-central-1 => ami-a8221fb5
eu-west-1 => ami-a10897d6
sa-east-1 => ami-b52890a8
us-east-1 => ami-1ecae776
us-west-1 => ami-d114f295
us-west-2 => ami-e7527ed7
```

## Create a stack based on the template
1. Open [CloudFormation](https://console.aws.amazon.com/cloudformation) in AWS Management Console.
1. Click **Create Stack** button.
1. Select **Upload a template to Amazon S3**.
1. Choose the template file you created for this lab.
1. Click **Next** button.
1. Insert ``lab6-$username``as stack name. Replace ``$username``with your username (e.g. lab6-awittig).
1. Select a random subnet as parameter for **Subnet**.
1. Select a random key as parameter for **Key Pair**.
1. Insert ``t2.micro`` as parameter for **InstanceType**.
1. Insert ``http://widdix.net/`` or a website you own for **URL**.
1. Click **Next** button.
1. Skip next step by clicking on **Next** button.
1. Review your input and click **Create** button.
1. Wait until your stack reaches status **CREATE_COMPLETE**.
1. Select your stack by clicking on row of the table.
1. Select **Delete Stack** from the **Actions** menu.
1. Confirm the deletion of your stack.
1. Congratulations! You are done with the lab!

## Documentation
* [Mappings section](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/mappings-section-structure.html)

## Sample solution
This lab includes a sample solution ``sample-solution.yaml``. Use it if you are stuck during the creation of your template of if you want to review your results.
