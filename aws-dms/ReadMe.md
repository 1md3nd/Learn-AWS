# Data Migration from MySQL to Aurora MySQL

Here I am going demonstrate how can we do migration of databases from MySQL to Aurora MySQL

## We can do migration by different methods

### 1. Using Manual Migration

In this we use `mysqldump` to dump the MySQL data and then load it to Aurora MySQL

[See Here](./manual_mirgation.md)

### 2. Using AWS DMS UI

In this we will perform the migration using the AWS interface to migrate the data.

[See Here](./migration_using_dms.md)

### 3. Using AWS Cloudformation

In this we will create all the resources using Cloudformation Template.

[See Here](./demo_cnf.md)