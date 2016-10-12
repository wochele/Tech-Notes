# Scheduling Backups

Scheduled backups run automatically to ensure that backups occur on an ongoing basis.
You can schedule backups to run daily, weekly, or monthly. The scheduled backup can
include multiple clients or a single server.

1. Create a dataset to define the data that is included in the backups.
2. Create a schedule for when the backups should occur.
3. Create a retention policy to define how long to keep the backups in the system.
4. Create a group for the backups.
  - Assign the new dataset to the new group.
  - Assign a schedule to the new group.
  - Assign a retention policy to the new group.
  - Add one or more clients to the new group.
5. Enable scheduling for the group.
