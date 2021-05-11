# Mongo Failover
Exploring MongoDB failover in ReplicaSet of FIVE data-bearing members across TWO datacenters.

This template explores the behavior of FIVE data-bearing members across TWO datacenters (ap-southeast-1a & ap-southeast-1b).

This template creates FIVE EC2 instances with the following breakdown :

| AWS Resource | MongoDB Member | Availability Zone | Priority |
|:------------:|:--------------:|:-----------------:|:--------:|
| EC2 Instance |     PRIMARY    |  ap-southeast-1a  |   10     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1a  |    8     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1a  |    6     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1b  |    4     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1b  |    2     |

This template also creates an additional EC2 instance called "temp" used for quick copy-paste of commands.

