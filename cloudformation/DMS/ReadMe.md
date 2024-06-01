# Using CloudFormation DMS Template

## Resources
1. **DMSReplicationSubnetGroup**: Defines the subnets in the VPC where the replication instance can be created.
2. **DMSReplicationInstance**: The replication instance that performs all the processing tasks for data migration.
3. **DMSSourceEndpoint**: The source endpoint configuration for the MySQL database.
4. **DMSTargetEndpoint**: The target endpoint configuration for the Aurora MySQL database.
5. **DMSMigrationTask**: The migration task that triggers the migration process.

## Parameters
The required parameters for creating the CloudFormation stack:

1. **Stage**: The deployment stage in which to create the resources (e.g., dev, prod).
2. **SourceDbUsername**: Username for the source MySQL database.
3. **SourceDbPassword**: Password for the source MySQL database.
4. **SourceDbEndpoint**: Endpoint for the source MySQL database.
5. **SourceDbName**: Name of the database in the source MySQL database that we want to migrate.
6. **TargetDbUsername**: Username for the target Aurora MySQL database.
7. **TargetDbPassword**: Password for the target Aurora MySQL database.
8. **TargetDbEndpoint**: Endpoint for the target Aurora MySQL database.
9. **ReplicationInstanceClass**: The instance class for the replication instance (e.g., dms.t2.medium).
10. **AllocatedStorage**: The allocated storage for the DMS instance.
11. **VPCId**: The VPC ID where both MySQL and Aurora MySQL databases are hosted.
12. **SubnetIds**: Subnets for the DMS subnet group. Must contain at least two subnets in two different Availability Zones in the same region.

## Outputs
1. **SecurityGroupId**: The ID of the security group for DMS.
2. **ReplicationInstanceArn**: The Amazon Resource Name (ARN) of the replication instance.
3. **SourceEndpointArn**: The ARN of the source endpoint.
4. **TargetEndpointArn**: The ARN of the target endpoint.
5. **MigrationTaskArn**: The ARN of the migration task.