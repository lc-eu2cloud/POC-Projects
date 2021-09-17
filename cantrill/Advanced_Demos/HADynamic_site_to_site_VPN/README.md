
## Overview - Highly Available, Dynamic, BGP Accelerated Site-to-Site VPN

In this demo, I used CloudFormation templates to create following base infrastructure: (Stage 1)

##### AWS Environment
* 2 virtual servers (EC2 instances, 2 different availability zones, 2 different private subnets)
* transit gateway, transit gateway attachment to AWS VPC using both private subnets
* Routes:
  * default route to transit gateway associated with both private subnets (setting up connectivity to On-prem servers in On-prem environment)  
##### On-prem Environment
* 2 On-prem servers (EC2 instances, 2 different private subnets)
* 2 customer gateways (EC2 instances with private network interface attachments, public subnet)
* internet gateway, internet gateway attachment to On-prem VPC using public subnet
* Routes:
  * default route to internet gateway
  * routes to AWS VPC from On-prem servers in private subnets (setting up connectivity to virtual servers in AWS environment)

After resources were provisioned, I created 2 VPN transit gateway attachments thus creating 2 VPN connections: (Stage 2)
##### IPSec Tunnel Architecture
* 1 customer gateway & 2 IPSec tunnels (AWS endpoints) per VPN connection
  * 2 Outside public IPv4 addresses per tunnel (AWS & On-prem/Customer Gateway), results in encrypted IPSec connectivity over the public internet
  * 2 Inside private IPv4 addresses per tunnel (AWS & On-prem/Customer Gateway), results in raw data transfer between AWS & On-prem environments
  * 1 BGP IPv4 addresss per tunnel (same IPv4 address as the AWS inside private IPv4 address), results in On-prem Customer Gateways peering with AWS environment  

[Project Source](https://github.com/acantril/learn-cantrill-io-labs/blob/master/AWS_HYBRID_AdvancedVPN/readme.md)
