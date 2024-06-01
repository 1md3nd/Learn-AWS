# Data Migration from MySQL to Aurora MySQL

In this guide, I will demonstrate how to migrate databases from MySQL to Aurora MySQL.

## Methods of Migration

### 1. Manual Migration

This method involves using `mysqldump` to dump the MySQL data and then load it into Aurora MySQL.

[See Here](./manualMigration/ReadMe.md)

### 2. Using AWS DMS UI

This method involves performing the migration using the AWS interface to transfer the data.

[See Here](./about/usage.md)

### 3. Using AWS CloudFormation

This method involves creating all the necessary resources using a CloudFormation template.

[See Here](./cloudformation/ReadMe.md)