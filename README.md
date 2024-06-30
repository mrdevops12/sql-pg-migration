Task: You need to share your experience of "how" you did the migration in the past and how actual challenges were mitigated through the assignment. What are the migration tools you used to migrate from SQL Server to PostgreSQL? Kindly explain as well

# sql-pg-migration

Planning and Assessment:
   1. Assess the Current Environment:
      Identify Components: List all databases, schemas, tables, views, stored procedures, and functions in SQL Server.
      Evaluate Database: Examine schema, data, dependencies, and custom features that might need special handling during migration.
  2. Compatibility Check:
       Feature Comparison: Compare SQL Server features with PostgreSQL. Note that some SQL Server features may not have direct equivalents in PostgreSQL.
Choosing the Right Tools
   1. AWS Schema Conversion Tool (SCT):
         Purpose: Helps convert SQL Server schemas and migrate data.
         Features: Assesses potential issues and provides conversion capabilities.
   2. pgLoader:
         Purpose: An open-source tool for loading data into PostgreSQL from SQL Server.
          Features: Automates data loading and transformation.
   3. pgAdmin:
         Purpose: Tool for managing and maintaining PostgreSQL databases.
         Use: Manage database objects and perform administrative tasks.
   4. AWS Database Migration Service (DMS):
         Purpose: Facilitates database migration with minimal downtime.
         Features: Supports continuous data replication.
 Migration Steps
      1. Schema Conversion:
             Process: Convert SQL Server schema (tables, views, procedures, etc.) to PostgreSQL format using AWS SCT or similar tools.
      2. Data Migration:
            Process: Transfer data from SQL Server tables to PostgreSQL tables.
            Methods: Use pgLoader for bulk data transfer or AWS DMS for ongoing replication.
      3. Validation:
           Process: Test the migrated database in a staging environment to ensure data integrity and functionality.
           Checks: Compare data, validate stored procedures, and test application functionality.
      4. Deployment:
           Process: Deploy the migrated database to production during a planned maintenance window to minimize downtime.
      5. Post-Migration:
          Monitoring: Closely monitor the new PostgreSQL database for any issues and make necessary adjustments.

Refernce documents: 
       https://docs.aws.amazon.com/dms/latest/sbs/schema-conversion-sql-server-aurora-postgresql.html
       https://docs.aws.amazon.com/SchemaConversionTool/latest/userguide/CHAP_Source.SQLServer.ToPostgreSQL.html
       https://bryteflow.com/sql-server-vs-postgres-how-to-migrate-sql-to-postgresql/
       https://docs.aws.amazon.com/prescriptive-guidance/latest/large-migration-guide/migration-strategies.html
Note:
  I have experience in migration, specifically in Rehost and Recreate migration. However, I do not have experience with database migration from one DB to another 
  DB. Based on my previous migration experience, I would like to provide few high-level overview of the process:

  Assess the environment: Identify all SQL Server database components.
  Check compatibility: Compare SQL Server and PostgreSQL features.
  Choose tools: Use AWS SCT, pgLoader, pgAdmin, and AWS DMS.
  Convert schema: Transform SQL Server schema to PostgreSQL.
  Migrate data: Transfer data using pgLoader or AWS DMS.
  Validate: Test the migrated database thoroughly.
  Deploy: Move to production with minimal downtime.
  Monitor: Keep an eye on the new PostgreSQL database for issues.
  Once you migrate your database from SQL Server to PostgreSQL, you need to ensure your application works correctly with the new database.
