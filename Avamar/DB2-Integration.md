# DB2 Integration

- [Restore and Recovery](#restore)

- Each DB2 server host requires the installation of the Avamar Plug-in for DB2 and an Avamar file system client. 
You can back up and restore DB2 databases by using AvamarAdministrator or the DB2 Command Line Processor (CLP)
- The Avamar Plug-in for DB2 supports the following types of backups:
  - Full backups from Avamar Administrator
  - Full, incremental, and delta backups from the DB2 CLP
  - Table space backups from the DB2 CLP
  - Online backups, You can perform an online backup while the database is active. During this type of backup, 
  users and applications can connect to the database and perform transactions. 
  Online backups can either include or exclude archived logs.
  - Offline backups, You can perform an offline backup while the database is inactive. Offline backups do 
  not allow connections to the database.
  - On-demand or scheduled backups from Avamar Administrator. You can perform either on-demand or scheduled 
  backups while the database is online or offline.
  - Backups of load copy images created by db2 load operations with copy yesoption

<a name="restore"></a>
### Restore and Recovery

- The Avamar Plug-in for DB2 supports DB2 database restores from both online and offlinebackups.
- You can restore and recover a database only while the database is offline. 
- The restore and recoveryoperation automatically establishes a connection to the specified database. The 
connection terminates after the restore operation completes
- The following restore and recovery options are available from the Avamar Administrator:
  - Restore and roll forward database
  - Restore only
  - Restore only archive logs from an online backup
  - Recover
- The Avamar Plug-in for DB2 includes the following recovery type options:
  - End of logs
  - Point in Time
  - End of Backup
