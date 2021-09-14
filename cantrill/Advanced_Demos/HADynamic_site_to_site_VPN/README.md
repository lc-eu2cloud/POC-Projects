
## Overview

In this demo, I used CloudFormation templates to create following base infrastructure:

##### AWS Environment
* 2 virtual servers (EC2 instances, 2 different availability zones, 2 different private subnets)
* transit gateway, transit gateway attachment to AWS VPC using both private subnets
* Routes:
  * default route to transit gateway (setting up connectivity to On-prem servers in On-prem environment)  
##### On-prem Environment
* 2 On-prem servers (EC2 instances, 2 different private subnets)
* 2 customer gateways (EC2 instances with private network interface attachments, public subnet)
* internet gateway, internet gateway attachment for On-prem VPC to public subnet
* Routes:
  * default route to internet gateway
  * routes to AWS VPC from On-prem servers in private subnets (setting up connectivity to virtual servers in AWS environment)
