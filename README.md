# MSSQL Docker Composer

### Restoring database
```sql
RESTORE DATABASE IDXDPS FROM DISK=N'/var/opt/mssql/shared/<backup_file>.bak'
WITH REPLACE,
MOVE '<db_name>' TO '/var/opt/mssql/data/<db_name>.mdf',
MOVE '<db_name>_Log' TO '/var/opt/mssql/data/<db_name>_Log.ldf'
GO
```

### Change owner
```sql
ALTER AUTHORIZATION ON DATABASE::<db_name> TO sa;
GO
```
