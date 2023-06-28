# RDS Aurora Postgres Cloudformation template
So I won't spend hours remembering it again

## Prerequisites

You have your VPC stack deployed with exports of:
* `${VPCStackName}-PrivateSubnet1`
* `${VPCStackName}-PrivateSubnet2`
* `${VPCStackName}-VPCID`
* `${VPCStackName}-VPCCIDR`

Example of the expected stack could be seen in `cloudformatino/vpc.yml`

Those parameters are used as a primary config of your DB VPC configuration. Currently, it's expecting that you
either have your app hosted within that VPC or you manually 
define a peering connection (e.g. via `AWS::EC2::VPCPeeringConnection`)

## Deployment
You should have `aws-cli` installed and logged-in to you AWS account.

Then, you run `sh deploy.sh`