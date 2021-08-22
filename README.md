# Proof of Concept (POC)

## Projects

Mithrandir
* Internal HR application
* ML data modeling application
* Hybrid environment - AWS & on-premises

cantrill
* Dynamic HA site-to-site VPN (BGP) - Transit/Customer Gateway(2xEC2), 2 IPSEC tunnels/VPN connection, DX (VPC peer)
* Hybrid DNS between AWS & on-premises - Route53 inbound/outbound endpoints, on-prem DNS resolvers (EC2), DX (VPC peer)
* Web Identity Federation -

rickroll
* Domain hosting - Route53, website hosting - EC2 & S3
* * Route53 failover routing test via CLI & CloudFormation template (Primary: EC2, Secondary: S3)
* * S3 static website hosting - root & subdomain bucket; testing HTTP redirect
*   * * testing CloudFront distribution domain name URL, S3 origin: static website (subdomain bucket)
*   * * testing CloudFront OAI on S3 origin: static website (subdomain bucket)
