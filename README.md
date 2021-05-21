# Mongo Failover
Exploring MongoDB failover in ReplicaSet of FIVE data-bearing members across TWO datacenters.

mongo.yaml file : creates FIVE EC2 instances with the following breakdown and ONE additional EC2 instance for quick copy-paste of commands:

| AWS Resource |   Member Name  |   MongoDB Member  | Availability Zone | Priority |
|:------------:|:--------------:|:-----------------:|:-----------------:|:--------:|
| EC2 Instance |   MongoA1      |     PRIMARY       |  ap-southeast-1a  |   10     |
| EC2 Instance |   MongoA2      |     SECONDARY     |  ap-southeast-1a  |    8     |
| EC2 Instance |   MongoA3      |     SECONDARY     |  ap-southeast-1a  |    6     |
| EC2 Instance |   MongoB1      |     SECONDARY     |  ap-southeast-1b  |    4     |
| EC2 Instance |   MongoB2      |     SECONDARY     |  ap-southeast-1b  |    2     |
| EC2 Instance |    temp        |      -----        |  ap-southeast-1b  |    -     |

test-case.yaml file : creates SEVEN EC2 instances with the following breakdown and ONE additional EC2 instance for quick copy-paste of commands:

| AWS Resource |   Member Name  |   MongoDB Member  | Availability Zone | Priority |
|:------------:|:--------------:|:-----------------:|:-----------------:|:--------:|
| EC2 Instance |   MongoA1      |     PRIMARY       |  ap-southeast-1a  |   12     |
| EC2 Instance |   MongoA2      |     SECONDARY     |  ap-southeast-1a  |   10     |
| EC2 Instance |   MongoA3      |     SECONDARY     |  ap-southeast-1a  |    8     |
| EC2 Instance |   MongoB1      |     SECONDARY     |  ap-southeast-1b  |    6     |
| EC2 Instance |   MongoB2      |     SECONDARY     |  ap-southeast-1b  |    4     |
| EC2 Instance |   MongoB3      |     SECONDARY     |  ap-southeast-1b  |    2     |
| EC2 Instance |   MongoB4      |     arbiter       |  ap-southeast-1b  |    -     |
| EC2 Instance |    temp        |      -----        |  ap-southeast-1b  |    -     |

# External Links

## Reconfiguring a ReplicaSet:
https://docs.mongodb.com/manual/tutorial/reconfigure-replica-set-with-unavailable-members/

## Adjusting Priority of Members in a ReplicaSet:
https://docs.mongodb.com/manual/tutorial/adjust-replica-set-member-priority/
