# Mongo Failover
Exploring MongoDB failover in ReplicaSet of FIVE data-bearing members across TWO datacenters + ONE arbiter.

This template explores the behavior of FIVE data-bearing members across TWO datacenters (ap-southeast-1a & ap-southeast-1b).

This template creates 7 EC2 instances with the following breakdown :

| AWS Resource | MongoDB Member | Availability Zone | Priority |
|:------------:|:--------------:|:-----------------:|:--------:|
| EC2 Instance |     PRIMARY    |  ap-southeast-1a  |    9     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1a  |    8     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1a  |    6     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1b  |    -     |
| EC2 Instance |    SECONDARY   |  ap-southeast-1b  |    -     |
| EC2 Instance |     ARBITER    |  ap-southeast-1b  |    -     |
| EC2 Instance |      -----     |  ap-southeast-1b  |    -     |

NOTE: The last row in the table above is a helper EC2 instance, meant for quick copy-paste of ReplicaSet commands
