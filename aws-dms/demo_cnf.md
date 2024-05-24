# Using Cloudformation DMS Template

## Resources
1. **DMSReplicationSubnetGroup** : Helps us to identify the subnets on the VPC where we can create the replicationInstance.
2. **DMSReplicationInstance** : This is the replation Instance which will perform all the processing.
3. **DMSSourceEndpoint** : The Source Endpoint of the MySQL.
4. **DMSTargetEndpoint** : The Target Endpoint of the Aurora MySQL.
5. **DMSMigrationTask** : The Migration Task which will trigger the migration.

## Parameters
The required parameters when we will create the Cloudformation Stack.

1. **Stage** : The stage in which we want to create the resource.
2. **DmsSecurityGroup** : The security Group which have inbound rule to access the both databases.
3. **SourceDbUsername** : Username for the source MySQL database.
4. **SourceDbPassword** : Password for the source MySQL database.
5. **SourceDbEndpoint** : Endpoint for the source MySQL database.
6. **SourceDbName** : Database name for the source MySQL database (which we want to migrate).
7. **TargetDbUsername** :  Username for the target Aurora MySQL database.
8. **TargetDbPassword** : Password for the target Aurora MySQL database.
9. **TargetDbEndpoint** : Endpoint for the target Aurora MySQL database.
10. **ReplicationInstanceClass** : The replication instance class for DMS.
11. **AllocatedStorage** : The allocated storage for the DMS instance.
12. **SubnetIds** : Subnets for DMS subnet group. Must contain at least two subnets in two different Availability Zones in the same region. 

## Outputs
1. **ReplicationInstanceArn** : The AWS Resource Name for the Replication Instance.
2. **SourceEndpointArn** : Source Endpoint ARN
3. **TargetEndpointArn** : Target Endpoint ARN
4. **MigrationTaskArn** : Migration Task ARN