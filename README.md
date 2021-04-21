# mongo-failover
Exploring MongoDB failover in ReplicaSet of FIVE data-bearing members across TWO datacenters + 1 arbitor.

The goal of this template is to explore the behavior of FIVE data-bearing member MongoDB ReplicaSet across TWO datacenters (ap-southeast-1a & ap-southeast-1b).
CloudFormation template creates 6 EC2 instances with the following breakdown :

| AWS Resource | MongoDB Member | Availability Zone |
|:------------:|:--------------:|:-----------------:|
| EC2 Instance |     PRIMARY    |  ap-southeast-1a  |
| EC2 Instance |    SECONDARY   |  ap-southeast-1a  |
| EC2 Instance |    SECONDARY   |  ap-southeast-1a  |
| EC2 Instance |    SECONDARY   |  ap-southeast-1b  |
| EC2 Instance |    SECONDARY   |  ap-southeast-1b  |
| EC2 Instance |     ARBITOR    |  ap-southeast-1b  |

