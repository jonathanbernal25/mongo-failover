# Mongo Failover
Exploring MongoDB failover in ReplicaSet of FIVE data-bearing members across TWO datacenters.

This template explores the behavior of FIVE data-bearing members across TWO datacenters (ap-southeast-1a & ap-southeast-1b).

This template creates FIVE EC2 instances with the following breakdown :

| AWS Resource |   Member Name  |   MongoDB Member  | Availability Zone | Priority |
|:------------:|:--------------:|:-----------------:|:-----------------:|:--------:|
| EC2 Instance |   MongoA1      |     PRIMARY       |  ap-southeast-1a  |   10     |
| EC2 Instance |   MongoA2      |     SECONDARY     |  ap-southeast-1a  |    8     |
| EC2 Instance |   MongoA3      |     SECONDARY     |  ap-southeast-1a  |    6     |
| EC2 Instance |   MongoB1      |     SECONDARY     |  ap-southeast-1b  |    4     |
| EC2 Instance |   MongoB2      |     SECONDARY     |  ap-southeast-1b  |    2     |

This template also creates an additional (6th) EC2 instance called "temp" used for quick copy-paste of commands.

# External Links

## For reconfiguring a ReplicaSet:
https://docs.mongodb.com/manual/tutorial/reconfigure-replica-set-with-unavailable-members/

## For adjusting the priority of members in a ReplicaSet:
https://docs.mongodb.com/manual/tutorial/adjust-replica-set-member-priority/
