# Mongo Failover
Exploring MongoDB failover in ReplicaSet of THREE data-bearing members across TWO datacenters.

**mongo.yaml** file : creates THREE EC2 instances with the following breakdown and ONE additional EC2 instance for quick copy-paste of commands:

| AWS Resource |   Member Name  |   MongoDB Member  | Availability Zone | Priority |
|:------------:|:--------------:|:-----------------:|:-----------------:|:--------:|
| EC2 Instance |   MongoA1      |     PRIMARY       |  ap-southeast-1a  |   10     |
| EC2 Instance |   MongoA2      |     SECONDARY     |  ap-southeast-1a  |    8     |
| EC2 Instance |   MongoB1      |     SECONDARY     |  ap-southeast-1b  |    6     |
| EC2 Instance |    temp        |      -----        |  ap-southeast-1b  |    -     |

# External Links

## Reconfiguring a ReplicaSet:
https://docs.mongodb.com/manual/tutorial/reconfigure-replica-set-with-unavailable-members/

## Adjusting Priority of Members in a ReplicaSet:
https://docs.mongodb.com/manual/tutorial/adjust-replica-set-member-priority/
